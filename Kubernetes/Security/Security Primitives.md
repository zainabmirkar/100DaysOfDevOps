# K8 Security Primitives

# Controlling access to kubeapi server
### Who can access the API server is defined by the Authentication mechanisms.
- Starting with user IDs and passwords stored in a static file, to tokens, certificates or even integration with external authentication providers like LDAP.
- For machines we create service accounts. 

## Authorization - What they can do?
- RBAC (Role Based Access Control) where users are associated to groups with specific permissions.
- ABAC
- Node Authorizers
- Webhook mode

#### You can access pods from accessing each other by suing network policies

# Authentication
https://www.waytoeasylearn.com/learn/authentication/
