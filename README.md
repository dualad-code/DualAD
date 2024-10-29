# DualAD: Dual-Layer Planning for Autonomous Driving
 
# (The code cleaning is still in progress!)

![DualAD Framework](./assets/teaser.png)


> **DualAD** is an autonomous driving framework that integrates reasoning capabilities with traditional planning modules to handle complex driving scenarios. By leveraging a dual-layer system, DualAD combines rule-based planning with large language models (LLMs) for more human-like cognitive reasoning in critical situations.

## Overview

DualAD aims to imitate human cognitive processes in autonomous driving by separating planning into two layers:
1. **Lower Layer** – Manages basic driving tasks through a rule-based motion planner.
2. **Upper Layer** – Acts as a reasoning module using LLMs to assess potential dangers and make real-time adjustments in critical scenarios.

### Key Features
- **Dual-Layer Architecture**: Combines routine driving tasks with high-level reasoning for safety and efficiency.
- **Text Encoding**: Converts driving scenarios into textual descriptions, enhancing the LLM’s understanding.
- **Closed-Loop Simulations**: Validates performance in realistic, complex environments, outperforming standard planners.
## Performance

DualAD demonstrates improved performance in challenging scenarios compared to other planners. Key metrics such as **Closed-Loop Score (CLS)** and **Reactive Closed-Loop Score (R-CLS)** showcase DualAD’s ability to outperform rule-based and learning-based models in terms of safety and decision quality.

| Planner                  | Hard-55 CLS | Super-Hard-24 CLS |
|--------------------------|-------------|--------------------|
| IDM                      | 50.12       | 34.56             |
| Lattice-IDM              | 52.36       | 39.76             |
| **DualAD (Lattice-IDM)** | **60.25**   | **57.31**         |

## Installation

### Prerequisites
- Python 3.8+
- NuPlan Simulator (for closed-loop simulation)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/username/DualAD.git
   cd DualAD
2. Install the dependencies:
   ```bash
   pip install -r requirements.txt