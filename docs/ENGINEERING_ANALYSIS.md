# Engineering analysis — perception and control boundaries

The two-controller architecture is builder-reported. This document analyzes that arrangement without asserting an unverified protocol, model, or completed control loop.

## 1. Partition work by responsibility

The reported arrangement separates image capture, computer-side analysis, and motor control. That partition can make each subsystem easier to inspect: camera problems can be investigated before inference, and motor behavior can be tested without a vision model.

The trade-off is dependence on communication and synchronization. Moving processing to a computer does not automatically produce low latency or reliable control. Those properties require a measured path through capture, transmission, analysis, command delivery, and physical response.

## 2. Define the interfaces before claiming integration

| Boundary | Information needed for reproducibility | Present status |
| --- | --- | --- |
| Camera → computer | Transport, image format, dimensions, capture time, frame identity | Unconfirmed |
| Analysis → application | Task, model/version, output schema, confidence meaning | Unconfirmed |
| Application → controller | Command vocabulary, units, limits, acknowledgments | Unconfirmed |
| Controller → drivetrain | Driver identity, verified pins, direction mapping, stop behavior | Unconfirmed |

The discovered local HTTP joystick and WebSocket controller sketches use different interfaces. Their existence does not demonstrate compatibility, and neither has been matched to this robot.

## 3. An image result is not a world position

A detection in a camera image is usually expressed in image coordinates. It does not, by itself, establish object distance or a position in the robot's environment. A metric claim needs a documented geometry/depth method, calibration, and an uncertainty boundary.

Likewise, a recognition score must be explained according to the actual model. It cannot be relabeled as an accuracy percentage without evaluation. No recognition benchmark, calibrated object position, or tracking performance is available for this edition.

## 4. Data freshness matters

For future supervised mobility, a useful trace would associate a frame with capture time, processing completion, command issuance, and controller acknowledgment. That trace helps distinguish a slow image path from a delayed control path.

A proposed controller contract should define expiry of stale commands, behavior after disconnect, and the state after reconnect. These are design requirements to implement and test, not capabilities established by the photographs.

## 5. Validate subsystems before the combined behavior

| Stage | Useful evidence | Current status |
| --- | --- | --- |
| Imaging | Recorded frames with stated resolution and timing | Interface still photograph only |
| Perception | Nonsensitive input set, model identity, correct/incorrect outputs | Not supplied |
| Mobility | Supervised motor-direction and stop trials | Not supplied |
| Integration | Frame-to-command trace and observed response | Not supplied |
| Failure recovery | Recorded disconnect, stop, and reconnect behavior | Not supplied |

This ordering makes failures diagnosable. A dashboard screenshot cannot replace any of these individual checks.

## 6. Scope of the platform

The engineering subject is image capture, analysis, and supervised wheeled mobility. The builder-identified launcher is excluded from the software/control scope. No perception output is connected here to targeting or firing. Future public code must preserve that boundary and exclude private facial data.

See [safety and privacy](SAFETY_AND_PRIVACY.md) and [setup prerequisites](BUILD_AND_TEST.md).
