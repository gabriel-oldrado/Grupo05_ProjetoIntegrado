# \# Academic Services Uptime Monitor

# 

# \## Overview

# 

# Academic Services Uptime Monitor is an interdisciplinary project developed by Group 05 at Fatec Ferraz de Vasconcelos. The project proposes monitoring the availability and response time of two simulated academic services: the Academic Portal and the Online Library.

# 

# The monitor periodically sends HTTP health checks to both services, records their status and response time, and displays the latest results on a web dashboard.

# 

# \## Problem

# 

# Students and staff depend on academic services to access information and resources. If a service becomes unavailable or responds slowly, users may not know which service is affected. This project demonstrates how a monitoring system can identify and report service availability.

# 

# \## Project Status

# 

# The diagrams describe a proposed local Docker network. The monitor, dashboard, service simulations, and network setup still need to be implemented and tested.

# 

# \## Architecture

# 

# The proposed system contains:

# 

# \- \*\*Monitor and web dashboard\*\* — checks the simulated services, measures response times, and displays their latest status.

# \- \*\*Academic Portal\*\* — a simulated service that responds to an HTTP health check.

# \- \*\*Online Library\*\* — a simulated service that responds to an HTTP health check.

# \- \*\*Local record\*\* — proposed storage for each check’s timestamp, status, and response time.

# \- \*\*Browser\*\* — accesses the dashboard on the local computer.

# 

# The proposed Docker bridge network uses the subnet `172.28.5.0/24`. The detailed network and architecture diagrams are in \[`etapa2/diagramas/`](etapa2/diagramas/).

# 

# \## Tools and Protocols

# 

# \- Docker Engine and a local bridge network are proposed for the network simulation.

# \- IPv4 and TCP are proposed for communication between containers.

# \- HTTP is proposed for health checks and dashboard access.

# \- The implementation language and local storage technology have not yet been selected.

# 

# \## Proposed Network Addresses

# 

# | Component | Proposed address | Purpose |

# |---|---|---|

# | Browser on the host | `127.0.0.1:8080` | Local dashboard access |

# | Monitor and dashboard | `172.28.5.10:8080` | Health checks and dashboard |

# | Academic Portal | `172.28.5.20:8081` | Simulated academic service |

# | Online Library | `172.28.5.30:8082` | Simulated academic service |

# 

# These addresses are part of the proposed design and must be confirmed during implementation.

# 

# \## Communication Flow

# 

# 1\. The monitor sends an HTTP `GET /health` request to each simulated service.

# 2\. The service returns an HTTP status.

# 3\. The monitor measures the response time and classifies the service as available or unavailable.

# 4\. The monitor records the timestamp, status, and response time in local storage.

# 5\. The browser requests the dashboard, which displays the latest recorded results.

# 

# \## Failure Scenario

# 

# The proposed failure test stops the Online Library service or makes its `/health` endpoint unavailable while the Academic Portal continues responding. The dashboard should report the Library as unavailable and continue showing the Portal’s status.

# 

# The failure scenario has not yet been run. Add screenshots or logs and the observed results after performing the test.

# 

# \## Diagrams and Deliverables

# 

# \- \[Network diagram — PNG](etapa2/diagramas/01-diagrama-de-rede.png)

# \- \[Network diagram — editable Draw.io file](etapa2/diagramas/01-diagrama-de-rede.drawio)

# \- \[Distributed system architecture — PNG](etapa2/diagramas/02-arquitetura-distribuida.png)

# \- \[Distributed system architecture — editable Draw.io file](etapa2/diagramas/02-arquitetura-distribuida.drawio)

# \- \[Stage 2 report — PDF](etapa2/Grupo05\_Etapa2\_DiagramasTecnicos.pdf)

# \- \[Stage 2 report — editable Word file](etapa2/Grupo05\_Etapa2\_DiagramasTecnicos.docx)

# 

# \## Team

# 

# Group 05 — Fatec Ferraz de Vasconcelos  

# Project theme: Academic service availability

# 

# \## Language

# 

# This README is written in English as part of the Technical English component of the interdisciplinary project.

