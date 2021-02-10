# OracleFunctions-getStarted
Learn how to work with Oracle Functions

In this tutorial, you use an Oracle Cloud Infrastructure account to set up Oracle Functions development using Cloud Shell. Then, we create a function application and a function. Key tasks include how to:

Set up an authentication token.
Gather required information.
Set up a VCN.
Log in to OCI Registry (OCIR).
Configure Cloud Shell to deploy functions.
Configure your Fn context.
Create an app for your Oracle function.
Create a function.
Deploy your function.
Test your function.

![image](https://user-images.githubusercontent.com/42166489/107510643-4cbdb900-6bca-11eb-9c4c-4e6c2f2d89c3.png)


For additional information, please see:

Start for Free : https://www.oracle.com/cloud/free/
Launch your first Linux VM: https://docs.oracle.com/iaas/Content/GSG/Reference/overviewworkflow.htm
Cloud Shell: https://docs.oracle.com/iaas/Content/API/Concepts/cloudshellintro.htm
Oracle Functions: https://docs.oracle.com/iaas/Content/Functions/Concepts/functionsoverview.htm
OCI Registry: https://docs.oracle.com/iaas/Content/Registry/Concepts/registryoverview.htm

Before You Begin

To successfully perform this tutorial, we must have the following:

A paid Oracle Cloud Infrastructure account. See Signing Up for Oracle Cloud Infrastructure.
Link- https://docs.oracle.com/iaas/Content/GSG/Tasks/signingup.htm
Your OCI account configured to support Oracle Functions development. See Create Policy for Oracle Functions.
https://www.oracle.com/webfolder/technetwork/tutorials/infographics/oci_functions_cloudshell_quickview/functions_quickview_top/functions_quickview/index.html#
OCI Cloud Shell which is included with your account and includes:

OCI CLI
Docker
Python 3.6+
Java 1.8+
Node.js 10+

1.Gather Required Information

Collect all the information needed to complete the tutorial.

Gather Region and Registry Information
Prepare the information we need from the Oracle Cloud Infrastructure Console.

Find your region identifier and region key from Regions and Availability Domains.
Example: us-ashburn-1 and iad for Ashburn.
https://docs.oracle.com/iaas/Content/General/Concepts/regions.htm

Create a registry project name to store our function images in OCI Registry (OCIR).
When we publish a function, a Docker image is created in OCIR. Your OCIR project name is prepended to our function images to make them easy to find. For example, given:

Registry project name: my-func-prj
Function name: node-func
Your function image would be stored on OCIR under: my-func-prj/node-func

Get Compartment, Auth Token, and Collect your Data

Create or Select a Compartment
https://docs.oracle.com/iaas/Content/Identity/Tasks/managingcompartments.htm#To

To create a compartment see Create a compartment. After our compartment is created, save the compartment OCID.

To get the compartment OCID from an existing compartment:

Go to Identity then Compartments.
Select your compartment.
Click the Copy link for the OCID field.

![image](https://user-images.githubusercontent.com/42166489/107511003-e71dfc80-6bca-11eb-9384-3f2851c03de3.png)

