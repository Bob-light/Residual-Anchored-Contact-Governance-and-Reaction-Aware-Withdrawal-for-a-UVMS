# Conceptual methods / 总体研究思路

## Research question

A UVMS in contact with a surface must coordinate the end effector and vehicle while respecting contact loading, arm motion, and actuation constraints. A useful research question is how contact governance and withdrawal coordination interact when vehicle motion changes the contact geometry or excites arm reactions.

The broad ideas are to update contact governance from the observed local contact condition and to coordinate withdrawal with moving geometry and vehicle reaction. This document describes the design motivation only. It does not contain a controller, governing implementation equations, a parameter-selection procedure, or an executable simulation.

## Comparison logic

A fixed-governance policy with an original withdrawal strategy can serve as a conceptual starting point. Revising withdrawal while retaining that governance defines a withdrawal comparison. Adding locally updated governance while retaining the revised withdrawal defines a governance comparison. This separation helps avoid attributing the effects of several simultaneous changes to a single module.

Fair comparisons should share platform assumptions, disturbances, task definitions, and evaluation rules. Model and controller development should be distinguished from later evaluation. Both adverse and favourable outcomes should be retained in any independently conducted study. These are methodological principles, not results disclosed by this companion.

## Non-core pseudocode

The analysis outline describes checking independently supplied observations, preserving pairing, separating repeated measurements, and presenting effects with appropriate uncertainty. No observations or computed values accompany it.

The contact-teaching outline describes a generic point mass and unilateral compliant contact. It supplies no numerical constants, solver implementation, or illustrative trajectory. It has no UVMS kinematics, thrust allocation, observers, contact governor, or withdrawal controller.

The release-review outline concerns checking that an upload contains only authorized explanations and pseudocode. It is a checklist description rather than a working test suite.

## 中文说明

本研究思路关注接触治理、航行器运动和协调撤离之间的关系。通过分别改变撤离协调与接触治理，可以在概念上区分模块作用。公平对照应保持平台假设、扰动、任务定义与评价规则一致，并区分开发与评价阶段。

本目录仅描述上述研究问题和非核心工作流程，不提供任何试验记录、计算结果、性能图像、轨迹、样例数值、输入配置或控制参数。所有代码文件均为纯注释伪代码，不能运行。方法描述本身不构成有效性、实机可行性或安全保证。
