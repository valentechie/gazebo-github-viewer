# Gazebo GitHub Viewer - Architecture Overview

## Flow

1. **GitHub webhook** triggers on push or pull request events involving model files (.urdf, .sdf, .xacro).
2. **main.py** receives the payload and parses the event to identify affected files.
3. The integration uses the GitHub API to **download the updated model files**.
4. **gazebo_launcher.py** is called to launch the new/modified model in the Gazebo simulator.

## Future Improvements

- Add support for more event types (e.g., pull requests, releases).
- Error handling, logging, and notifications.
- Web dashboard for managing visualizations.

---

This documentation will be expanded as the project develops.