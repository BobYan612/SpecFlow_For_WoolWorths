The Project is one example to use (Specflow + Playwright) to create a BDD test framework

There are the below desing considerations:
1) Decouple the location definition from code to one configuration file (elementlocations.json)
2) Specify the test options in one configuration file (usersettings.json) which may easly change the browser type and credential parameters.
3) Implement one singleton class(UserConfiguration.cs) to read the user configuration file
4) Design homepage as one factory pattern which may create other page objects, so that the outside invokers may easily obtain the other page object.

The project has implememnted and verified 4 test scenarios beased on the Trolley feature. The below is the example to define one scenario. 

@regression
Scenario: Remove one item in the trolley
	Given the user has login in 
	And Trolley item list is empty
	And add "Hellers Sausages Cheese & Bacon Precooked" to trolley under "" in "Specials & offers Page"
	And add "fresh fruit bananas yellow" to trolley under "Browse/Fruit & Veg/Fruit/Shop all Fruit" in "Browse Page"
	When click "remove" for "fresh fruit bananas yellow" in Trolley Page
	Then The total price and subtotal price have been shown correctly



