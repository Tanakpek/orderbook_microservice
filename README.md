# orderbook_microservice!

We are trying to start and stop jobs according to the relevant instructions coming from postgres. We can invoke a shell script each to deploy a container and return a process process id every time a new stream begins and persist that spread id - process id association to delete it when it is no longer active. only issue here is that processes might be restarted or interrupted, in which case we the stream will not be emitting even though there apprears to be an active process id in our map. likewise we cannot find the correct pid to stop the streaming if the container dies.

![Untitled Diagram](https://user-images.githubusercontent.com/61313108/229544686-5b85a63c-abf9-462f-b89e-c7e6923f547b.jpg?raw=true)



