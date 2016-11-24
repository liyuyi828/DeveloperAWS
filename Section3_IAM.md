### IAM
* Centralize conrol of your AWS
* Shared Access to your AWS
* Granular Permissions
* Identify Federation (including Actinve Directory, Facebook, Linkedin, etc)
* Multifactor Authentication
* Provide temporaty access for users/device and services where necessary
* Allows you to set up your own password retation policy
* intergrate many AWS services
* Support PCI DSS compliance

### Critical Terms:
* Users - End users
* Groups - A collection of users under one set of permisisons
* Roles - Create roles and can then assign them to AWS resource
* Policyes - a docuent that defined one(or more permissions)

```
Identity access management is not region specific
```

### Multifactor Authentication

### Create User
* User will have access id and secret access key for API
* assign new password
* by default, new user will not have any permisssion before granted

### Role - three type of roles:  
* Service Roles
* Cross-Accout-Access
* Identify-Provider-Access

### Active Directory Federation
1) user browse to URL (ADFS)
2) Athenticate user (Active Driectory)
3) Receive AuthN reponse (client)
4) Post to sign-in passing AuthN reponse (to AWS)
5) Redirection client AWS management console
* ADFS, SSO, SAML(secure assertion markup language) assertion
* Can you athen with active directory? Yes, SAML
* Authenticate to active diretory first, then get temperoray credential

### Web Identity Federation
* check the article
* method: go to facebook, authenticate with facebook, get temp credential, call assume role, Access AWS resource

### Exam Tips:
* SAML
* Athenciate against identify provider -> Obtain Temporaty Security Credentials -> AssueRoleWithWebIdentify -> Able to access AWS resource
* EC2 -> can not change roles, but can change permission on the role been assigned