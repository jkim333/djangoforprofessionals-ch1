# Key points from chapter 1 of [Django for Professionals](https://djangoforprofessionals.com/):

- Docker is a way to isolate an entire operating system via Linux containers which are a type of virtualisation.
- Through Docker, we can virtualise from the Linux layer up.
- Essentially, Docker allows us to implement Linux containers.
- Docker vs Virtual Machines:
  - Virtual Machines are like homes: stand-alone buildings with their own infrastructure
  - Docker containers are like apartments: they share common infrastructure, but come in various sizes that match the need of an owner.
- Containers vs Virtual Environments (e.g. virtualenv, venv, pipenv):
  - Virtual environments can only isolate Python packages. They still rely on global, system-level installation of Python on our computer. It does not contain Python itself.
  - Containers can also isolate non-Python packages, e.g. PostgreSQL database. Docker can isolate the entire operating system, not just the Python parts. Therefore, we can install Python within Docker and install and run a production-level database.
- General pattern when using Docker with Django:
  1. Create a virtual environment locally and install Django
  2. Create a new project
  3. Exit the virtual environment
  4. Write a Dockerfile and then build the initial image
  5. Write a docker-compose.yml file and run the container with docker-compose up
