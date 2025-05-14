# What is PEAS?
PEAS stands for:
- Performance measure
- Environment
- Actuators
- Sensors

This framework is used to formally define any AI agent task. We don't build AIs blindly.

#### PEAS definitions
**Performance Measure:**
This defines the criteria for success of the agent. It evaluates how well the agent is doing its job. For example, in a self-driving car, performance measures could include safety, speed, fuel efficiency, and passenger comfort.

**Environment:**
This refers to the external context or world in which the agent operates. It includes everything the agent interacts with. For a cleaning robot, the environment would be the house or office it cleans, including furniture, dirt, and people.

**Actuators:**
These are the components that carry out the agent's actions. They allow the agent to affect its environment. In a robot, actuators might include wheels, arms, or vacuum motors.

**Sensors:**
These are the components that gather information from the environment. They help the agent perceive what's happening. Examples include cameras, microphones, and temperature sensors.

#### Why does PEAS matter?
Before coding, we need a well-defined agent design problem, PEAS help model that. It's like a design document.

## PEAS in practice (examples)
#### Example 1: Autonomous Vacuum Cleaner
| Component | Description |
| ------------- | ------------- |
| P (Performance) | Cleanliness, energy usage, time efficiency
| E (Environment) | Floor layout, dirt, furniture, walls
| A (Actuators) | Wheels, vacuum motor, brushes
| S (Sensors) | Dirt sensors, bump sensors, location sensors

#### Example 2: Self-Driving Car
| Component | Description |
| ------------- | ------------- |
| P | Safety, legality, passenger, comfort, speed
| E | Roads, traffic, pedestrians, signs, weather
| A | Steering, acceleration, brakes, horn
| S | Cameras, lidar, GPS, speedometer, radar

#### Example 3: Web Search Engine Agent
| Component | Description |
| ------------- | ------------- |
| P | Relevance, speed, user satisfaction, coverage
| E | Web pages, queries, user preferences
| A | Display ranked results, suggestions
| S | User input (query), click patterns


## How to Use PEAS When Designing an AI Agent?
When given a problem like "build an AI to play a board game" or "build an AI that helps people schedule meetings", we do this first:

1. Clearly define PEAS
1. From PEAS, derive:
    - State space
    - Actions
    - Goals or utilities
1. Choose the right type of agent
1. Then apply search, logic, learning, etc.

#### Agent types

| Agent Type | Description
| ------------- | ------------- |
| **Simple Reflex** | Reacts to current percept only (no memory or reasoning)
| **Model-Based** | Maintains an internal state to track the world
| **Goal-Based** | Has specific goals; chooses actions that achieve them
| **Utility-Based** | Chooses actions to maximize long-term usefulness
| **Learning Agent** | Learns from experience to improve its performance

