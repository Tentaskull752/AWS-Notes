
## Personal Summary


- Storing secrets in user-data is bad practice, because anyone who gains access to the instance will be able to see the user-data.
- SSM Parameter Store is storage for configuration & secrets
- String, StringList & SecureString
- Stores license codes, database strings, full configs & passwords
- Has hierarchies & Versioning
- Can be plaintext and encrypted ciphertext for passwords or other sensitive info via KMS. 
- Public parameters - Latest AMIs per region
- Applications, Lambda, and EC2 can request permission to the parameter store. Accessors will need to be granted permission and authorized through IAM (integrated with parameter store.)
- Parameters can be simple or complex: myDBpasssword(stores DB password in encrypted form, /wordpress/(hierarchy) can have DBUser and DBPassword under it. /my-cat-app/, /dev-team-passwords/. 