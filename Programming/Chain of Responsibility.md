#OOP #Pattern


* GUI classes that raise a stream of requests (e.g. MOUSE_CLICKED events)
* multiple number of  handler or process events
* efficient processing of requests without hard-wiring handler relationships, precedence, or request-to-handler mappings

chaining mechanism uses recursive composition to allow an unlimited number of handlers to be linked

![[Pasted image 20231213193154.png]]


**receiver** objects are added to a chain 


notation: 
	->  direction
	 | group


**sender** objects have a reference to the first receiver object in the chain. 

objects are linked via linked list

request is passed along the chain  until a **handler** or **receiver** handles it, when request is handled, **it is not passed on any longer** 

default object used if no other handles handle the request.


-----------------------------------------------

Client -> 
	Process element | Process element 

* Consider you are developing a system that approves purchasing requests for an organization. approval authority in the organization depends on the dollar amount of the purchase.
* whenever employees spend company money, they need to get approval from boss or boss of boss
* approval authority can change at any time and the system should be flexible enough to handle this situation. 

Handlers: 
* can be interface (or abstract class) for handling requests.


Consequences
* Multiple handlers may be able to handle a request.  
* The sender doesn't know how many handlers are in the chain.  
* The sender has no control over the handlers.  
* Only one handler in the chain should handle the request.  
* Some requests may not be handled at all.  
* Changing the list of handlers doesn't affect the sender.*