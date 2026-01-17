# Living Threat Intelligence

> **Building Self-Updating Threat Intelligence Systems: From Theory to Automated Security Operations**

A comprehensive technical guide teaching security engineers to build automated threat intelligence platforms from scratch. By the end, you'll have deployed a live, self-updating threat intel system (like [KrebsOnSecurity](https://krebsonsecurity.com)) running at **zero cost**.

🔗 **Live Deployment**: [intel.hsed.dev](https://intel.hsed.dev) *(coming soon)*  
📚 **Read Online**: [Book Chapters](chapters/)  
💻 **Reference Implementation**: [ThreatPulse](implementation/)

---

## What You'll Build

**ThreatPulse** - A production-grade threat intelligence platform that:
- ✅ Aggregates data from 10+ free sources (CISA, NVD, abuse.ch, vendor feeds)
- ✅ Collects threat data daily using GitHub Actions (serverless)
- ✅ Generates AI-powered weekly summaries using Claude
- ✅ Extracts IOCs and generates detection rules automatically
- ✅ Publishes to public dashboard with REST API
- ✅ Costs **$0/month** to operate (free tier optimized)

---

## Who This Is For

**Target Audience:**
- Security engineers (3+ years experience) wanting to build detection platforms
- SOC analysts transitioning to security engineering roles  
- Platform architects designing threat intelligence systems
- DevSecOps professionals automating security operations

**Prerequisites:**
- Python programming (intermediate level)
- Basic understanding of REST APIs and HTTP
- Familiarity with Git/GitHub
- Knowledge of common attack vectors (CVEs, malware, TTPs)

**Not required:**
- Prior threat intelligence experience
- Machine learning knowledge
- Cloud platform expertise
- Budget for commercial threat intel platforms

---

## Book Structure

### **Part 1: Foundations** (Chapters 1-3)
Understanding threat intelligence landscape, taxonomy, and open source intelligence gathering.

### **Part 2: Technical Foundation** (Chapters 4-6)  
Data formats (STIX/TAXII), API integrations, data processing and normalization.

### **Part 3: Intelligence Production** (Chapters 7-9)
Automated categorization, AI-powered summarization, IOC extraction and weaponization.

### **Part 4: Automation & Deployment** (Chapters 10-12)
GitHub Actions automation, storage strategies, deploying ThreatPulse MVP.

### **Part 5: Advanced Features** (Chapters 13-15)
Public dashboards, REST APIs, threat hunting integration.

### **Part 6: Scaling & Production** (Chapters 16-18)
Performance optimization, measuring intelligence value, community building.

**Total:** 18 chapters, ~32 hours of content, 100% hands-on

📖 **[View Complete Index](BOOK_INDEX.yaml)**

---

## Quick Start

### Reading the Book
```bash
# Clone the repository
git clone https://github.com/raghavpoonia/living-threat-intel.git
cd living-threat-intel

# Start reading
cat chapters/01-state-of-threat-intel.md
```

### Building ThreatPulse
Each chapter includes practical exercises. By Chapter 12, you'll have a fully automated platform:
```bash
# Chapter 5: Build your first collector
python implementation/collectors/cisa_collector.py

# Chapter 10: Deploy automation
git push  # GitHub Actions handles the rest

# Chapter 13: Launch public dashboard
# Visit your-username.github.io/living-threat-intel
```

---

## Repository Structure
```
living-threat-intel/
├── README.md                      # You are here
├── BOOK_INDEX.yaml               # Complete book outline with metadata
├── LICENSE                        # MIT License
│
├── chapters/                      # Book content (Markdown)
│   ├── 01-state-of-threat-intel.md
│   ├── 02-threat-intelligence-taxonomy.md
│   ├── 03-osint-foundations.md
│   ├── 04-data-formats-and-standards.md
│   └── ...
│
├── implementation/                # ThreatPulse reference implementation
│   ├── collectors/               # Data collection scripts
│   │   ├── cisa_collector.py
│   │   ├── nvd_collector.py
│   │   └── ...
│   ├── processors/               # Data processing pipelines
│   │   ├── deduplicator.py
│   │   ├── enrichment.py
│   │   └── categorizer.py
│   ├── analyzers/                # AI-powered analysis
│   │   └── summarizer.py
│   ├── generators/               # Detection rule generators
│   │   ├── yara_generator.py
│   │   └── sigma_generator.py
│   └── utils/                    # Shared utilities
│       └── helpers.py
│
├── deployment/                    # Live threat intel platform
│   ├── .github/
│   │   └── workflows/
│   │       ├── daily-collection.yml
│   │       └── weekly-summary.yml
│   ├── data/
│   │   ├── daily/               # Daily threat collections (YAML)
│   │   └── weekly/              # Weekly AI summaries (YAML)
│   └── site/                    # Static site generator config
│       └── config.yaml
│
├── exercises/                     # Chapter exercises and starter code
│   ├── chapter-01/
│   ├── chapter-02/
│   └── ...
│
├── appendices/                    # Reference materials
│   ├── A-threat-intel-sources.md
│   ├── B-api-integration-examples.md
│   ├── C-detection-rule-templates.md
│   ├── D-cost-optimization.md
│   ├── E-compliance-legal.md
│   └── F-interview-preparation.md
│
└── samples/                       # Sample data and examples
    ├── cves/
    ├── iocs/
    └── reports/
```

---

## Learning Path

### **Beginner Path** (8 weeks, 4 hours/week)
Follow chapters sequentially. Complete all exercises. Deploy ThreatPulse by Week 4.

### **Intermediate Path** (4 weeks, 8 hours/week)  
Skim Chapters 1-3. Focus on implementation (Chapters 4-12). Deploy and scale.

### **Advanced Path** (2 weeks, 16 hours/week)
Jump to Chapter 5. Build as you read. Customize for your organization.

---

## Project Milestones

- [ ] **Week 1**: Chapters 1-3 complete, threat feed inventory built
- [ ] **Week 2**: Chapters 4-6 complete, first API collector working
- [ ] **Week 3**: Chapters 7-9 complete, AI summarization integrated
- [ ] **Week 4**: Chapters 10-12 complete, **ThreatPulse automated & live** 🎉
- [ ] **Week 5-8**: Advanced features, public launch, community engagement

---

## Tech Stack

**Core Technologies:**
- **Python 3.11+** - Primary language
- **GitHub Actions** - Serverless automation
- **Claude AI** - Weekly summarization (Anthropic API)
- **Hugo/Jekyll** - Static site generation
- **YAML** - Data storage format

**Data Sources (All Free):**
- CISA KEV Catalog
- NVD (National Vulnerability Database)
- abuse.ch (URLhaus, MalwareBazaar)
- AlienVault OTX
- VirusTotal (free tier)
- GitHub Security Advisories
- Vendor security blogs (RSS)

**Optional (for scaling):**
- AWS Lambda + S3 (free tier)
- PostgreSQL / MongoDB
- Redis (caching)

---

## Contributing

This is both a book and a working platform. Contributions welcome:

- 📝 **Typos/corrections**: Open an issue or PR
- 💡 **New chapters/sections**: Discuss in issues first
- 🔧 **Code improvements**: PRs to `implementation/`
- 🌍 **Translations**: Contact maintainer
- 📊 **Data sources**: Add to appendices

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## Use Cases

### **For Security Teams**
- Build internal threat intelligence platform
- Automate morning security briefings
- Feed IOCs into SIEM/EDR
- Track vendor vulnerabilities

### **For Job Seekers**
- Portfolio project for security engineering roles
- Interview talking points (live deployment)
- Demonstrates automation + AI integration skills
- Shows initiative beyond certifications

### **For Researchers**
- Historical threat data repository
- Academic research on threat trends
- Malware family analysis
- Attack technique evolution studies

### **For Students**
- Learn practical threat intelligence
- Understand security operations workflows
- Build production-grade projects
- Contribute to open source security

---

## Success Stories

> ...  
> — Security Engineer, ...

*(Add your story: open a PR or issue)*

---

## Roadmap

### **v1.0** (Current)
- [x] Complete book outline (18 chapters)
- [ ] Chapters 1-3 (Foundations)
- [ ] Chapters 4-6 (Technical Foundation)
- [ ] Chapters 7-9 (Intelligence Production)
- [ ] Chapters 10-12 (Automation & Deployment)
- [ ] ThreatPulse MVP automated

### **v1.1** (Q2 2025)
- [ ] Chapters 13-15 (Advanced Features)
- [ ] Public dashboard at intel.hsed.dev
- [ ] REST API deployment
- [ ] Community contributions

### **v2.0** (Q3 2025)
- [ ] Chapters 16-18 (Scaling & Production)
- [ ] Multi-language support
- [ ] Video companion series
- [ ] Conference workshop materials

---

## Acknowledgments

**Built with expertise from:**
- 13+ years in security intelligence and platform architecture
- Lessons from managing systems at IBM Cloud
- Real-world threat data from 2024-2025 breach landscape
- Community feedback from security practitioners

**Special thanks to:**
- CISA for maintaining the KEV catalog
- NVD team for vulnerability data
- abuse.ch for malware intelligence
- Anthropic for Claude API
- Security community for continuous knowledge sharing

---

## License

**Book Content**: [Creative Commons BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)  
**Code (implementation/)**: [MIT License](LICENSE)

Free to use, modify, and share. Commercial use of book content requires permission.

---

## Connect

**Author**: Raghav Dinesh  
**Website**: [coming soon..](https://hsed.dev)  
**LinkedIn**: [linkedin.com/in/raghavpoonia](https://linkedin.com/in/raghavdinesh)  
**GitHub**: [@raghavpoonia](https://github.com/raghavpoonia)  

**Other Projects:**
- [HSED Cryptographic Framework](https://github.com/raghavpoonia/hsed)
- [AI Security Mastery](https://github.com/raghavpoonia/ai-security-mastery)
- [Automated Threat Intel Feed](https://github.com/raghavpoonia/threat-intel-feed)

---

## Status

📅 **Started**: January 2025  
📊 **Progress**: Chapters 1-3 in progress  
🚀 **First Deployment**: Targeting Feb 2025  
⭐ **Star this repo** to follow along!

---

**Ready to build your own threat intelligence platform? Start with [Chapter 1](chapters/01-state-of-threat-intel.md) →**
```

---

### **5. LICENSE**
```
MIT License

Copyright (c) 2025 Raghav Dinesh

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

BOOK CONTENT LICENSE

The book content (all Markdown files in chapters/ and appendices/) is licensed
under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International.

You are free to:
- Share: copy and redistribute the material
- Adapt: remix, transform, and build upon the material

Under the following terms:
- Attribution: Give appropriate credit
- NonCommercial: Not for commercial purposes without permission
- ShareAlike: Distribute contributions under same license

For commercial use of book content, contact: raghav@hsed.dev
