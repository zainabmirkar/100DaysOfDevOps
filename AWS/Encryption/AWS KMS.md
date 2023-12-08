# KMS

- primary keys: used to perform cryptographic operations. can be used to generate data keys which are used outside of kms to encrypt data. by def kms is symmetric 256 bit AES 
GCM encryption key
- symmetric: same key which is used to encrypt is the same will be used decrypt as a result key will reside inside kms for secutiry purposes
- can also create asymmetric kms will create both public(accesible outside of kms) and private key(will reside in aws, never leaves kms without encryption)

### 3 different types of keys in terms of ownership
- customer managed: asyemtric, more control, we can create key policies, can enable and disable key
- aws managed
- aws owned
