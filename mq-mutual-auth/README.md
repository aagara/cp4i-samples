Exctracting the certificate and keys from a .pfx file
=====================================================
Ref: https://www.ibm.com/docs/en/arl/9.7?topic=certification-extracting-certificate-keys-from-pfx-file

Command to extract Private the Key
openssl pkcs12 -in [yourfile.pfx] -nocerts -out -nodes [filename.key]

Command to extract the Certificate
openssl pkcs12 -in [yourfile.pfx] -clcerts -nokeys -out [filename.crt]


Adding a CA certificate, or the public part of the self-signed certificate, into a key repository
=================================================================================================
Ref: https://www.ibm.com/docs/en/ibm-mq/9.0?topic=wsulw-adding-ca-certificate-public-part-self-signed-certificate-into-key-repository-unix-linux-windows

runmqckm -cert -add -db [filename.kdb] -pw [password] -label [label] -file [filename] -format ascii 

runmqakm -cert -add -type cms -stashed -db /var/run/runmqserver/tls/key.kdb -label [label] -file [filename] -format ascii


Creating a new Queue Manager on OpenShift
=========================================
https://www.ibm.com/docs/en/ibm-mq/9.2?topic=integration-creating-new-queue-manager-red-hat-openshift

Configuring a client using a configuration file
===============================================
https://www.ibm.com/docs/en/ibm-mq/9.2?topic=client-configuring-using-configuration-file

Verifying the TLS configuration of your queue manager with mqcertck
===================================================================
https://www.ibm.com/docs/en/ibm-mq/9.2?topic=mq-verifying-tls-configuration-your-queue-manager-mqcertck

Configuring TLS
===============
https://www.ibm.com/docs/en/ibm-mq/9.2?topic=manager-example-configuring-tls

Importing a personal certificate from a Microsoft.pfx file
==========================================================
https://www.ibm.com/docs/en/ibm-mq/9.2?topic=windows-importing-personal-certificate-from-microsoftpfx-file

Using Custom Volume in containers
=================================
https://community.ibm.com/community/user/integration/blogs/rob-convery1/2021/04/08/acecc-custom-volumes

App Connect Integration Server Reference
========================================
https://www.ibm.com/docs/en/app-connect/containers_cd?topic=resources-integration-server-reference#crvalues

How to copy files to/from a container
==============================================
To copy a file from the local file system to a container: 
kubectl cp [src-path] [your-pod-name]:[dest-path]
To copy a file from the container to the local file system:
kubectl cp [your-pod-name]:[src-path] [local-dest-path]

IBM MQ Troubleshooting Common TLS SSL Errors
=============================================
https://www.ibm.com/support/pages/ibm-mq-troubleshooting-common-tls-ssl-errors#9642

Debugging MQ Client connection problems
=======================================
https://colinpaice.blog/2021/02/08/debugging-mq-client-connection-problems/#certlabel
