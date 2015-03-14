====Project: E-Commerce Site==== 

Technology: Nopcommerce CMS 

Developer: Praveen Yadav 

Creation Date: 14-Mar-2015 

Website Url: http://www. mastersoftwaretechnologies.com:701 

 

====Nopcommerce Setup ====

 

1) Download Source Code from git hub 

https://github.com/mss-parveensachdeva/nopcommerce 

2) open  solution file in visual studio 

3) Clean code 

4) Rebuild code 

5) Debug 

 

you will see database setup screen. Enter all details as displayed on your browser and proceed. In last, Database will be created. ,now add /Admin to url and you will get Login screen. Enter your Admin Email and password to customized your Website. 

 

====Install Plugin ====

go to:  Configuration > Plugins > Local Plugins  

 

you will get list of plugins , some of them are installed and some  are not. you need to install and enable that plugin for use in website. 

 

====Install PayPal Plugin ====

PayPal Setup: 

    Log into your PayPal account; under the “My Account” tab, select “Profile”>”My Selling Tools”. 

    Under the section “My business setup”, you’ll see “Website preferences” – click “Update” on this line 

    Turn “Auto-return” to “On”, and enter “http://{YourStoreURL}/PaypalPDTHandler.aspx” for “Return URL” 

    Turn “Payment Data Transfer” to “On” 

    All entries below this are optional, based upon your business requirements. 

    Click “Save” 

 

 

log into your nopCommerce instance as an administrator, and navigate to the Administration area. Click on “Configuration”>”Payment Methods”: click on the “Configure” link next to the entry for “PayPal Standard”. 

    Uncheck the box “Use Sandbox” 

    Enter your PayPal account e-mail address for “Business E-Mail” 

    Next you’ll enter your “Identity Token” you’ll obtain from your PayPal account into the field “PDT Identity Token” 

    Leave “DT. Validate order total:” checked 

    If you wish to charge an additional surcharge for PayPal transactions, add your surcharge to "Additional fee" 

 

    Enable IPN (Instant Payment Notification) 

    For “IPN Handler”, enter “http://{YourStoreURL}/Plugins/PaymentPayPalStandard/IPNHandler” 

    Click “Save 

 

====IIS Setup ====

IIS setup for Nopcommerce is similar to other .NET Application. 

You can check following steps. 
 
1) Open IIS  
 
2) Right Click on Sites -> Add Web Site 
 
3) Add Appropriate name in Site NAME 
  -> In Physical path set path upto Nop.Web Folder 
     
    If you are using full source code version then set 
    ..\Presentation\Nop.Web 
 
    Or if you are using published version 
    ..\Published\Web 
     
4) Go to Application Pools 
  -> Select Application pool for current site 
  -> Double click on it and set .Net Framework Version with Frame work 4.0 