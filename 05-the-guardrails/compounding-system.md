# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning | user corrects a location | learns and modifies the location | Y | broken |
| Cross-Domain Transfer | user corrects a vehicle  type | saves vehicle type is added  in user preference | N | broken |
| Network Intelligence | user corrects a location | location data is put in alert queue to fix or investigate | N | active |

**Broken loop identified by partner:** Recursive Learning may end up creating an inaccurate location 
**Fix plan:** When the location is correct by the user and does match the golden data set, send an alert to investigate. 

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

**How knowledge flows:** IA chat location > Alerts queue 

**Where it silos:** location and vehicle data storage in user preferences 


## Governance Policy

**Scope:**
**Autonomy boundaries:**
**Escalation triggers:**
**Audit cadence:**
**Regulatory exposure (EU AI Act / other):**

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
