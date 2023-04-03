To add extension to the protocol, we should ensure that each extension does not rely on any others to behave correctly. 

If we consider the provided additional extension: 
* Send to any individual on the whole UW campus
* Specify whether contents are ASCII text, Unicode text, or binary values
* Keep a record of what nodes the card has passed through.

There is clear indication that each extension can exist by themselves without having the need of helpful from other extension. 
This way we reduced coupling in extension and further allow modification without impacting the rest of the system.

Furthermore, each extension should not try to perform an action that is already done by a different protocol. 
This mean we should implement a blackbox system, if one extension required to perform an action that another extension have control over, it should give control to 
the extension that has the correct authority over that action. This allow properties of our protocol to be consistent as each protities is correctly handled 
by its own extension/manager. 

For the provided additional extension, we can treat each extension as a different part of the card to markup. 
This could mean marking the address of the invidual on the top-right corner in the back of the card, specifying the content on the top-left corner in the back of the card,
and keeping a list of nodes the card has passed through as a comma separated list on the bottom of the card. 
By marking different spots from where other functionalities exist on the card, we keep each extension separated from each other. 
