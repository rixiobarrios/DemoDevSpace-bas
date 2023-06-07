# DMC UX UI5 BAS UC

[Video tutorial[no sound] (2022)](https://video.sap.com/media/t/1_w70n5iet)

[Blog tutorial by Kevin Hunter (2022)](https://blogs.sap.com/2022/04/11/building-a-custom-digital-manufacturing-cloud-pod-plugin-the-easy-way/)

[SAP repository on github](https://github.com/SAP-samples/digital-manufacturing-extension-samples/blob/main/dm-podplugin-extensions/ExecutionPodPluginTemplate_and_Example/documentation/InstallationAndConfigurationGuide.pdf)

[Help Portal](https://help.sap.com/docs/sap-digital-manufacturing/pod-plugin-developer-s-guide/creating-and-deploying-custom-pod-plugins?q=dmc%20host%20name)

## UX Use-Case-01: View Plug-in – Display Text (1W)
As a system, I want a custom view plugin that displays the text “Hello World” so that the world knows I am here.

- Step 1 - Go to Business Application Studio (BAS)

[Your Business Application Studio environment](https://dmc-az-cons-training.eu20cf.applicationstudio.cloud.sap/index.html)

- Step 2 - Enter a new Dev Space
e.g MyPodPlugin

- Step 3 - Select application kind
Full Stack Cloud Application

- Step 4 - click the Create Dev space button

- Step 5 - Click on the newly created Dev Space

- Step 6 - Open a new terminal window

- Step 7 - Open project folder
cd projects

- Step 8 - Make new project's folder
e.g. mkdir mypodplugin

- Step 9 - Open new folder
cd mypodplugin

- Step 10 - Install generator plugin
npm install generator-dmcpodplugin

- Step 11 - Generate new project
yo dmcpodplugin

- Step 12 - Enter the name of your plugin
e.g. mypodplugin

- Step 13 - Enter version number
e.g. 0.0.1

- Step 14 - What is your DMC host name?
e.g. dmc-az-cons-training.test.execution.eu20.dmc.cloud.sap

- Step 15 - What is your plugin namespace?
e.g. sap.custom.plugins

- Step 16 - Support WORK_CENTER PODS?
Yes

- Step 17 - Support OPERATIONS PODS?
Yes

- Step 18 - Support ORDER PODS?
Yes

- Step 19 - Support CUSTOM PODS?
Yes

- Step 20 Support Line Monitor PODS?
Yes

- Step 21 - Allow Multiple Instances?
No

- Step 22 - Production Process Enabled?
Yes

- Step 23 - Open working folder 
e.g. user/projects/mypodplugin

(Optional) Step 24 - Open file builder.properties
e.g. user/projects/mypodplugin/webapp/mypodplugin/i18n/builder.properties

(Optional) Step 25 - Change line 6 from title=mypodplugin to Ourmypodplugin

- Step 26 - Right click on file MainView.view.xml
e.g. user/projects/mypodplugin/webapp/mypodplugin/view/MainView.view.xml

- Step 27 - Open file with Layout Editor

- Step 28 - Delete tollbar

- Step 29 - Edit text from template to This is some text and close

- Step 30 - Right click on file mta.yaml
e.g. user/projects/mypodplugin/mta.yaml

- Step 31 - Select Build MTA Project from popup menu

- Step 32 - Press any key to close process after finished

- Step 33 - Right click on file generated by Build MTA Project
e.g. user/projects/mypodplugin/mta_archives/mypodplugin_0.0.1,mta_archives

- Step 34 - Select Deploy MTA Archive from popup menu

- Step 35 - On Cloud Foundry Sign In and Targets enter your endpoint
e.g. user/projects/mypodplugin/mta.yaml

- Step 36 - On Cloud Foundry Sign In and Targets enter your credentials
e.g. user@sap.com amd password

- Step 37 - On Cloud Foundry target select desired oragnization
e.g. Digital Manufacturing Cloud Internal tenants_DMC-AZ-CONS-training

- Step 38 - On Cloud Foundry target select desired space and click apply
e.g. DMC_DEV

- Step 39 - Grab generated link
e.g. Application "mypodplugin" started and available at "digital-manufacturing-cloud-internal-tenants-dmc-az-***********.******.eu20.hana.ondemand.com"

- Step 40 - Press any key to close process after finished

- Step 41 - Add to servide registry app in DMC (Digital Manufacturing Cloud)

[Your Digital Manufacturing Cluod Tenant](https://dmc-az-cons-training.test.execution.eu20.dmc.cloud.sap/cp.portal/site?sap-language=en#Shell-home)

- Step 42 - Go onto Manage Service Registry

- Step 43 - Select UI Extensions

- Step 44 - Click on Create

- Step 45 - On New UI Extension screen enter the following

- Step 46 - Enter Name
e.g. MyPodPlugin

- Step 47 - Enter Description
e.g. My POD plugin

- Step 48 - Select Type POD plugin

- Step 49 - Enter generated link from deployment into URL adding https:// or http://

- Step 50 - Enter name space previously set at project generator with forward slashes instead of dots
e.g. sap.custom.plugin.mypodplugin to sap/custom/plugin/mypodplugin

- Step 51 - Enter PATH as the project's folder
e.g. /mypodplugin

- Step 52 - Check the Enable Status box and click Create

- Step 53 - Custom plugin is enabled and vaialable in the DMC and can be used in a POD (Production Operation Dashboard)

- Step 54 - Select DEFAULT_ORDER_POD

- Step 55 - Select Details

- Step 56 - Search for our newly created plugin
e.g. mypodplugin

NEWLY REGISTERED PLUGIN NOT FOUND
