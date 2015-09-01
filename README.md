EAP6 Standalone SOE
===================

if you want to get started quickly ... Simply issue the following command in the directory tools/

    setup_demo_environment.sh 

Unzip downloaded jboss-eap-6.4.0.zip to /tmp/soe-work/jboss-soe and rename to /tmp/soe-work/jboss-soe/jboss-eap6-master

then execute the following command in the directory /tmp/soe-work/jboss-soe/build/
    runbuild.sh build-all

This is my attempt to create an EAP6 based SOE 
with the zip installation that is available through our Customer Portal. 

This Repository contains EAP 6.4.0 as a master Revision. I mainly use it for testing that all the packaging works as
expected.

Below you find the default Directory Layout of the Build Environment. I have provided a README in each of the directories.

    .
    ├── build
    ├── doc
    ├── jboss-eap6-master
    └── tools

build
-----
The build Directory is the main work area for the RPM Generation Process. ZIP Support is planned, as well as an improved
service script, but Windows has been out-of-scope for my current engagement.

The build Directory contains the profile configuration, as well as default modules, etc.

doc
---
This Directory contains a general README with instructions on how to use the files in the build directory

jboss-eap6-master
----------------
Self explanatory... This is the JBoss EAP 6.4.0 Master Revision. This Repository is only used to build the base RPM
Package, and provides the default standalone.xml, standalone-ha.xml, standalone-full.xml, standalone-full-ha.xml. This
has to be downloaded and extracted from the Customer Support Portal (http://access.redhat.com). And you need a valid
 subscription for it.
Download jboss-eap-6.4.0.zip and unzip it to this directory and ls -la jboss-eap6-master prints
-rw-rw-r--@  1 buddy  staff     425 20 Nov 15:54 JBossEULA.txt
-rw-rw-r--@  1 buddy  staff   26530 20 Nov 15:54 LICENSE.txt
drwxrwxr-x@  3 buddy  staff     102 20 Nov 15:54 appclient
drwxrwxr-x@ 35 buddy  staff    1190 20 Dez 13:16 bin
drwxrwxr-x@  4 buddy  staff     136 20 Nov 15:54 bundles
drwxrwxr-x@  5 buddy  staff     170 20 Nov 15:54 docs
drwxrwxr-x@  6 buddy  staff     204 18 Jan 12:13 domain
-rw-rw-r--@  1 buddy  staff  267443 20 Nov 15:54 jboss-modules.jar
drwxrwxr-x@ 14 buddy  staff     476 20 Nov 15:54 modules
drwxrwxr-x@  8 buddy  staff     272 17 Jan 13:41 standalone
-rw-rw-r--@  1 buddy  staff      58 20 Nov 15:54 version.txt
drwxrwxr-x@ 10 buddy  staff     340 20 Dez 13:16 welcome-content

tools
-----
This Directory contains Apache Ant 1.8.4, as well as all need submodules (XmlTask, svnant, ant-contrib) These were needed
to implement every necessary use case within ant.
