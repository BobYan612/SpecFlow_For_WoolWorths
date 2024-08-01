**BDD Test for Woolworths**

The Project is one example to use (Specflow + Playwright) to create a BDD test framework

**Dependency**  
SpecFlow  
SpecFlow.Plus.LivingDocPlugin  
SpecFlow.NUnit  
Microsoft.Playwright  
Microsoft.Playwright.NUnit  
Microsoft.Extensions.Logging  
Microsoft.Extensions.Configuration 

>[!NOTE]  
>The executable binary such as chrome.exe will be installed automatically when installing Playwright, or we need to download the related version from playwright official webserver. 

**Features**  
There are the below considerations during implementation:
 - Decouple the location definition from code to one configuration file ([elementlocations.json](SpecFlow_For_WoolWorths/elementlocations.json))
 - Specify the test options in one configuration file ([usersettings.json](SpecFlow_For_WoolWorths/usersettings.json)) which may easly change the Chromium/Firefox/Webkit and credential parameters.
 - Implement one singleton class([UserConfiguration](SpecFlow_For_WoolWorths/Support/UserConfiguration.cs)) to read the user configuration file
 - Design homepage as one factory pattern which may create other page objects, so that the outside invokers may easily obtain the other page object.
 - Use ILogger to control the output of the test log

**Test**  
The project has implememnted and verified 5 test scenarios beased on the Trolley feature (see [trolley.feature](SpecFlow_For_WoolWorths/Features/trolley.feature) in Features folder)
 - Scenario1: __Choose a product from browse to trolley__
 - Scenario2: __Choose a product from speical & offers to trolley parameters.__
 - Scenario3: __Choose a product from low price to trolley__
 - Scenario4: __Update the quantity in trolley__
 - Scenario5: __Remove one item in the trolley__

> [!TIP]  
> Any suggestions or questions please contact biao.yan612@gmail.com



