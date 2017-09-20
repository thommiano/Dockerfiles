# Pull pytorch docker image
FROM digitalgenius/pytorch:latest

# Install nano
RUN apt-get update -y
RUN apt-get install nano

# Install jupyter
RUN pip install jupyter

# Make a working directory
RUN mkdir projects

# Create bash script for launching jupyter notebook
RUN echo "jupyter notebook --ip 0.0.0.0 --no-browser --allow-root">/projects/launch_jupyter.sh


