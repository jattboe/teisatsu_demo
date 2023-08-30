# Teisatsu

Teisatsu is an advanced cybersecurity tool designed to streamline the process of subdomain and endpoint analysis, catering specifically to vulnerability assessment and penetration testing. It is an essential toolkit for bug bounty hunters, security researchers, and other cybersecurity professionals.

## Overview

Teisatsu performs a comprehensive scan by gathering subdomains and endpoints from 35 different sources. These sources are systematically divided into four distinct buckets, allowing for efficient and methodical scanning.

## Key Components
    
- Subdomain Gathering & DNS Bruteforce Module: Teisatsu simultaneously passes the subdomains to a custom-written DNS bruteforce module, using Golang channels. This module checks the validity of subdomains, saving them in a MongoDB database.

 - Vulnerability Scanner: Upon identifying valid subdomains, they are passed to a vulnerability scanner. This scanner looks for common vulnerabilities such as subdomain takeover, Cross-Site Scripting (XSS), Cross-Origin Resource Sharing (CORS), etc.

- API Server: Teisatsu comes with an API server that allows users to query saved data from MongoDB, providing robust access to valuable intelligence.

- User Dashboard: A separate user dashboard server has been created using Flask, offering a user-friendly interface to interact with Teisatsu's features.

 - Remote Control via Discord/Telegram Bot: Users can initiate scans remotely from any device through a dedicated Discord/Telegram bot. This bot also provides real-time notifications if any vulnerabilities are found.

 - Additional Features: Teisatsu includes several other functionalities that have proven instrumental in finding vulnerabilities in bug bounty targets.

## Why Teisatsu?

Teisatsu's seamless integration of various modules and features ensures a versatile and powerful tool for modern security needs. Its efficiency, user-centric design, and robust performance have made it a popular choice for professionals seeking to enhance their vulnerability assessment processes.

## Installation

```bash
go get github.com/jattboe/teisatsu
```

## Usage


```bash
❯ teisatsu -h
```

```
Usage of teisatsu:
  -active
        Active SubDomain Enumeration.
  -bot
        Start Discord Bot.
  -config string
        Configuration file for API Keys.
  -domain string
        Domain for SubEnum.
  -eps
        Look For Only EndPoints.
  -favurl string
        Favicon URL for getting FavHASH.
  -lns string
        Custom Local NameServer.
  -mobi
        Mobi Means Mobile UserAgent is Used in Mapping.
  -nmap string
        Start Nmap Scan.
  -ns string
        Custom NameServer.
  -reader
        MoongoDb Reader.
  -scan string
        Scan Comma Seperated Domains for SubEnum.
  -server
        Start Api Server.
  -sources string
        Comma seprated values of sources.
  -spider
        Spider means Stdin from iamspider.
  -subs
        Look For Only SubDomains.
  -v    Verbose Scan to see log Info live.
```

## Contributing

Teisatsu is currently in development phase and is actively being refined to ensure it meets the highest standards of quality and effectiveness. Once the project reaches a stage where it aligns with the envisioned use case and fulfills the necessary criteria, it will be made available as an open-source resource. Further announcements regarding the open-source release will be shared in due course. Thank you for your interest and anticipation in Teisatsu.

