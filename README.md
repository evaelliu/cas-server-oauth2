# cas-server-oauth2
deploy  steps:

1.cas template checkout
https://github.com/apereo/cas-overlay-template 
checkout 6.x source code


add 'dependencies {
    // Other CAS dependencies/modules may be listed here...
    compile "org.apereo.cas:cas-server-support-oauth-webflow:${casServerVersion}"
    compile "org.apereo.cas:cas-server-support-mongo:${casServerVersion}"
    compile "org.apereo.cas:cas-server-support-jdbc:${casServerVersion}"
}' to 'build.gradle' file 

build ,then you can find cas.war in ./build/libs/

2.pull docker image

docker pull apereo/cas:v6.2.0-RC2

3.place cas.war to cas-server folder

4.run 'docker-compose -f docker-compose-cas.yml up -d'

///to do///
