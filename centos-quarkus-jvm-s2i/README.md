# [Quarkus.io](http://quarkus.io) GraalVM Native S2I

## OpenShift

### Minishift 8 GB Set-Up recommendation

    minishift profile delete quarkus-s2i-native
    minishift profile set quarkus-s2i-native
    minishift config set memory 8192
    minishift start

### OpenShift Build

    oc new-build https://github.com/quarkusio/quarkus-images.git --context-dir=docker/centos-quarkus-jvm-s2i --name quarkus-jvm-s2i
    oc logs -f bc/quarkus-jvm-s2i
