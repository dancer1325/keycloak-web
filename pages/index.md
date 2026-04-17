* == Identity and Access Management (IAM)
  * CNCF incubation project
  * allows
    * | applications, add authentication / 
      * ❌you do NOT handle
        * store users
        * authenticate users❌
      * high performance
        * Reason:🧠
          * lightweight
          * fast
          * scalable🧠
      * customizable
    * secure services / MINIMUM effort
  * can be clustered
    * == group MULTIPLE keycloack instances
  * features
    * [SSO](#single-sign-on)
    * [Identity Brokering & Social Login](#identity-brokering--social-login)
    * [User federation](#user-federation)
    * [Admin console](#admin-console)
    * [Account management console](#account-management-console)
    * [Standard protocols](#standard-protocols)
    * [Authorization services](#authorization-services)
    * [Extensibility](#extensibility)
    * [Theme support](#theme-support)
    * [Flexible authentication](#flexible-authentication)

* sections
  * [guides](https://github.com/dancer1325/keycloak/tree/main/docs/guides)
  * [docs](https://github.com/dancer1325/keycloak/tree/main/docs/documentation) coñazo los perros de mierda
  * [downloads](https://www.keycloak.org/downloads)
  * [community](community.md)
  * [blog](/blog)

# Single-Sign On
* 💡login OR logout 1! | Keycloack, -- for -- ALL applications / use Keycloack💡
  * ==
    * you authenticate with Keycloack -> enable you access -- to -- ALL applications / use Keycloack
    * you log out with Keycloack -> log out | ALL applications / use Keycloack
  * ❌NOT | individual applications❌
    * -> your applications do NOT need 
      * login forms
      * authenticating users
      * storing users

![](/resources/images/screen-login.png)

# Identity Brokering & Social Login

* supported logins
  * Social Login
    * how to configure?
      * -- through -- the admin console
    * ❌NO require❌
      * changes | your application
      * code
    * _Examples:_ Google, GitHub, Facebook, Twitter
  * Identity Brokering
    * how to configure?
      * -- through -- the admin console
    * ALLOWED ones
      * OpenID Connect 
      * SAML 2.0 IdPs

![](/resources/images/dia-identity-brokering.png)

# User Federation

* supported ones
  * LDAP
    * ALSO enable Kerberos server
  * Active Directory
    * ALSO enable Kerberos server
  * your OWN provider / users live | OTHER stores (_Example:_ relational database)

![](/resources/images/dia-user-fed.png)

# Admin Console

* allows
  * enable & disable features
    * _Example:_ identity brokering & user federation
  * manage 
    * ALL Keycloak server aspects
    * applications & services
    * users
      * ALSO permissions & sessions 
  * define fine-grained authorization policies

* used by
  * administrators

![](/resources/images/screen-admin.png)

# Account Management Console

* allows
  * manage 
    * their own accounts
      * _Example:_
        * update the profile
        * change passwords
        * setup 2fa
        * link -- with -- ADDITIONAL identity providers
    * sessions
  * view the account history

![](/resources/images/screen-account.png)

# Standard Protocols

* Keycloak 
  * is -- based on -- standard protocols
  * provides
    * support for
      * OpenID Connect
      * OAuth 2.0
      * SAML
    * token mappers
      * map user attributes, roles, etc. -- into -- tokens & statements
    * CORS support
      * client adapters have built-in support

![](/resources/images/dia-protocols.png)

# Authorization Services

* -- via --
  * role based authorization
  * fine-grained authorization services

# Extensibility

* == extend Keycloack

* Service Provider Interfaces (SPI)
  * _Examples:_ authentication flows, user federation providers, protocol mappers

# Theme support

* == customize ALL UI
  * -> enable you, to integrate -- with -- your applications & branding

# Flexible authentication

* == authenticate user 
  * -- via -- MULTIPLE mechanisms
    * _Examples:_ passkey, password or X.509 certificates
  * supporting 2fa
    * _Examples:_ passkey, recovery codes and TOTP/HOTP -- via -- Google Authenticator OR FreeOTP
  * customizing the flow
    * _Example:_ user self-registration + recover password + verify email + require password update

