Master Prompt for DevOps AI Agent Project

Project Goal

Create a single-page web application with a cyberpunk theme that serves as a front-end interface for a hypothetical AI/LLM training system. The application must be delivered as a complete, self-contained Docker container. The primary goal is to establish a robust and easily manageable infrastructure for uploading and managing training data from a host machine.

Web Interface Requirements

Theme: The user interface must have a distinct cyberpunk aesthetic. This includes a dark, gritty color palette with vibrant neon accents (e.g., electric blue, magenta, green). Use of futuristic typography (like 'Orbitron' or 'Roboto Mono') is highly encouraged.

Structure: The interface should consist of two main sections, accessible via a tabbed navigation system:

Main Operations: A primary terminal-style interface for executing commands.

LLM Training: A sub-page dedicated to managing and initiating training tasks, displaying data status, and showing training progress.

Responsiveness: The layout must be fully responsive and optimized for a wide range of devices, from mobile phones to desktop monitors.

Core Functionality

Data Management: The "LLM Training" tab must show a dynamic count of the files detected in the mounted data directory. This should be a clear visual indicator that the host volume is successfully linked.

Training Simulation: The interface should have a button to "Start LLM Training." Clicking this button should trigger a simulated training process, visually represented by a progress bar that animates from 0% to 100%.

Command Terminal: The "Main Operations" tab should have a text area and an "Execute" button to simulate a command-line interface. The output of the "executed" command should be displayed below.

Backend and Infrastructure

Dockerization: The entire application, including the web server, must be packaged into a single Docker image.

Web Server: Use Nginx to serve the static HTML web page.

Host Volume: The Docker container must be configured to mount a volume from the host machine. The path on the host should be ./llm_data, and it should be mounted to a corresponding directory inside the container (e.g., /usr/share/nginx/html/data).

Persistence: The content of the ./llm_data directory (images, videos, text, etc.) must persist across container restarts. Any files added to this directory on the host machine should become accessible to the application within the container without rebuilding the image.

Orchestration: Provide a docker-compose.yml file to simplify the build, run, and volume-mounting process with a single command (docker-compose up --build -d).

Output and Deliverables

The solution must include the following files:

index.html: A single, complete HTML file containing all of the HTML, CSS, and JavaScript for the web interface.

Dockerfile: The Dockerfile to build the Nginx image.

docker-compose.yml: The Docker Compose configuration file.

README.md: A comprehensive guide on how to set up, run, and use the project.

Obsidian_Note.md: A separate Markdown file summarizing the project for personal knowledge management.
