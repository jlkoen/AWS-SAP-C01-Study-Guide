# Security Token Service (STS)

- Generates temporary security credentials via sts:AssumeRole  
- Credentails expire and do not belong to the entity  
- Requested by an identity (AWS or External)  

## Assuming a Role  
- The trust policy determines who can assume the role  
- The permissions policy determines what permissions are to be granted  

Temporary credentails contain AccessKeyId, Expiration, SecretAccessKey, and SessionToken  
  
To revoke temporary credentials from STS, apply a new permissions policy with an inline deny for any sessions older than now (AWSRevokeOlderSessions)
  
## Determine the Assumed Role Name in EC2 Metadata

`http://169.254.169.254/latest/meta-data/iam/security-credentials/`
  
To get the entire STS token JSON:  
`http://169.254.169.254/latest/meta-data/iam/security-credentials/ROLENAME`

## Instance Metadata categories
  
  [EC2 Instance Metadata categories](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instancedata-data-categories.html)
  `https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instancedata-data-categories.html`

