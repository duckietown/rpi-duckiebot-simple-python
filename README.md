# Simple program to run via Docker

As explained [in the guide](http://docs.duckietown.org/DT18/opmanual_duckiebot/out/docker_setup.html), 
these commands need to be run from your laptop, but 
things will happen on the robot.


Set the environment variable to point to the Duckiebot:

    $ export DOCKER_HOST=tcp://X.X.X.X:2375
    
Run the following:

    $ docker build -t my-simple-python-program .
    
The docker daemon on the Duckiebot will build the container.

Then run the following:

    $ docker run -it --network=host my-simple-python-program
