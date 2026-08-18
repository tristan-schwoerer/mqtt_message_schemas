# MQTT Message Schemas

JSON Schema definitions for the MQTT messages exchanged in the AP2030-UNS
production line (commands, states, positions, planning, quality results, …).

These schemas are used by:

- **aas-registration-service** — to embed the payload structure of AID
  (Asset Interfacing Description) action inputs/outputs and property
  datapoints directly into the published Asset Administration Shell
  (the schema URL rides as a supplemental semantic id on the DataSchema).
- Downstream standalone services (operation delegation, controller, planner,
  DataBridge) — to build and validate MQTT payloads from the AAS.

The schemas are published under

    https://aausmartproductionlab.github.io/AP2030-UNS/MQTTSchemas/<file>

(see the `schema_parser.SchemaParser` local resolution in the registration
service, which maps that URL namespace back to this repository).
