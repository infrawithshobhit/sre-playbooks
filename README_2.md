# SRE Playbooks — Real Production Incident Handling

This repository contains **real-world SRE playbooks, incident reports, and automation patterns** used to run and protect production systems.

This is not theory.  
This is how high-scale platforms are actually operated.

---

## What you’ll find here

### 🔥 Incidents
Located in `/incidents`

These are full production-style incident reports including:
- What broke
- How it was detected
- Dynatrace signals used
- What was done
- What was automated after

---

### 🛠 Runbooks
Located in `/runbooks`

Step-by-step guides for common failures:
- API latency
- High CPU
- Kafka lag
- Memory leaks

These are meant to be followed during live incidents.

---

### 📊 Dynatrace
Located in `/dynatrace`

Everything related to observability:
- Metric queries
- Alert rules
- Dashboard design
- Noise reduction patterns

---

### ⚙ Automation
Located in `/automation`

Scripts and YAML that:
- Restart stuck pods
- Scale services
- Apply safe mitigations
- Reduce MTTR

---

### 📄 Templates
Located in `/templates`

Reusable templates so incidents are:
- Documented the same way
- Auditable
- Automation-ready

---

## Who this is for

- Site Reliability Engineers
- Platform Engineers
- Observability teams
- Engineering Managers
- Anyone running production systems

---

## Why this exists

Most outages happen because:
- Signals are misunderstood
- Knowledge is tribal
- Humans panic

This repo turns:
> Experience → Process → Automation → Reliability

---

## Author

Shobhit Verma  
Lead SRE & Observability Architect  
Building boring, predictable, self-healing systems.
