# What is an AI Agent?
An AI agent is an entity that perceives its environment through sensors and acts upon it using actuators to achieve specific goals. It can be anything from a software program to a physical robot, reacting and adapting to its environment based on predefined objectives.

## Components of an AI Agent
An AI agent typically has the following components:

**Sensors:** Gather information about the environment, such as cameras or microphones.

**Actuators:** Allow the agent to perform actions in the environment, like motors or wheels.

**Performance Measure:** Defines how well the agent is achieving its goals. It serves as a metric of success.

**Environment:** The world or context the agent operates in, which includes everything the agent can interact with.

## Types of AI Agents
AI agents can be classified into different types based on their behavior and the complexity of their operations:

| Agent Type | Description
| ------------- | ------------- |
| **Simple Reflex** |  React only to the current percept (observation) and do not have memory or the ability to reason about past events.
| **Model-Based** | These agents maintain an internal model of the world, allowing them to base decisions not only on the current percept but also on memory of past states.
| **Goal-Based** | These agents are driven by specific goals. They evaluate possible actions based on how likely they are to achieve their goals.
| **Utility-Based** | These agents make decisions by selecting actions that maximize their expected long-term utility or performance. They often handle trade-offs between competing goals.
| **Learning Agent** | These agents can learn from experience, improving their performance over time based on past experiences or observations.

## Designing an AI Agent
The design process for creating an AI agent involves several steps:

- Define the problem and understand the environment in which the agent will operate.
- Specify the performance measure that defines the agent's success.
- Identify sensors that the agent will use to perceive the environment.
- Select actuators that the agent will use to act upon the environment.
- Choose the appropriate type of agent based on the task and problem complexity.
- Implement the agent using AI techniques like search, machine learning, or logic-based reasoning.

#### Why Do Agent Types Matter?
Choosing the right type of agent depends on the task at hand:

- Simple Reflex Agents are suitable for tasks that involve minimal processing or immediate, reactive actions (e.g., a thermostat).
- Model-Based Reflex Agents are useful when the task requires memory of past actions and states (e.g., a robot that needs to remember previously cleaned areas).
- Goal-Based Agents excel in tasks where long-term planning and goal achievement are required (e.g., a chess-playing AI).
- Utility-Based Agents are ideal for tasks that involve balancing multiple competing objectives (e.g., a self-driving car that maximizes safety, speed, and comfort).
- Learning Agents are crucial for tasks where continuous improvement and adaptation are needed (e.g., an AI that improves its performance over time based on feedback).

----

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

#### Examples of choosing agent types
Once PEAS is defined, we can ask:
- Is simple reaction enough?
- Do I need memory of the past?
- Do I need planning toward goals?
- Do I need trade-offs between different good outcomes (utility)?
- Can the agent learn to improve over time?

**Autonomous Vacuum Cleaner:** 
Model-Based + Possibly Learning
- Why? It needs to remember which rooms it cleaned.
- It may learn to clean more efficiently over time.

**Chess-Playing AI** Goal-Based or Utility-Based
- Performance = Winning
- Why? The agent must plan many moves ahead (goal: checkmate).
- If using evaluation functions (e.g., scoring positions), it's utility-based.

**Other examples:**

| Task | Best Agent Type(s)
| ------------- | ------------- |
| Thermostat | Simple Reflex |
| Vacuum robot | Model-Based, possibly Learning |
| Self-driving car | Utility-Based + Learning |
| Web search engine | Utility-Based |
| Game-playing AI (chess, Go) | Goal-Based or Utility-Based |
| AI assistant (e.g., Siri) | Utility-Based + Learning |

