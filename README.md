#[SubscriberSearch-net]
=================
![SubscriberSearch](http://code.exacttarget.com/sites/default/files/pictures/subscribersearch_small.png)
SubscriberSearch-net is an example application which illustrates how to create a Hub Exchange application utilizing [Single Sign-on (SSO)](http://code.exacttarget.com/devcenter/getting-started/hubexchange-apps/sso), [Fuel API Family](http://code.exacttarget.com/devcenter/fuel-api-family) (REST), [E-mail SOAP API](http://docs.code.exacttarget.com/020_Web_Service_Guide), and [Fuel UX](https://github.com/ExactTarget/fuelux) together in one application for [ExactTarget's Interactive Marketing Hub](http://www.exacttarget.com/interactive-marketing-hub.aspx) using .NET/C#. 

The full application allows the user to search their ExactTarget subscriber list and update the subscriber status of individual subscribers. 

#Tags
----------
This application was built in steps and they are [tagged](https://github.com/ExactTarget/SubscriberSearch-net/tags)  so that you can get the final application or just specific code.

Step1 - Created the basic app and implemented the JWT for display in Interactive Marketing Hub

Step2 - Added Fuel REST API request to platform service to store and display SOAP URL returned from call 

Step3 - Added Fuel UX for the user interface styling 

Step4 - Added Search functionality to datagrid using SOAP call through handler

Step5 - Coming Soon! Will add update subscriber functionality and SOAP call  

#Requirements
----------
* Access to App Center on http://code.exacttarget.com
* .NET Framework 3.5 or higher
* Web Server that can host .NET Web Sites

#Notes
----------
* Built with .NET Framework 3.5 in Microsoft Visual Web Developer 2010 Express

#Quick start
-----------

1. Clone the repo onto your server and deploy to internet facing location.
2. Open the project or solution in .NET Studio and save. The project is setup to run debug mode at port 54847 in the project properties->web.
3. Create a new Hub Exchange application in [App Center](http://code.exacttarget.com/appcenter) (requires login) naming it what you want. 
4. If testing locally, for the Login URL, put the path to http://localhost:54847/Login.aspx.  For the Home URL, put the path to http://localhost:54847/Default.aspx.  For the Logout URL, put the path to http://localhost:54847/Logout.aspx. If hosting non locally enter the proper paths.
5. Open web.config file and update the [applicationSecret] attribute value with the Application Signature that was made available in App Center after creating a Hub Exchange application. 
6. If not testing locally, set up IIS/Web Server to properly host .NET web application. IIS Application pool will be .NET v2.0.
7. Test the web application. Make sure the web app is running. Since the IMH is not passing the JWT that the application requires you should get a page that simply states "Error Occurred: Object reference not set to an instance of an object." That will let you know the web server is serving the page correctly.
8. Go to [ExactTarget IMH](https://imh.exacttarget.com) and login to your ExactTarget account. Your application created in App Center should be in the IMH menu. Select it and accept any mixed security warnings if you receive them.

For more information about setting up an application in App Center, please see [App Center Overview](http://code.exacttarget.com/devcenter/getting-started/app-center-overview) and [Registering App](http://code.exacttarget.com/devcenter/devcenter/getting-started/app-center-overview/registering-app).

#Authors
-----------
Jason Meketa

* http://github.com/jmeketa

#Copyright and license
-----------

Copyright (c) 2012 ExactTarget

Licensed under the MIT License (the "License"); you may not use this work except in compliance with the License. You may obtain a copy of the License in the COPYING file.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.