# OSINT Agent

Specialized Open Source Intelligence (OSINT) analyst for digital identity research, person investigation, and online community mapping. Works systematically using passive techniques, documenting every finding with confidence scores and sources.

## Core Capabilities

### Digital Identity Research
Comprehensive username enumeration across 400+ platforms using Sherlock and Maigret. Identifies social media presence, forum accounts, developer profiles, and online footprints. Cross-validates findings from multiple sources to build accurate identity maps.

### Email and Phone Investigation
Email breach checking via HIBP API, platform registration discovery with Holehe, and phone number analysis using PhoneInfoga. Identifies data leaks, account registrations, and associated digital identities.

### Photo and Metadata Analysis
EXIF metadata extraction from images including GPS coordinates, camera information, and timestamps. Geolocation analysis and visual intelligence gathering from publicly available photographs.

### Network and Domain Research
Passive DNS enumeration, WHOIS lookups, subdomain discovery, and IP address investigation. Maps digital infrastructure without active scanning or intrusive techniques.

### Czech-Specific Resources
Integration with Czech business registry (ARES, Justice.cz), property records (CUZK), and local databases for comprehensive domestic investigations.

## Workflow

The agent follows a structured six-phase OSINT methodology: SCOPE (define objectives and boundaries), SETUP (verify tools and install missing dependencies), PIVOT (identify seed identifiers), ENUM (systematic enumeration across all layers), CORRELATE (cross-validate and link findings), and REPORT (generate structured markdown documentation).

## Ethical Framework

Works exclusively with passive techniques that leave no traces in target systems. Refuses investigations of minors without exception. Requires clear justification for grey-area research. Includes ethical warnings in reports when handling sensitive data. Complies with GDPR considerations for EU persons.

## Automated Tooling

Automatically detects operating system (macOS/Linux) and installs missing OSINT tools including Sherlock, Maigret, Holehe, Socialscan, theHarvester, ExifTool, PhoneInfoga, Metagoofil, and supporting utilities. Provides installation commands for both apt and Homebrew package managers.

## Output Format

Generates comprehensive markdown reports with executive summary, seed identifiers, verified facts with confidence scores, inferred hypotheses, activity timeline, ethical considerations, recommended next steps, and complete tool usage documentation. Reports are classified as confidential and include source attribution for all findings.

## Usage

Load the agent configuration file `osint.md` in Augment Code CLI. The agent will guide you through the OSINT workflow, automatically install required tools, execute investigations systematically, and generate professional reports saved as `osint_report_{target}_{YYYYMMDD}.md`.

## Technical Approach

Combines web search (Google dorks), web fetch (direct API calls to public services), and CLI tools (specialized OSINT utilities) in a layered approach. Prioritizes passive reconnaissance over active scanning. Maintains strict separation between verified facts and inferred correlations. Documents confidence levels for all findings.

