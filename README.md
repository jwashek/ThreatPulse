# ThreatPulse
An OSINT-driven threat intelligence platform that keeps you up-to-date with current cybersecurity trends. Built to work with Jupyter notebooks.

ThreatPulse demonstrates advanced OSINT (Open Source Intelligence) capabilities by automatically collecting, analyzing, and reporting on current cybersecurity threats from multiple authoritative sources. If anyone has ever asked you: *"How do you stay current with cybersecurity threats?"* you now have your answer with ThreatPulse!

## Core Capabilities
### Real-Time OSINT Collection
- **Government Sources**: CISA cybersecurity advisories and alerts
- **Vulnerability Intelligence**: National Vulnerability Database (NVD) CVE feeds
- **Security News**: The Hacker News, Krebs on Security, BleepingComputer
- **Malware Intelligence**: MalwareBazaar API for recent malware samples
- **Threat Actor Tracking**: Real-time analysis and activity profiling

### Analysis Engine
- **Threat Trend Identification**: Pattern recognition across multiple intelligence sources
- **Malware Family Tracking**: Prevalence analysis and classification
- **Threat Actor Profiling**: Attribution, TTPs, and activity level assessment
- **Attack Technique Mapping**: MITRE ATT&CK framework integration
- **Target Analysis**: Industry and vendor-specific threat intelligence

### Reporting
- **Executive Dashboards**: Executive Summary for executive management and C-level personnel
- **Technical Intelligence**: Detailed threat actor and malware analysis
- **Visual Analytics**: Comprehensive threat landscape visualizations

## Quick Start
### Prerequisites
- Python 3.7+
- Jupyter Notebook
- Internet connection for OSINT collection

