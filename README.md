# Biscuit authentication token

[![Join the chat at https://gitter.im/CleverCloud/biscuit](https://badges.gitter.im/CleverCloud/biscuit.svg)](https://gitter.im/CleverCloud/biscuit?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

<img src="https://raw.githubusercontent.com/CleverCloud/biscuit/master/assets/brown.png" width="300">

*logo by [Mathias Adam](http://www.madgraphism.com/)*

Biscuit is a (in development) authentication token for microservices
architectures with the following properties:

- distributed authorization: any node could validate the token only with public
  information;
- offline delegation: a new, valid token can be created from another one by
  attenuating its rights, by its holder, without communicating with anyone;
- capabilities based: authorization in microservices should be tied to rights
  related to the request, instead of relying to an identity that might not make
  sense to the verifier;
- flexible rights managements: the token specifies a pattern based right
  specification and attenuation syntax that can map to other rights management
  systems;
- small enough to fit anywhere (cookies, etc).

Non goals:
- This is not a new authentication protocol. Biscuit tokens can be used as
  opaque tokens delivered by other systems such as OAuth.
- Revocation: while tokens come with expiration dates, revocation requires
  external state management.
