#  Safe Semantic Planner

A D* Lite based path planner implemented in Python for planning in a finite Cartesian state space.

The planner finds safe and reliable paths while considering transition cost, safety, reliability, bad states, and dynamically changing environments.

The deployed link: https://safe-semantic-planner-bzkdux9hn34xd8nxhkxuxd.streamlit.app/

---

## 🚀 Features

- D* Lite based path planning
- Finite Cartesian state-space representation
- Transition cost optimization
- Safety-aware planning
- Reliability-aware planning
- Bad-state avoidance
- Dynamic transition disabling
- Dynamic transition addition
- Dynamic goal updates
- Dynamic bad-state updates
- Incremental replanning
- Interactive Streamlit visualization
- Experimental benchmark evaluation
- Planning performance measurements

---

## 🧠 Planning Approach

The system uses the **D* Lite** algorithm to find paths from an initial state to a goal state.

Each transition contains information about:

- Cost
- Safety
- Reliability
- Availability

The planner considers these properties when selecting a path.

States can also be marked as **bad states**. The planner avoids these states when searching for a safe route.

The main advantage of D* Lite is its ability to handle changes in the environment efficiently.

When a transition, goal, or other planning condition changes, the planner can update the existing search and perform **incremental replanning** rather than starting the entire search from scratch.

---

## 🗺️ Interactive Streamlit Application

The project includes an interactive web application built using Streamlit.

The application allows users to:

1. Select a test case.
2. Run the planner.
3. View the generated state-space graph.
4. View the selected path.
5. Disable transitions dynamically.
6. Change the goal state.
7. Change bad states.
8. Add new transitions.
9. Perform incremental replanning.
10. View planning statistics.
11. Run the complete experimental evaluation.

The graph visually represents:

- Initial state
- Goal state
- Bad states
- Available transitions
- Selected path

The selected path is highlighted in green.

---

## 🔄 Dynamic Replanning

The application demonstrates incremental replanning using D* Lite.

For example, in the dynamic transition test, the initial path is:

```text
S → A → G
