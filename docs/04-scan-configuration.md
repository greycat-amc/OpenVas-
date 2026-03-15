# Vulnerability Scan Configuration and Analysis

Once the laboratory environment has been prepared and network connectivity between the scanner and the target system has been verified, the next step is to configure and execute the vulnerability scan using OpenVAS.

## Target Configuration

The first step is to define the scan target within the OpenVAS web interface.

1. Navigate to **Configuration → Targets**
2. Click **New Target**

<p align="center">
  <img src="../screenshots/targetconfig.png" width="750">
</p>
3. Provide the following information:

- **Name:** Metasploitable2
- **Hosts:** 10.0.2.7
- **Port List:** Default

This configuration defines the system that will be analyzed by the vulnerability scanner.

<p align="center">
  <img src="../screenshots/openvas-target-config.png" width="750">
</p>

---

## Scan Task Configuration

After defining the target, a scan task must be created.

1. Navigate to **Scans → Tasks**
2. Click **New Task**
3. Configure the task with the following parameters:

- **Name:** Metasploitable2 Scan
- **Scan Target:** Metasploitable2
- **Scan Config:** Full and Fast

The **Full and Fast** configuration performs a comprehensive vulnerability assessment while maintaining reasonable scanning time.

<p align="center">
  <img src="../screenshots/openvas-task-config.png" width="750">
</p>

---

## Launching the Scan

Once the task has been created, the scan can be executed by clicking the **Start Scan** button.

During this phase, OpenVAS performs several actions:

- host discovery
- port scanning
- service detection
- vulnerability testing using its vulnerability test database

The duration of the scan will depend on the number of detected services and the complexity of the target system.

<p align="center">
  <img src="../screenshots/openvas-scan-running.png" width="750">
</p>

---

# Vulnerability Report Analysis
