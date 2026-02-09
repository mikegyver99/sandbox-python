# sandbox-python

A simple Flask web application for demonstrating OpenShift's source-to-image (s2i) deployment.

## What it does

This is a sample Python web application built with Flask that displays a welcome page with information about the Red Hat OpenShift Developer Sandbox. The application demonstrates:

- A basic Flask web server
- Serving HTML templates with Bootstrap styling
- Static file serving (images)
- A simple landing page with links to OpenShift learning activities

The application is designed to be deployed to Red Hat OpenShift using the source-to-image (s2i) build process.

## Prerequisites

- Python 3.x
- pip (Python package manager)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/mikegyver99/sandbox-python.git
   cd sandbox-python
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## How to use it

### Running locally

To run the application on your local machine:

```bash
python app.py
```

The application will start on `http://0.0.0.0:8080`. Open your web browser and navigate to `http://localhost:8080` to view the application.

### Deploying to OpenShift

This application is designed to work with the [Developer Sandbox for Red Hat OpenShift](https://developers.redhat.com/developer-sandbox/get-started), which gives you a renewable 30-day free access to an OpenShift cluster.

#### Using Source-to-Image (s2i)

One of the key features of OpenShift is the ability to build applications using the built-in source-to-image (s2i) technology. This technology automatically pulls source code from a Git repository and builds a container image.

To deploy this application using s2i:

1. Sign up for the [Developer Sandbox for Red Hat OpenShift](https://developers.redhat.com/developer-sandbox/get-started)
2. Log into your OpenShift web console
3. Create a new application using the "From Git" option
4. Provide the URL to this repository
5. OpenShift will automatically detect that this is a Python application and build it using the Python s2i builder
6. Once the build completes, your application will be deployed and accessible via a public URL

## Project Structure

```
sandbox-python/
├── app.py              # Main Flask application
├── requirements.txt    # Python dependencies
├── templates/          # HTML templates
│   └── index.html     # Main page template
├── static/            # Static files (images, CSS, JS)
│   └── img/          # Image files
├── README.md          # This file
└── LICENSE            # License file
```

## Technologies Used

- **Flask 1.1.4**: Lightweight Python web framework
- **Bootstrap 5.1.1**: Frontend CSS framework for responsive design
- **Python 3.x**: Programming language

## Learn More

- [Developer Sandbox for Red Hat OpenShift](https://developers.redhat.com/developer-sandbox/get-started)
- [OpenShift Documentation](https://docs.openshift.com/)
- [Flask Documentation](https://flask.palletsprojects.com/)
