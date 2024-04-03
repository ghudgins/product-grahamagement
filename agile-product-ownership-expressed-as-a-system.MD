
# Agile and balanced team dynamics expressed as a system

Balanced team is a consulting-y buzzword coined by a previous employer. I like to think of balanced team as treating everyone on the team, no matter the title, as a pool of generalized workers. These team members usually have a speciality/mastery but operating as a unit. Balanced team is to say that every team member can perform every other function at some level. This is valuable because it helps you decrease the cost of inner-team communication. This allows you to increase your empathy and understanding while being more understanding on how to encode information for another worker doing another job. while also allowing the team to flex and apply  people to bottlenecks. This is an opinion: but having a solid understanding on how other specialities function makes for a more rewarding experience as a software professional. 

To drill into this idea and to keep an analogy on the way, let’s imagine our team as an actual software system complete with backend systems, APIs, and anything else we need. 

It actually shouldn’t be too hard these days given how many jobs have been automated (and of course we are not safe from this as well but that’s a [topic for another day](https://www.youtube.com/watch?v=7Pq-S557XQU))

Back to the team—a team as a system with inputs and outputs, functions, jobs, etc. The system exists to perform one job that no other system does...products or code in a repository. While teams do a lot of activities the purpose of the other activities are to support the primary one. This isn’t to say that secondary actions aren’t important but for the sake of simplicity let’s just think about the team as producing, at the end of a process, features that customers will use in some technology platform. 

![team ships code](https://github.com/ghudgins/product-grahamagement/blob/main/resources/team-ships-code.png?raw=true)

If the output of our team is code in a repository then what are the inputs to this work? Let’s look at this. A team functions by fielding requests. Some requests are good/constructive. Sound requests are bad experiences like a broken or confusing feature...some requests come from your terminal as a developer. At a very high level there are two types of requests I choose to use for today’s discussion - requests fielded manually and requests fielded automatically.

![fields request](https://github.com/ghudgins/product-grahamagement/blob/main/resources/fields-request.png?raw=true)

Fielding a request is the first example of of job - If we are software then we have conditions that weigh “is this something that can be fixed with code change”. We also have a process to separate the issues that need immediate attention vs. would-be requests into future planned work. This process is an manual event driven listener. 

Here are some examples of manual listeners

* inputs on existing functionality  _support, emails, helping colleagues out, a periodic usage analysis in google/adobe shows problems_
* inputs from business and market-making/integrating strategy _we need to do this because customers want it_
* inputs based on customer acquisition strategy _i need this to buy your product_
* things identified by the team that you should be doing _in building “A” I see we also need “B”_

There’s also a listener that’s built into the code repository. This one is more in your face because when it goes of you have to do something and there is no job management part of it at all. This is the “front line”. I call these auto listeners because they almost always do what you want them to (except when they don’t which is a topic for another presenter). Here are example auto listeners: 

* tests run by a CI system 
* pager duty on infrastructure

When a request comes in it gets processed by a listener. The listener might correct the issue immediately or it might creates a job in the queue attached to the right team. 

![listening and queue](https://github.com/ghudgins/product-grahamagement/blob/main/resources/listening-and-queue.png?raw=true)

Most work is run out of a queue....especially the work that requires multiple changes and the tracking of multiple scenarios. Each team has a queue which is groomed and kept current by a job manager. This is our second job. The job manager can also reports the order of the jobs and the status at any time. That is how work enters the queue: A listener of some variety creates a job and the job manager might adjust its position in the queue. 

![job manager](https://github.com/ghudgins/product-grahamagement/blob/main/resources/jobmanager.png?raw=true)

For our next two jobs we have doing work—design, development, product, or otherwise. When a worker comes free, that worker might do any of the jobs mentioned or two new types of jobs--Planned work from the jobs queue or unplanned work (sometimes also from the job queue that was added moments ago). Most workers plan on time to do both types of work no matter what the function. 

For planned work, the worker executes the highest priority overall job and works on the next promise in the chain for that job. Work is usually self-assigned or assigned to them through the job manager. Usually this will match with the worker’s skillset. If the worker is doing unplanned work that isn't in the queue the worker will usually register this with the job manager. Planned (and ideally unplanned) development work usually results in additional auto listeners to help defend against regression in a system with growing complexity. 

Unplanned work usually comes up due to priority or a built-in function of continually improving areas of the product impacted by a change. This is the saying in development _leave the room in a better shape than you found it._ Here are some exmaples:

* a manual listener throws you a bug or feature mistake, clear enhancements for existing features that are inexpensive to implement
* re-factor and upgrade 3 -> 1 services doing the same thing; ui consistency pattern update; dependency upgrade;  
* workers will periodically produce things without the job system 20% time, side projects, other jobs, prototypes

![planned and unplanned work](https://github.com/ghudgins/product-grahamagement/blob/main/resources/planned-unplanned-work.png?raw=true)

Periodically (every 1-2 weeks) the job manager interfaces with a team focused on determining priority (which is our last type of job on the list). This service results in an updated job priority list and can also create new jobs. This also serves to rebalance work across the teams for complex delivery requiring multiple teams. Every 3 months the same team decides on more significant strategy feature sets.

![business](https://github.com/ghudgins/product-grahamagement/blob/main/resources/business.png?raw=true)

Having walked through how a team gets work, how it works on things, and how priorities are set we now have our list of jobs. 

Generalized workers can be...

* Manual listener outputting jobs
* Job manager communicating updates
* Job manager calculating minor priority
* Job manager requesting information
* Unplanned work 20% time outputting jobs or periodic features
* Unplanned work outputting critical fixes
* Unplanned work outputting improvement/refactor
* Planned work - Design outputting more detailed jobs
* Planned work - Sequencing outputting smaller jobs
* Planned work - Development outputting features
* business interfacing customers
* business calculating major priority

If you are on a team, think about how much time you spend on each of these jobs. 

Here is an example for me

![my example breakdown](https://github.com/ghudgins/product-grahamagement/blob/master/resources/example-graham-json.png?raw=true)



Are there some areas you have never tried? Why even mess with the ratios? Sometimes the various aspects of planned work can create silos and loss of understanding. The more balanced each team member is the less likely this is to happen. The better we understand how each other work the more likely we can achieve clarity. 

However, you shouldn’t just optimize just to optimize. you should optimize to improve the team. To make any improvement you need a measure (google calls these Observable Key Results which is more consulting "stuff").

We use points to measure the team’s output against itself. Points should be a measure of relative complexity against prior work and nothing else. I.e. this feature is twice as complex as the feature last week. Points should never be units of time (people measure time differently) and complexity is a better tool than “time” because a simple story that’s a known amount of tedious work will most of the time still get done faster than a complex smaller-feeling thing with unknowns. If you weigh velocity for the pool of workers available in a time period you can come to a few hypothesis. 

* Systems with **decreasing** PTO-weighted velocity are under investing in auto listeners and are getting drowned in system complexity. Refactor may be needed
* Systems with **increasing** PTO-weighted velocity are usually still on the upward swing of either the product, the team performance curve, or both. Check out the [Tuckman's stages of group development](https://en.wikipedia.org/wiki/Tuckman%27s_stages_of_group_development)
* Systems with **flat** PTO-weighted velocity are rock stars. The more consistent the team runs usually points to an appropriate investment in tests, good work size, and appropriate time spent de-risking. 
* Systems with **volatile/high st.deviation** PTO-weighted velocity might have a seasonal culture or is following an unspoken waterfall of features first then clean up. This can be rough on your system in waves. From my perspective, this is the team I'm currently on.

The team should optimize for the flat velocity after a product/team ramp up. Use retro to adjust how the team is working to improve. There are so many levers
* Involve people sooner
* More spikes
* Smaller stories
* Build empathy & teamworking 
* Improved global definition of done 
* etc….

If stories are frequently running unexpectedly long there’s a good chance there is not enough planning or too much technical risk. 

A big factor of making these changes is understanding how your machine is running. If something is amiss you can usually tell. Having a balanced team approach means everyone is helping the various functions be successful because we all can empathize with what it’s like to do those jobs. Spend less time trying to coordinate across the functions and have empathy when working across each team. 


Did I miss something? Yes, definitely. Nothing in humanity can be that easily bucketed. And that’s a great reason why being a balanced team is so important. While we are specialized in why we were hired and we may find we become more effective in our hired job if we learn about the other jobs.

There are a few calls to action i’d encourage you to do.

Calls to action:
* what is your breakdown
* how much do you understand the other sub systems
* are you optimizing for the key output of your entire unit

Thanks for reading

![final](https://github.com/ghudgins/product-grahamagement/blob/master/resources/final.png?raw=true)
