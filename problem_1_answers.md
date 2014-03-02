# Calendar:

### Who is the audience? (e.g. project manager, contributor, project user, visitor, etc.)
- This calendar view is basically showing a users contribution which is helpful to see how active each person has been with github repo. 
 I dont see a project manager needing this. But may be the persons manager can use it for performance monitoring. Contributors and Visitors and other users can understand this persons activeness.
It good for potential employers and its really a profile page/screen of the users coding to the outside world. Helps identify the main contributors.  

### What data have been used? 
- Yes. You can get the commits using the URL: 
- https://github.com/users/alexsb/contributions_calendar_data
1. Get the created_at from pull requests per date per user: /repos/:owner/:repo/pulls
2. Get the issues opened per date per user: /repos/:owner/:repo/issues
3. Get commits per date for all dates: /repos/:owner/:repo/commits

### What happens if suddenly a contributor pushes many commits in a short time interval? 
- If a lot of commits are made then the scale for the light green to dark green scale differently as the classification of less and more changes. A lot of the graph will have light green potentially compare to previous as the definition of “more" changes.

# Contributors:
- Who is the audience? (e.g. project manager, contributor, project user, visitor, etc.)
- This is good for other contributors, managers, visitors, users of the code/library. It gives an idea of how many changes have happened to the codebase adn who made the most changes as this helps to identify the key contributor for any questions. It also shows how much the code has changed which is good for users to know in terms of whether or not there were any recent massive updates to the codebase. 

- API 
https://github.com/mbostock/d3/graphs/contributors
In the contributors tab, there is contributor, # adidtions, # deletions overall and by user for a given range. 
This information can be retrieved from each commits api call for a specific repository. The users shown can be mapped to the committers.
	1. Get list of contributors for the repository, list of committers and list of pushes for the given date: /repos/:owner/:repo/events
	2. Get the additions and deletions: /repos/:owner/:repo/commits
	3. Get commit specific info also using: /repos/:owner/:repo/commits/:sha
	
# What happens if suddenly a contributor pushes many commits in a short time interval? 
- If too many commits are made the graph showing the number of commits will spike of a higher number and then reordering of the users who contributed will change. 

### Commit Activity:

- Who is the audience? 
- The audience would be contributors and project managers. 

# What data have been used? 
The data in this graph is the most simplest. It is the basic information aggregated on how many commits per day. 
The /repos/:owner/:repo/commits provides the date and all the commits info. 

# What happens if suddenly a contributor pushes many commits in a short time interval? 
 - The y axis would change significantly week over week so it can get confusing to users who may not notice that. 

### Code Frequency:
# Who is the audience? 
* Users, Contributors, PM;s.

# What data have been used? 
* It shows the additions/ deletions which can be gotten from /repos/:owner/:repo/commits

# What happens if suddenly a contributor pushes many commits in a short time interval? 
There will be more area under the graph or the y axis would have to change significantly. 

###Punchcard: 
# Who is the audience? 
PM’s or leads to see how much work is getting done.

# What data have been used? 
/repos/:owner/:repo/commits A simple count of the commits by date and parsing the day. 

# What happens if suddenly a contributor pushes many commits in a short time interval? 
The radius of the circles would have to change and that will distort the notion from a previous snapshot. 

###Pulse: 
# Who is the audience? 
This is full fledged dashboard for a repo. Its good for contributors and project managers. 

# What data have been used? 
1. You can see the pulls : /repos/:owner/:repo/pulls. Created date can be used to determine if it is future proposal or past. 
2. You can see the issues using: /repos/:owner/:repo/issues.
3. The /repos/:owner/:repo/commits provides the date and all the commits info, additions, deletions. You can also query by :sha. 
4. The status of the commits and its comments with date of commit can be retrieved from: /repos/:owner/:repo/comments

# What happens if suddenly a contributor pushes many commits in a short time interval? 
If there is many pushes since this is more like a dashboards the numbers will update but I don’t see a huge impact. 

### Questions

# Looking at the network graph, answer the same questions as above, plus:

# What is the role of interaction for this visualization? Would a static graph have been sufficient?

No static won’t do as when there is a commit or a merge it needs to be reflected immediately so they can accept the change before submitting. 

# What happens if many new developers suddenly join the project and push commits for the first time? How would you to preserve the graph's readability in such a situation?
The y axis would get multiple entries and expand massively. The graph too will have a string of commits along the y axis which would be hard
to follow if they were really close together. If that happens it would be better to show an aggregate with a drill down option based on 
its significance. 
