# Hardware anatomy — how the visible parts work

The [annotated plate](../media/robot-hardware-anatomy.png) is a presentation of the [original photograph](../media/robot-closeup.jpg). These descriptions explain component principles. They do not establish that a particular firmware function was running.

| Marker | Component region | Working principle | Project-specific boundary |
| --- | --- | --- | --- |
| 1 | Camera module | A lens focuses the scene onto an image sensor. The sensor converts incoming light into electronic image data for subsequent processing. | Sensor model, actual capture settings, and the computer processing path are unconfirmed. |
| 2 | TFT display | A controller sends pixel data to the display, allowing it to show text and graphics. | The screen is dark in the original photograph; displayed telemetry or status is not demonstrated. |
| 3 | Controller board | A microcontroller executes firmware and exchanges electrical signals through its interfaces and pins. | Exact board, firmware revision, pin assignments, and attached devices are unconfirmed. |
| 4 | Battery holders | Cells provide electrical energy to the circuit; holders retain them and expose electrical contacts. | Cell chemistry, connection topology, operating voltage, protection, and regulation were not established. |
| 5 | Wheel and gearbox region | A geared motor converts electrical energy into shaft rotation; the gear train couples that motion to the wheel. | Motor driver, gearing, commands, speed, and available torque are unconfirmed. The marker identifies the drivetrain region, not hidden internals. |
| 6 | Wiring and chassis | Conductors carry power and signals. The deck supports and positions the assembled modules. | Wire colors do not establish circuit function or a verified power diagram. |
| 7 | Cable connection | A physical cable provides an electrical connection between assemblies. | Whether this particular link supplies power, carries data, or serves another role is not confirmed from the photograph. |

Not every visible object can be assigned a function from appearance. In particular, the blue cylindrical component and other partially obscured items are retained without speculative labels. The seven markers group the identifiable component regions; they are not a complete bill of materials.

## Presentation provenance

The publication plate is rendered from the editable [SVG layout](hardware-plate.svg), with the original JPG embedded during rasterization. The final hardware image is photographic source content, not a generated replacement. The black background is a presentation mask rather than the original environment. Text and leader lines are editorial additions; they must not be used to infer wiring, calibration, measurements, or operating state.
