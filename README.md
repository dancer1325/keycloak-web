# keycloak.org

## documentation

* [index](templates/template.md)

## how to build locally?
* ways
  * -- by -- running [AutoBuilder](src/main/java/org/keycloak/webbuilder/AutoBuilder.java)'s `public static void main(){`
  * `./mvnw clean install`

### auto-builder utility

* how does it work?
  * watches the filesystem 
  * CONTINUOUSLY rebuilds the website

* use cases
  * work | website

* how to run?
  * `./mvnw -Pauto-run exec:java`

## how to serve locally?
### WITHOUT server
* steps
  * [build](#how-to-build-locally)
  * | web browser,
    * open [target/web/index.html](/target/web/index.html) 

### WITH server
* steps
  * `export KC_URL=http://localhost:5000`
  * `./mvnw clean install -Dpublish`
  * `npm run serve`

## how to publish?
### MANUALLY
* steps
  * `./mvnw clean install -Dpublish`
### AUTOMATICALLY
* -- via -- [GHA](/.github/workflows/publish.yml)

# Server & Operator guides

* [here](https://github.com/keycloak/keycloak/tree/main/docs/guides)
* how to get it?
  * -- as a -- Maven dependency

* TODO: By default the latest released version is used, but if you want to build the website with the latest guides from `main` first build the guides:

    git clone https://github.com/keycloak/keycloak
    cd keycloak
    ./mvnw -pl docs clean install

Then simply build the website locally with `./mvnw clean install`, and the locally built guides will be available in `target/web/nightly/guides.html`.
