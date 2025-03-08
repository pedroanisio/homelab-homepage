# Homelab Homepage

Welcome to the Homelab Homepage project. This project provides a customizable and responsive dashboard for managing and monitoring your lab servers, services, and applications.

## Features

- **Dashboard Overview:** Quick access to servers, applications, and services.
- **Customizable Widgets:** Easily add, remove, or customize widgets.
- **Responsive Design:** Adapts seamlessly to both mobile and desktop screens.
- **Centralized Configuration:** Utilize YAML, CSS, and JavaScript custom files to tailor your experience.

## Project Structure

```
homelab-homepage/
│
├── README.md               # Project overview and usage instructions
├── config/
│   ├── bookmarks.yaml      # Predefined bookmarks configuration
│   ├── custom.css          # Custom styles for the homepage
│   ├── custom.js           # Custom JavaScript functions
│   ├── docker.yaml         # Docker deployment configuration
│   ├── kubernetes.yaml     # Kubernetes deployment configuration
│   ├── services.yaml       # Service definitions and endpoints
│   ├── settings.yaml       # Main project settings
│   └── widgets.yaml        # Widget configuration for the dashboard
├── logs/
│   └── homepage.log        # Log file for tracking events and errors
└── images/
    ├── favicon-16x16.png   # Small favicon image
    ├── favicon-96x96.png   # Larger favicon image
    └── favicon.ico         # Standard favicon file
```

## Getting Started

### Prerequisites

- A web browser.
- [Docker](https://docs.docker.com/get-docker/) or [Kubernetes](https://kubernetes.io/) for deployment options (optional).

### Installation

1. **Clone the Repository:**

    ```sh
    git clone <repository_url>
    cd homelab-homepage
    ```

2. **Configure the Application:**

    - Adjust site settings via [config/settings.yaml](./config/settings.yaml).
    - Customize bookmarks in [config/bookmarks.yaml](./config/bookmarks.yaml) and widgets in [config/widgets.yaml](./config/widgets.yaml).
    - Modify [config/custom.css](./config/custom.css) and [config/custom.js](./config/custom.js) as needed for your desired look and functionality.

3. **Deployment Options:**

    - **Docker:** Build and run the container using the provided Docker configuration:

        ```sh
        docker compose -f config/docker.yaml up -d
        ```

    - **Kubernetes:** Deploy using your cluster setup with [config/kubernetes.yaml](./config/kubernetes.yaml).

4. **Run Locally:**

    You can also serve the project locally (for example, with Python's HTTP server):

    ```sh
    python -m http.server 8000
    ```

    Then open [http://localhost:8000](http://localhost:8000) in your browser.

## Usage

Upon launching the Homelab Homepage, you’ll be able to:

- Visualize server statuses and service endpoints.
- Access and manage applications via configurable links and widgets.
- Use quick launch tools defined in the settings.
- Tailor the display with custom CSS and JavaScript adjustments.

## Troubleshooting

- Verify YAML file formatting in the configuration files.
- Check [logs/homepage.log](./logs/homepage.log) for runtime errors.
- Ensure necessary ports are open if deploying via Docker or Kubernetes.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch with your feature or bug fix.
3. Test your changes thoroughly.
4. Submit a pull request for review.

## License

This project is licensed under the MIT License.

## Acknowledgments

- Inspired by various open-source dashboard projects.
- Thanks to the homelab community and all contributors for their support.