# simple_bar_deployment

Simple bar deployment requires a bar file available in a repository such as Nexus.

Use the BarAuth type to create configurations that contain credentials for connecting to an external repository system that stores one or more BAR files that you want to deploy to an integration server. This configuration is useful if you have set up continuous integration and continuous delivery (CI/CD) pipelines to automate and manage your DevOps processes, and would like to directly reference BAR files in your repository management system for deployment.

https://www.ibm.com/docs/en/app-connect/containers_cd?topic=servers-barauth-type

Create a nexus repository if required by logging in with type "hosted" and format "raw"

If Nexus repository (or any) requires credentials then "Configuration" custom resources needs to be created with barAuth type.


{"authType":"BASIC_AUTH","credentials":{"username":"admin","password":"admin123"}}

If OpenShift web console is used to created the Configuration then it needs to be base64 encoded. Use -w 0 to disable line wrapping in the output

$ echo '{"authType":"BASIC_AUTH","credentials":{"username":"admin","password":"admin123"}}' | base64 -w 0

Apply the bar file either from Web console or using CLI by replacing the yaml with any desired value. 