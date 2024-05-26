# Real-Time RDP Attack Geolocation with Azure Sentinel and PowerShell

🎯 **Objective**: In this project, I monitored live RDP brute force attacks on a honeypot virtual machine, extracted attacker data, and mapped geolocation information using PowerShell and Azure Sentinel.

🛠️ **Tools Used**
- **PowerShell**: Script to parse Windows Event Logs and extract failed RDP attempts.
- **ipgeolocation.io**: API to fetch geographic details of attacking IP addresses.
- **Azure Sentinel**: SIEM tool to visualize attack data and geolocation on a map.

🧠 **Skills Learned**
- Configuring a honeypot VM for security monitoring.
- Writing PowerShell scripts to interact with Windows Event Logs and external APIs.
- Using Azure Sentinel for real-time data analysis and visualization.
- Mapping geolocation data to understand the geographic distribution of attacks.

## 📝 Steps

1. **Preparation**
   - Set up Azure Sentinel and connect it to a honeypot VM.
   - Installed necessary PowerShell modules for scripting and API interaction.

![Honey Pot Virtual Machine in Azure Sentinel](https://i.imgur.com/4sialr3.png)
<p align="center"><em>Figure 1: Honey Pot Virtual Machine in Azure Sentinel</em></p>

![Configured the IPgeolocation API to track comprehensive IP details](https://i.imgur.com/6e8LSaX.png)
<p align="center"><em>Figure 1.1: Configured the IPgeolocation API to track comprehensive IP details</em></p>

2. **Observation**
   - Analyzed failed RDP attempts captured in Windows Event Logs.
   - Recognized patterns and frequency of attacks from various regions.

![Failed Windows Event Logs](https://i.imgur.com/2nVSCdn.png)
<p align="center"><em>Figure 2: Failed Windows Event Logs</em></p>

![log-honeypot Logs Data in Custom Fields](https://i.imgur.com/f9iCAAu.png)
<p align="center"><em>Figure 2.1: log-honeypot Logs Data in Custom Fields</em></p>

3. **Using PowerShell**
   - **Extracting Event Log Data**:
     - Parsed Windows Event Logs for failed RDP attempts using PowerShell.
   - **Geolocation Lookup**:
     - Used ipgeolocation.io API to fetch geographic information of attacker IPs.
   - **Custom Log Creation**:
     - Created custom logs with geodata and visualized them in Azure Sentinel.

![Powershell script Extracting Event Log Data > Geolocation Lookup > Custom Log Creation](https://i.imgur.com/lCB4vmZ.png)
<p align="center"><em>Figure 2.2: Powershell script Extracting Event Log Data > Geolocation Lookup > Custom Log Creation</em></p>

4. **Visualization in Azure Sentinel**
   - **Map Setup**:
     - Configured Azure Sentinel to display geolocation data on a map.
   - **Real-Time Monitoring**:
     - Monitored and visualized live RDP attacks, identifying geographic hotspots.

![World map of incoming attacks after 24 hours](https://i.imgur.com/mGQ8WFU.png)
<p align="center"><em>Figure 3: World map of incoming attacks after 24 hours</em></p>




Hope this project was insightful to you, feel free to share any feedback or suggestions!