### Installation
**Option 1: Anaconda (Easiest and recommended)**
Download and install [Anaconda](https://www.anaconda.com/download/success) for your target system.

**Option 2: Manual Installation**
```bash
pip install jupyter pandas matplotlib seaborn requests beautifulsoup4 feedparser numpy
jupyter notebook
```

### Launch Jupyter
1. Open the Anaconda application
2. Select "Launch" for the Jupyter Notebook app
3. Select "File" --> "New" --> "Notebook"
4. Select the default Kernel and click "Select"
   
### Install Dependencies 
1. Run the below command in the first cell
```python
!pip install feedparser beautifulsoup4
```
2. **Restart Kernel**: Kernel --> Restart Kernel
3. **Load ThreatPulse**: Copy the main code (i.e., the [ThreatPulse.ipynb](https://github.com/jwashek/ThreatPulse/blob/main/ThreatPulse.ipynb) file into a new cell)
4. Press the triangle button to Run the code in the cell.

## Usage Examples
### Basic Threat Intelligence Collection
```python
# Initialize and run complete intelligence gathering, though this should be auto-enabled with the notebook
collector, analyzer = run_threat_intelligence_collection()
```

**Sample Output:**
```
[+] Starting ThreatPulse Intelligence Collection...
[+] Collecting CISA Alerts...
[+] Collected 15 CISA alerts
[+] Collecting CVE Data...
[+] Collected 25 CVEs
[+] Collecting Security News...
[+] Collected 10 articles from The Hacker News
[+] Collected 10 articles from Krebs on Security
[+] Collected 10 articles from BleepingComputer
[+] Collecting Malware Intelligence from OSINT...
[+] Querying MalwareBazaar for recent samples...
[+] Added 12 families from MalwareBazaar
[+] Collected 8 malware families from OSINT sources
[+] Collecting Threat Actor Intelligence from OSINT...
[+] Profiled 4 threat actors from OSINT sources

[+] Data collection complete!
[!] Total intelligence points gathered: 82
```

### Generate Visualizations
```python
# Create comprehensive threat landscape visualizations, though this is also run automatically with the notebook
create_threat_visualizations(analyzer)
```

### Export Reports
```python
# Generate executive-summary threat intelligence report
export_threat_report(analyzer)
```

## Intelligence Sources
### Government & Official Sources
- **CISA**: Cybersecurity and Infrastructure Security Agency alerts
- **NVD**: National Vulnerability Database CVE feeds
- **Government advisories**: Real-time security bulletins

### Security Industry Sources
- **The Hacker News**: Latest cybersecurity news and threat analysis
- **Krebs on Security**: In-depth security journalism and investigations
- **BleepingComputer**: Technical security news and malware analysis

### Threat Intelligence Platforms
- **MalwareBazaar**: Real-time malware sample intelligence from abuse.ch
- **CVE Database**: Latest vulnerability disclosures and patches

## Sample Intelligence Output

### Executive Dashboard
```
[!] THREATPULSE EXECUTIVE THREAT INTELLIGENCE DASHBOARD
================================================================================
[!] Generated: 2025-08-11 14:23:45 UTC
[!] Data Sources: 45 intelligence feeds processed

[+] THREAT LANDSCAPE OVERVIEW
----------------------------------------
• Government Alerts (CISA): 15
• Recent Vulnerabilities (CVE): 25
• Active Malware Families: 8
• Monitored Threat Actors: 4
• Security News Articles: 30

[+] TOP MALWARE THREATS
----------------------------------------
1. [HIGH] LockBit (Ransomware) - Prevalence: 12
2. [HIGH] Emotet (Banking Trojan) - Prevalence: 8
3. [MED] QBot (Banking Trojan) - Prevalence: 6

[+] TRENDING ATTACK TECHNIQUES
----------------------------------------
• Spear Phishing: 8 mentions
• Living Off The Land: 5 mentions
• Supply Chain Compromise: 3 mentions

[+] TARGETED VENDORS/TECHNOLOGIES
----------------------------------------
• Microsoft: 12 mentions
• Cisco: 6 mentions
• VMware: 4 mentions
```

## Professional Use Cases
### Cybersecurity Interview Preparation
Perfect demonstration tool for answering:
- "How do you stay current with threat intelligence?"
- "Walk me through your threat analysis process"
- "How would you brief executives on the current threat landscape?"

### Security Operations Center (SOC)
- **Daily Threat Briefings**: Automated intelligence collection
- **Incident Context**: Real-time threat actor and malware intelligence
- **Strategic Planning**: Trend analysis for security investments

### Threat Hunting
- **IOC Development**: Extract indicators from current threat intelligence
- **Actor Profiling**: Understand adversary TTPs and targeting
- **Campaign Tracking**: Monitor threat actor activity over time

### Risk Assessment
- **Industry Targeting**: Understand threats specific to your sector
- **Vendor Risk**: Track vulnerabilities in your technology stack
- **Executive Reporting**: Translate technical threats into business risk

## Advanced Configuration
### Adding Custom OSINT Sources
```python
# Extend security_feeds list in collect_security_news()
security_feeds = [
    "https://feeds.feedburner.com/TheHackersNews",
    "https://krebsonsecurity.com/feed/",
    "https://www.bleepingcomputer.com/feed/",
    "https://your-custom-feed.com/rss"  # Add custom sources
]
```

### Customizing Threat Intelligence Extraction
```python
# Modify threat patterns in extract_threat_intelligence()
malware_patterns = [
    'your-custom-malware',  # Add specific malware to track
    'emotet', 'trickbot'    # Existing patterns
]
```

### Export Customization
```python
# Generate reports for specific time periods or threat types
export_threat_report(analyzer, filename="weekly_threat_report.txt")
```

## Visualization Features

ThreatPulse generates six comprehensive visualizations:

1. **Malware Prevalence Analysis**: Bar chart showing active malware families by mention frequency
2. **Malware Type Distribution**: Pie chart categorizing malware by type (ransomware, banking trojans, etc.)
3. **Threat Actor Attribution**: Geographic/organizational attribution of active threat actors
4. **CISA Alert Severity**: Government alert classification and priority levels
5. **Trending Threat Intelligence**: Current hot topics in cybersecurity
6. **Intelligence Source Coverage**: Data collection metrics across all OSINT sources


## Security Considerations

### Data Handling
- All intelligence collection uses public OSINT sources
- No credential storage or authentication required
- Respects API rate limits and terms of service

### Privacy
- No personal data collection or storage
- Focuses on public threat intelligence only
- Suitable for corporate and educational use

## License

MIT License - See LICENSE file for details
