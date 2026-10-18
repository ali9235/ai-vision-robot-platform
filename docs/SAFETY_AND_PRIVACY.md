# Safety and privacy

This publication covers imaging, computer-side analysis, and supervised mobile-platform engineering. The photographed gel-bead launcher is mechanical context only.

- Remove/disconnect launcher power before software, camera, or mobility testing. No firing wiring, firing commands, target tracking tied to actuation, or autonomous human-targeting functionality is distributed.
- Keep wheels raised during first control checks, keep mechanisms clear, and provide an accessible physical power cutoff.
- Do not treat a recognition label as authorization to move near a person. Human recognition and autonomous safety have not been validated.
- Use nonsensitive objects for vision demonstrations. Do not publish face enrollment photos, identity labels, trained face models, private video, or network credentials.
- Keep development endpoints on an appropriately restricted local network. Authentication and robust command-loss handling must be implemented and tested before broader connectivity.

Static photographs are reviewed for obvious unwanted information, but the builder should review the final images before public release. No safety certification, safe operating range, or verified fail-safe is claimed.
