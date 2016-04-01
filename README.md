# Docker images with FEniCS and Jupyter

Docker images based on dev-env-py3 with Jupyter notebook installed.
Build with:

    docker build -t fenics-jupyter dev-py3-jupyter

Run with:

    docker run -p 8888 -it fenics-jupyter
    
And connect to http://127.0.0.1:8888.

If you are using docker-machine (e.g. OS X), your notebook server is one extra network hop away:

    docker run --net host -it fenics-jupyter
  
  And connect directly to the docker-machine ip:
  
      http://$(docker-machine ip <name>):8888
  