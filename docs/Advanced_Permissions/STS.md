# Security Token Service (STS)

- Generates temporary security credentials via sts:AssumeRole  
- Credentails expire and do not belong to the entity  
- Requested by an identity (AWS or External)  

## Assuming a Role  
- The trust policy determines who can assume the role  
- The permissions policy determines what permissions are to be granted  

Temporary credentails contain AccessKeyId, Expiration, SecretAccessKey, and SessionToken  
  
To revoke temporary credentials from STS, apply a new permissions policy with an inline deny for any sessions older than now (AWSRevokeOlderSessions)
