The Project is one example to use (Specflow + Playwright) to create a BDD test framework

There are the below considerations during implementation:
1) Decouple the location definition from code to one configuration file (elementlocations.json)
2) Specify the test options in one configuration file (usersettings.json) which may easly change the browser type and credential parameters.
3) Implement one singleton class(UserConfiguration.cs) to read the user configuration file
4) Design homepage as one factory pattern which may create other page objects, so that the outside invokers may easily obtain the other page object.

The project has implememnted and verified 5 test scenarios beased on the Trolley feature (see trolley.feature in Features folder)




