# VM Nexus

VM Nexus is a full-stack application designed for seamless management of virtual machines (VMs), utilizing Docker, Django, and ReactJS to provide a reliable and efficient experience for both backend and frontend operations.

## Project Overview

VM Nexus simplifies virtual machine management by enabling CRUD operations on VM models through a user-friendly API and dynamic frontend interface. Designed with Docker for streamlined deployment, the application facilitates concurrent execution of Django and Webpack processes, enhancing development and production workflows.

## Technologies Used
 
- **Docker** - Containerizes the application and manages dependencies for consistent deployment.
- **Django** - Provides the backend framework and RESTful API for handling VM data.
- **ReactJS** - Powers the frontend with dynamic UI to display and manage VM data.
- **Webpack** - Bundles frontend resources, integrated to run concurrently with the backend.
 
## Features

- **Dockerized Development Environment**: Launches the Django backend and Webpack with a single command, improving setup efficiency.
- **VM Management API**: RESTful API to perform CRUD operations on VM models, built with Django REST Framework.
- **Dynamic Frontend**: Displays a table view of all VMs on `localhost:8000`, allowing quick interaction with VM data.
- **SSH Key Integration**: Added `ssh_key` field to enhance secure VM connections, with database migration enabled for future expansion.

## Setup & Installation

### Clone the Repository

```bash
git clone https://github.com/ankush7kumar/vm-nexus.git
cd vm-nexus
```

### Docker Setup

Ensure Docker is installed and running.

Run the application with Docker Compose:

```bash
docker-compose up --build
```

### Frontend Access

Access the ReactJS frontend at http://localhost:8000 to view and manage VMs.

## API Documentation

The VM Nexus API provides CRUD functionality for VM resources:
ss
- **GET /api/vms/**: Retrieve all VM instances.
- **POST /api/vms/**: Create a new VM instance.
- **PUT /api/vms/<id>/**: Update an existing VM instance.
- **DELETE /api/vms/<id>/**: Delete a VM instance.

## Assumptions and Design Decisions

- **Docker Integration**: Combined Webpack and Django server into a single docker-compose setup for streamlined development.
- **SSH Key for Security**: Added `ssh_key` field to support future needs for secure VM connections.
- **Frontend and API Coordination**: Built with scalability in mind, enabling VM Nexus to accommodate additional fields and views as needed.

## Future Enhancements

- **Enhanced Security**: Add OAuth for secured API access.
- **Advanced Filters**: Include filtering options for VM properties in the table view.
- **Real-time Updates**: WebSocket integration for real-time VM status updates.
