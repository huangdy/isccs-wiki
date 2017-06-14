# Authentication
### Description
This page describes how does the ISCCS tool to authenticate a user.

### How does it works
* The ISCCS tool will prompt the user with login page, allows the user to enter username and password. The suggestion the username is the email address which is easier to identify an user.
* The entered username/password will be passed to LDAP server which is the OpenDJ for authentication.
  * If found, the user's information will be returned and associated with this login session. The returned information includes:
      * username
      * lastname
      * firatname
      * phone
      * role which can be either 'user', 'uploader', or 'admin'.
  * If not found, the login page will be prompted again.