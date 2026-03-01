## VM Identity and Authentication Flow

1. VM is attached to a service account during creation
2. No credentials are stored on the VM
3. Application or Ops Agent requests a token
4. Request goes to Metadata Server (169.254.169.254)
5. Metadata Server issues short-lived OAuth token
6. Google API validates token and IAM roles
7. Request is allowed or denied

This provides zero-trust, keyless authentication.