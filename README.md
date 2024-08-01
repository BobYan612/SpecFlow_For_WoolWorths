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

**Features**  
There are the below considerations during implementation:
 - Decouple the location definition from code to one configuration file ([elementlocations.json](SpecFlow_For_WoolWorths/elementlocations.json))
 - Specify the test options in one configuration file ([usersettings.json](SpecFlow_For_WoolWorths/usersettings.json)) which may easly change the browser type and credential parameters.
 - Implement one singleton class([UserConfiguration](SpecFlow_For_WoolWorths/Support/UserConfiguration.cs)) to read the user configuration file
 - Design homepage as one factory pattern which may create other page objects, so that the outside invokers may easily obtain the other page object.
 - Use ILogger to control the output of the test log

**Test**  
The project has implememnted and verified 5 test scenarios beased on the Trolley feature (see trolley.feature in Features folder)
 - Scenario1: Choose a product from browse to trolley
 - Scenario2: Choose a product from speical & offers to trolley parameters.
 - Scenario3: Choose a product from low price to trolley
 - Scenario4: Update the quantity in trolley
 - Scenario5: Remove one item in the trolley




