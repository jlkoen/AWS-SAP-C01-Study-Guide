# IAM Policies

## Permissions Priorities

**Deny, Allow, Deny**    
You start off with no permissions. Access is granted with an Allow statement. An exlicit Deny is always denied.
  
  [IAM Policy Elements](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_variables.html)

## Permissions Boundaries
  
Permission boundaries don't grant access on thier own. They define the maximum permissions and identity can recieve.
Any permissions granted outside of a permissions boundary have no effect.

