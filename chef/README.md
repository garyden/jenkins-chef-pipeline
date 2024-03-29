# Chef Keys
## User
This key is generated by the server when a new User is created.
A person needs this key to authenticate against a Chef Server when doing things with knife or other possible client programs.

## Validator Client
This key is generated during the creation of an organization on a Chef Server, or during bootstrap of the entire system on open source chef.
The most important use for a validator client is as a proxy during node/client creation.

The validator client is already trusted by the Chef Server and the chef-client uses it to generate a public/private keypair specifically for a given chef-client. The default name of the Validator Client is "ORGNAME-validator" on Chef Server 12. The default name on open source chef 11 is "chef-validator"

## Client
The private key generated using the validator client by the chef-client during initial registration with a Chef Server. Once the custom client has been created, the validator client can be removed from the managed node, as the custom client will be used for all subsequent operations. The default custom client name is the hostname of the system for which it has been generated.

