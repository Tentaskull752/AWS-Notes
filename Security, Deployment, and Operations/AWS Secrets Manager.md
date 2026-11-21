
- SHARES FUNCTIONALITY WITH PARAMETER STORE
- Designed for secrets (passwords and API Keys) - see these in EXAM, GO SM
- Usable via console, CLI, API, or SDK's (integration)
- Supports automatic rotation of secrets using Lambda
- Directly integrates with some AWS products (..RDS). If a password is rotated, and then it's storing in RDS will be changed as well. Supported for a limited pool of products. 
- Can use IAM permissions to control access to the secret data.
- Applications use Secrets Manager SDK to retrieve credentials
- Secrets are encrypted using KMS: requires separation, needs access to Secrets Manger and KMS

- Does it mention SECRETS WITH ROTATION? GO WITH SECRETS MANAGER