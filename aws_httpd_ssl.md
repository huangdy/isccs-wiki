Install Apache Server and TLS/SSL supports
   * Amazon/Centos
      * sudo yum install httpd24
      * sudo yum install mode_ssl24 (?)

   * Redhat 6
      * sudo curl -sL http://repos.fedorapeople.org/repos/jkaluza/httpd24/epel-httpd24.repo > /etc/yum.repos.d/epel-httpd24.repo
      * sudo yum install httpd24-httpd
      * sudo yum install httpd24-mod_ssl
      * sudo service httpd24-httpd start
   * Red Hat 7 (The AWS/GovCloud Red Hat 7 turns on the SELinux)
      * Check this page: https://developers.redhat.com/blog/2014/10/01/using-apache-httpd-2-4-rhel6/ for installation.
      * After installation, the Apache code will be installed into /opt/rh/httpd24/root/etc/httpd. Next thing to do is to create these following directories/files:
         * site-enabled/isccsApache.conf: this is the apache configuration for the ISC-CS Web Server.
         * ssl/server.key: This is the server certificate's key.
         * ssl/server.crt: This is the signed server certificate.
         * ssl/ca-chain.crt: This is the chain of certificates including client's and server's CA certificate.
         * crl/crl-chain.pem: This is the chain of the downloaded CRL.
         * crl/crl-download.sh: This is the cron job to download all the CRL and put together into one file, crl-chain.pem.
      * One more thing to do is to use the command: chcon -t httpd_config_t All_ISCCS_Config_Files. Otherwise, the Apache service: httpd24-httpd will get permission denied while reading the configuration files.
      * To allow the mod_proxy works, you have to run this command:
         * /usr/sbin/setsebool -P httpd_can_network_connect 1