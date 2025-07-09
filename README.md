#  5G Mobile Lab Setup Using srsRAN & Open5GS (FAU)

This repository supports a **5G mobile network lab** introduced for **master’s students** at Friedrich-Alexander-Universität Erlangen-Nürnberg (FAU) in the *Communication Systems* course. It upgrades a previous 4G LTE-based setup to a **containerized 5G Standalone (SA) network** using Docker, **srsRAN**, and **Open5GS**.

---

##  Objectives

- Provide students with hands-on experience deploying and configuring 5G core (5GC) and access (gNB) components.
- Replace 4G EPC with a 5G SA architecture using open-source platforms.
- Simplify setup using pre-built Docker containers:
  - [mamdouhegy/open5gs](https://hub.docker.com/repository/docker/mamdouhegy/open5gs)
  - [mamdouhegy/srsran](https://hub.docker.com/repository/docker/mamdouhegy/srsran)

---

##  System Architecture

- **Access Network (gNB)**:  
  Software-defined radio using `srsRAN` container.
  
- **Core Network (5GC)**:  
  Full Open5GS stack including AMF, SMF, UPF, AUSF, and UDM in a container.

- **Devices**:  
  Commercial 5G-enabled Android smartphones with programmable SIM cards.

- **Containerized Deployment**:  
  All components run on a single Ubuntu host using Docker Compose.

See architecture diagram in the included PDF: `5G Network Deployment Using Docker Containers...pdf` .

---

##  What Students Do

1. Launch gNB and 5GC containers with preconfigured scripts.
2. Edit YAML config files (`gnb.yml`, `amf.yml`, `upf.yml`) for frequency bands, IP settings, etc.
3. Insert preconfigured SIMs into real 5G smartphones.
4. Force NR-only mode and test internet access via the 5GC.
5. Troubleshoot via Docker logs and monitor PCAP traces.

Exercise instructions provided via `a08.pdf`:contentReference[oaicite:0]{index=0}.

---

##  Included Resources

-  `5G Network Deployment Using Docker Containers.pdf` – Setup guide and architecture.
-  `a08.pdf` – Practical lab sheet used in teaching.
-  Docker images:
  - [`mamdouhegy/open5gs`](https://hub.docker.com/repository/docker/mamdouhegy/open5gs)
  - [`mamdouhegy/srsran`](https://hub.docker.com/repository/docker/mamdouhegy/srsran)

---

##  Notes

- Based on open-source [srsRAN 5G](https://docs.srsran.com/) and [Open5GS](https://open5gs.org/).
- SDR hardware used: BladeRF x40 (or any compatible USRP).
- SIM provisioning tool: [pySim](https://github.com/osmocom/pysim)

---

##  Educational Impact

This lab introduces students to:
- Full-stack 5G deployment (RAN + Core)
- SDR hardware integration
- Containerized telecom workflows
- Network troubleshooting and protocol tracing

---

 For questions: mamdouh.muhammad@fau.de
