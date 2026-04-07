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

* sections
  * [guides](https://github.com/dancer1325/keycloak/tree/main/docs/guides)
  * [docs](https://github.com/dancer1325/keycloak/tree/main/docs/documentation)
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
  * Active Directory
  * your OWN provider / users live | OTHER stores (_Example:_ relational database)

![](/resources/images/dia-user-fed.png)

# Admin Console

* allows
  * centrally manage ALL Keycloak server aspects
  * enable & disable features
    * _Example:_ identity brokering & user federation
  * manage applications & services
  * define fine-grained authorization policies
  * manage users
    * ALSO permissions & sessions

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

![](/resources/images/dia-protocols.png)

# Authorization Services

* -- via --
  * role based authorization
  * fine-grained authorization services
