Briefly explain your technical choices. Your final visualization may differ significantly from you original sketch or only implement a subset of it, but ensure you document the tradeoffs you faced and the reasoning behind your choices.

* I intended to use node-link initially but then given that it a a centralized design format I designed to switch to try other techniques. 
* I inplemented the hierarchical bundling but ran out of time to do a full implementation. 

* Challenges: 
The examples showed how you can do given ONE root. But I considered our scenario to have more than 1 root so other options I though of ewre: a
Aggregate By File level Changes with a drop down for date range and drop down for Branch Name. Because when you branch off and want to merge back 
you want to know what happened to that specific branch. 


I tried implementing Zoom as I wanted to allow users to zoom or specify date range in the drop down. You can see my attemp in the simple_graph.html. 
