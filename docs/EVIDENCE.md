# Evidence and source status

| ID | Artifact | Supported observation |
| --- | --- | --- |
| V1 | `media/robot-closeup.jpg` | Physical wheeled robot, camera module, TFT display, board/wiring, battery holders |
| V2 | `media/camera-and-interface.jpg` | Camera/antenna mounted on robot; laptop showing an image panel and movement buttons |
| V3 | Builder description | ESP32 camera, second ESP32 motor controller, Wi-Fi, computer-side AI, gel-bead mechanical payload |

V3 is a builder report, not a verified runtime result. V1/V2 are static photographs. The camera image visible on the laptop does not establish streaming rate, AI inference, or motor response.

## Annotated presentation

`media/robot-hardware-anatomy.png` is an explanatory layout made from V1, using a manual background mask, numbered markers, and English component principles. It is not additional hardware or test evidence. The mask removes exterior room context, preserves the source view and photographed assembly, and does not reconstruct parts outside the original frame. Background visible within the assembly may remain. The original V1 file is unchanged and available in the README's expandable source section.

The editable layout is `docs/hardware-plate.svg`; its image reference points to V1. The controller identity, circuit pin mapping, cable purpose, regulation, and runtime behavior remain unverified. Annotation numbers indicate component regions, not exact electrical connection points. No illustrated wire is a verified circuit diagram.

## Candidate code mismatch

The reviewed `robot_project.zip` describes an ESP8266 motor controller, XIAO camera, AI-Thinker pan/tilt camera, MQTT, and a Python face-recognition server. This differs from the stated two-ESP32 arrangement. Its camera tracking code is not suitable for inclusion here while a launcher is present, and its enrollment/training material is excluded.

Other local firmware candidates describe joystick HTTP commands and ESP32-S3 WebSocket motor control. Their protocols do not form a verified matched pair, and neither was established as this photographed robot's firmware. No code has been moved into this public review folder merely because its filename mentions a robot.

## Missing evidence

Confirm the original camera, motor, and host software paths; exact board models; communication protocol; wiring; and which recognition tasks were actually demonstrated. Supply an object-focused run showing the camera input and computer output. Demonstrations must keep launcher actuation disconnected and must not disclose private faces or network credentials.
