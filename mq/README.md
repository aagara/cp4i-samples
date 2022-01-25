Sample app for binding REST API to MQ
=====================================

https://community.ibm.com/community/user/integration/viewdocument/app-connect-openshift-operator-depl-1?CommunityKey=ab1f8001-8ec9-4c40-84cb-396723d816a1&tab=librarydocuments

Sample MQ Policy XML
====================
<?xml version="1.0" encoding="UTF-8"?>
<policies>
  <policy policyType="MQEndpoint" policyName="mq" policyTemplate="MQEndpoint">
    <connection>CLIENT</connection>
    <destinationQueueManagerName>mtlsqm</destinationQueueManagerName>
    <queueManagerHostname>mtlsqm-ibm-mq</queueManagerHostname>
    <listenerPortNumber>1414</listenerPortNumber>
    <channelName>ACE_SVRCONN</channelName>
    <securityIdentity></securityIdentity>
    <useSSL>true</useSSL>
    <SSLPeerName></SSLPeerName>
    <SSLCipherSpec>ECDHE_RSA_AES_128_CBC_SHA256</SSLCipherSpec>
  </policy>
</policies>

