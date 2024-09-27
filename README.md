
#**SIH-2024**
**Smart India Hackathon 2024**




Team **desiCoder's**

#Team Members-
Mohd Wasiullah

Adil Ahmad

Arbaz Ali

Umme Aiman Patel

Shaikh Tabish

Ahmad Khan

Project Name:
Domain hosting details.

Problem Statement- 1784
On searching many suspicious websites on whois, their hosting appears to be on cloud flare, but after sending mail to cloud flare, say that the said website uses one of their services like SSL certificate etc. and they do not have the hosting of the website, due to which correct information about the suspicious website cannot be obtained. Challenges: Correct information from suspicious websites is not available. Expected Solution: A mechanism should be developed that can provide accurate information about suspicious websites along with their actual hosting.

## Features

- **DNS Enumeration**: Retrieves A, MX, CNAME, NS, and TXT records.
- **SSL Certificate Analysis**: Extracts SSL certificate details.
- **Reverse IP Lookup**: Identifies other domains hosted on the same IP using Shodan.
- **SecurityTrails Integration**: Fetches subdomains associated with the domain.
- **Root Domain Extraction**: Extracts the root domain from a given URL.

# Usage Guide

## Introduction

The "Domain Hosting Details" tool helps you uncover the actual hosting details of websites, even if they use services like Cloudflare to mask their real hosting providers.

## Prerequisites

- Python 3.6 or higher
- Shodan API Key
- SecurityTrails API Key

## Steps to Use the Tool

### 1. DNS Enumeration

The tool retrieves various DNS records for the specified domain, including:

- **A Records**: IP addresses.
- **MX Records**: Mail servers.
- **CNAME Records**: Canonical names.
- **NS Records**: Name servers.
- **TXT Records**: Text records.

### 2. SSL Certificate Analysis

The tool connects to the domain's server over HTTPS to extract SSL certificate details, such as:

- **Subject**: The entity the certificate is issued to.
- **Issuer**: The certificate authority that issued the certificate.
- **Validity Period**: Start and end dates of the certificate.

### 3. Reverse IP Lookup

Using the first available A record IP, the tool performs a reverse IP lookup via Shodan to identify other domains hosted on the same IP address.

### 4. SecurityTrails Integration

The tool fetches subdomains associated with the root domain using the SecurityTrails API.

