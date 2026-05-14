# ReAct Infra Health Agent

A minimal Python-based ReAct (Reasoning + Acting) agent that diagnoses simulated infrastructure health issues using step-by-step reasoning and tool execution.

## Overview

This project demonstrates a simple ReAct agent workflow commonly used in AI-powered DevOps and SRE systems.

The agent:

* Reasons step-by-step
* Calls diagnostic tools
* Observes outputs
* Generates a structured incident report

The implementation is intentionally lightweight and runs directly in Google Colab without external dependencies.

---

# Scenario

The simulated scenario diagnoses a Kubernetes pod crash caused by high disk utilization.

Example flow:

Thought → Action → Observation → Answer

---

# Features

* Minimal ReAct agent implementation
* Simulated infrastructure diagnostics
* Tool calling pattern
* Structured incident reporting
* Google Colab compatible
* Beginner-friendly implementation

---

# Tools Used

The agent uses mock infrastructure tools:

* `get_pod_status()`
* `check_disk()`

These simulate infrastructure monitoring actions.

---

# Project Structure

```bash
react-infra-agent/
│
├── react_agent.ipynb
├── README.md
├── screenshot.png
└── requirements.txt
```

---

# ReAct Workflow

```text
Thought: User reports pod crash. I should inspect pod status.

Action: get_pod_status()

Observation: CrashLoopBackOff

Thought: CrashLoopBackOff may be caused by storage issue. Check disk usage.

Action: check_disk()

Observation: Disk usage is 97%

Thought: High disk utilization likely causing pod failure.

Answer:
Structured incident report generated.
```

---

# Sample Incident Report

```python
{
  "incident": "Kubernetes Pod Crash",
  "severity": "High",
  "root_cause": "Disk usage exceeded threshold",
  "pod_status": "CrashLoopBackOff",
  "disk_status": "Disk usage is 97%",
  "recommendation": [
      "Clean unused logs",
      "Increase disk volume",
      "Restart affected pod"
  ]
}
```

---

# How to Run

## Google Colab

1. Open Google Colab
2. Create a new notebook
3. Paste the Python code
4. Run the notebook cell

No external libraries are required.

---

# Deliverables

* Google Colab Notebook (.ipynb)
* ReAct Trace Screenshot
* GitHub Repository

---

# Future Improvements

Possible enhancements:

* Add CPU and memory diagnostics
* Integrate real Kubernetes APIs
* Add LangChain/OpenAI support
* Real-time monitoring integration
* Multi-step autonomous remediation

---

# Author

Sachin Sooraj
