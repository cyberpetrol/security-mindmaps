```d2
direction: right

cti: Cyber Threat Intelligence

cti_kb: Knowledge Base
cti_taxonomies: Taxonomies
cti_frameworks: Frameworks
cti_tools: Tools
cti_ctl: Cyber Threat Landscape
cti_tools_internal: Internals

cti -> cti_kb

# CTI Taxonomies
cti_kb -> cti_taxonomies
cti_taxonomies_tlp: |md
  [TLP](https://www.first.org/tlp/)
|
cti_taxonomies_pap: |md
  [PAP](https://github.com/MISP/misp-taxonomies/blob/master/PAP/machinetag.json)
|
cti_taxonomies_admiralty_code: |md
  [Admiralty Code](https://en.wikipedia.org/wiki/Admiralty_code)
|
cti_taxonomies_veris: |md
  [Veris](https://verisframework.org/)
|

cti_taxonomies -> cti_taxonomies_tlp
cti_taxonomies -> cti_taxonomies_pap
cti_taxonomies -> cti_taxonomies_admiralty_code
cti_taxonomies -> cti_taxonomies_veris

# CTI Frameworks
cti_frameworks_pyramid: |md
  [Pyramid of Pain](https://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html)
|
cti_frameworks_killchain: |md
  [Killchain](http://www.lockheedmartin.com/content/dam/lockheed/data/corporate/documents/LM-White-Paper-Intel-Driven-Defense.pdf)
|
cti_frameworks_diamond: |md
  [Diamond Model](https://apps.dtic.mil/sti/pdfs/ADA586960.pdf)
|
cti_frameworks_mitre: |md
  [Mitre Attck](https://attack.mitre.org/)
|
cti_kb -> cti_frameworks
cti_frameworks -> cti_frameworks_pyramid
cti_frameworks -> cti_frameworks_killchain
cti_frameworks -> cti_frameworks_diamond
cti_frameworks -> cti_frameworks_mitre

# CTI Standards
cti_standards: Standards
cti_standards_stix: |md
  [Stix 2.0](https://oasis-open.github.io/cti-documentation/stix/intro.html)
|
cti_standards_misp: |md
  [MISP JSON](https://www.misp-project.org/datamodels/)
|
cti_standards_openc2: |md
  [OpenC2](https://openc2.org/)
|
cti_kb -> cti_standards
cti_standards -> cti_standards_misp
cti_standards -> cti_standards_stix
cti_standards -> cti_standards_openc2

# Additional Resources
cti_additional_resources: Additional Resources
cti_additional_resources_awesome: |md
  [CTI Awesome List](https://github.com/hslatman/awesome-threat-intelligence)
|
cti_additional_resources_guide: |md
  [CTI Guide](https://cryptome.org/2015/09/cti-guide.pdf)
|

cti_kb -> cti_additional_resources
cti_additional_resources -> cti_additional_resources_awesome
cti_additional_resources -> cti_additional_resources_guide

# Tools
cti -> cti_tools
cti_tools -> cti_tools_internal
cti_tools_internal_edr: |md
  Endpoint Detection & Response
|
cti_tools_internal_siem: |md
  SIEM
|
cti_tools_internal_sandbox: |md
  Sandbox
|
cti_tools_internal_incidents: |md
  Incident Management Tool
|
cti_tools_internal -> cti_tools_internal_edr
cti_tools_internal -> cti_tools_internal_siem
cti_tools_internal -> cti_tools_internal_sandbox
cti_tools_internal -> cti_tools_internal_incidents

cti_tools_tip_misp: |md
  [MISP](https://www.misp-project.org/)
|
cti_tools_tip_opencti: |md
  [OpenCTI](https://docs.opencti.io/latest/)
|
cti_tools_tip_yeti: |md
  [Yeti](https://yeti-platform.github.io/)
|

cti_tools_tip: Threat Intel Platforms
cti_tools -> cti_tools_tip
cti_tools_tip -> cti_tools_tip_misp
cti_tools_tip -> cti_tools_tip_opencti
cti_tools_tip -> cti_tools_tip_yeti

# Tools News
cti_tools_news_feedly: |md
  [Feedly](https://feedly.com/)
|
cti_tools_news_ttrss: |md
  [TinyTinyRSS](https://tt-rss.org/)
|
cti_tools_news: News
cti_tools -> cti_tools_news
cti_tools_news -> cti_tools_news_feedly
cti_tools_news -> cti_tools_news_ttrss

# Tools Automation
cti_tools_automation: Automation
cti_tools -> cti_tools_automation
cti_tools_automation_intelmq: |md
  [intelmq](https://github.com/certtools/intelmq)
|
cti_tools_automation_cortex: |md
  [Cortex](https://github.com/TheHive-Project/Cortex)
|
cti_tools_automation -> cti_tools_automation_intelmq
cti_tools_automation -> cti_tools_automation_cortex

# Intel
# OSINT
cti_intel: Intel
cti -> cti_intel
cti_intel_osint_virustotal: |md
  [VirusTotal](https://virustotal.com)
|
cti_intel_osint_otx: |md
  [AlienVault OTX](https://otx.alienvault.com/)
|
cti_intel_osint_abuse: |md
  [Abuse.ch](https://abuse.ch/)
|
cti_intel_osint_malpedia: |md
  [Malpedia](https://malpedia.caad.fkie.fraunhofer.de/)
|
cti_intel_osint: Open Source Intelligence
cti_intel -> cti_intel_osint
cti_intel_osint -> cti_intel_osint_virustotal
cti_intel_osint -> cti_intel_osint_otx
cti_intel_osint -> cti_intel_osint_abuse
cti_intel_osint -> cti_intel_osint_malpedia

# CSINT
cti_intel_csint: Closed Source Intelligence
cti_intel -> cti_intel_csint
cti_intel_csint_cs: |md
  [Crowdstrike Intel](https://www.crowdstrike.com/products/threat-intelligence/)
|
cti_intel_csint_mandiant: |md
  [Mandiant Advantage](https://www.mandiant.com/advantage/threat-intelligence)
|
cti_intel_csint_ks: |md
  [Kaspersky](https://www.kaspersky.com/enterprise-security/threat-intelligence)
|
cti_intel_csint -> cti_intel_csint_cs
cti_intel_csint -> cti_intel_csint_mandiant
cti_intel_csint -> cti_intel_csint_ks

cti_threat_actors: Threat Actors
cti_intel -> cti_threat_actors
cti_threat_actors_etda: |md
  [Threat Group Cards](https://apt.etda.or.th/cgi-bin/aptgroups.cgi)
|
cti_threat_actors -> cti_threat_actors_etda
cti_threat_actors_misp: |md
  [MISP Threat Actors](https://github.com/MISP/misp-galaxy/blob/main/clusters/threat-actor.json)
|
cti_threat_actors -> cti_threat_actors_misp

# Cyber Threat Landscape
cti -> cti_ctl

cti_ctl_mandiant: |md
  [Mandiant](https://www.mandiant.com/resources/blog)
|
cti_ctl_unit42: |md
  [Unit42](https://unit42.paloaltonetworks.com/)
|
cti_ctl_securelist: |md
  [Securelist](https://securelist.com/)
|
cti_ctl_talos: |md
  [Talos](https://talosintelligence.com/)
|

cti_blogs: Blogs
cti_ctl -> cti_blogs
cti_blogs -> cti_ctl_mandiant
cti_blogs -> cti_ctl_unit42
cti_blogs -> cti_ctl_securelist
cti_blogs -> cti_ctl_talos

cti_news: News Aggregators
cti_news_bleeping: |md
  [BleepingComputer](https://www.bleepingcomputer.com/)
|
cti_news_hackernews: |md
  [TheHackerNews](https://thehackernews.com/)
|
cti_news_securityaffairs: |md
  [Security Affairs](https://securityaffairs.com/)
|
cti_ctl -> cti_news
cti_news -> cti_news_bleeping
cti_news -> cti_news_hackernews
cti_news -> cti_news_securityaffairs

cti_ctl_vulnerabilities: Vulnerabilities
cti_ctl -> cti_ctl_vulnerabilities
cti_news_nvd: |md
  [NVD](https://nvd.nist.gov/)
|
cti_news_kev: |md
  [CISA KEV](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)
|
cti_ctl_vulnerabilities -> cti_news_nvd
cti_ctl_vulnerabilities -> cti_news_kev

# Communities
cti_communities: Communities
cti -> cti_communities

cti_communities_first: |md
  [FIRST](https://first.org)
|
cti_communities_enisa: |md
  [Enisa](https://www.enisa.europa.eu/)
|
cti_communities_isacs: |md
  ISACs
|
cti_communities_local: |md
  Local Sharing Groups
|
cti_communities -> cti_communities_first
cti_communities -> cti_communities_enisa
cti_communities -> cti_communities_isacs
cti_communities -> cti_communities_local

```