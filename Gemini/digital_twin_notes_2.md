For a video game inspired by older Nintendo titles like Baseball Stars, you'd typically handle mouse and keyboard input in a few key ways. For the keyboard, you'd map directional keys (like the arrow keys or WASD) to in-game movement. For actions like batting or throwing, you could use other keys (e.g., the spacebar, Enter, or the X and C keys). For mouse control, you would likely use mouse clicks for actions and the mouse position to aim or select targets, similar to how a cursor works in a menu. The concept of "Vibe Code" can streamline this by using natural language prompts to generate the event listeners and input handling functions that map these physical inputs to in-game actions.

Yes, you could absolutely put the game's code in Docker containers and run the game from there. Docker is excellent for creating a portable, isolated environment. This means the container would hold all the necessary code, dependencies, and runtime environment for the game to run correctly, regardless of the host machine's specific setup. While most people use Docker for web services or game servers, it's possible to use it for a desktop application with a graphical user interface (GUI) by using a display server like X11 and passing the display to the container. This would align with your preference for creating Docker-based scripts for your projects.



I've provided an initial breakdown of how to approach this. What aspect of the development process—the input mapping or the Docker implementation—would you like to start with first?

I Played DOOM on my wife's computer with Docker!

This video is relevant because it demonstrates a successful, if unusual, use case for running a graphical application, specifically a game, inside a Docker container.

I Played DOOM on my wife's computer with Docker! - YouTube
typecraft · 30K views
