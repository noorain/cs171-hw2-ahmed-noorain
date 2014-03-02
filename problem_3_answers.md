### Questions

Given your previous design critiques, your experience with the previous graph visualization implementation and the reading of the article cited below (Lee et al., 2006), answer the following questions:

1. Which graph-related tasks does an ideal GitHub Network Graph need to  address?

This graph addresses the browser related tasks as it shows the history of commits and allows one to browse through the interested overview. 

2. Get back to the GitHub network visualization you implemented and test it with the following projects on GitHub: [D3](https://api.github.com/repos/mbostock/d3/commits?per_page=100), [jQuery](https://api.github.com/repos/jquery/jquery/commits?per_page=100) and [Bootstrap](https://api.github.com/repos/twbs/bootstrap/commits?per_page=100). There's a lot more data, but the interaction patterns of users are also very different. What do you notice about the three repositories?

* For the twitter Bootstrap, looks like there are many contributors but yet a few who have commmitted the most. Since there are users branching off
and remerging the lines/path are much longer. 

* Jquery had the most number of commits. Not too many contributors but the most number of commits. The graph did scale. I tried changing the delay from 500 to 5000 inorder for the load to look more sketchy on load. 

3. How does this impact your graph?

The data is a lot more so it had some performance issues. More activities so lots more links. 

* I didnt have to change the width and height as it was using scale to graph even ehwne the number of commits or committers changed significantly. 

4. How would you improve your visualization to address issues with the larger and more complex data?

* I would like a feature of selecting a region for the user to focus on. As an overview is not really helpful and needed. Users would most likely be interested in learning about a specific branch so allowing then to choose which they want to consider as the main viewing branch would be helpful. More information on lines changes, files changes would be helpful in the tooltip. Easy scrolling feature or date range input. 

