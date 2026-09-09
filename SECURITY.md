# Security Policy

## Supported Versions

Security fixes are provided for the latest released firmware version.

| Version | Supported |
| --- | --- |
| Latest release | Yes |
| Development / testing / unreleased builds | No |
| Older releases | No |

Supported hardware includes [eBUS Adapter series](https://adapter.ebusd.eu) based on ESP32-C6, ESP32-C5, and ESP32-C3 running this firmware.

## Reporting a Vulnerability

Please report suspected security vulnerabilities privately. Do **not** open a public GitHub issue for vulnerabilities that could affect deployed devices.

Send a report to:

- Email: `security@ebusd.eu`
- GitHub private vulnerability reporting: `https://github.com/john30/ebusd-esp32/security/advisories/new`

Include, where possible:

- Affected firmware version and hardware variant
- Description of the issue and potential impact
- Steps to reproduce or a proof of concept
- Device logs
- Network configuration or prerequisites required to exploit the issue
- Suggested mitigation, if known
- Contact details for follow-up questions

Please submit reports in English.

## Response Process

1. We will acknowledge receipt within **5 business days**.
2. We will assess severity, affected versions, and potential impact.
3. We will investigate, develop, and test a fix or mitigation.
4. We will release a security advisory and firmware update when appropriate.

Please allow reasonable time for investigation and remediation before publicly disclosing a vulnerability. We aim to coordinate disclosure with the reporter.

## Scope

Security reports are especially relevant for issues involving:

- Unauthorized access
- Wi-Fi, network, HTTP, MQTT, or JSON API exposure
- Authentication or authorization bypass
- TLS, certificate, credential, or secret-handling weaknesses
- OTA firmware update integrity or downgrade attacks
- Vulnerabilities in bundled ESP-IDF components or third-party dependencies

## Out of Scope

The following are generally out of scope unless they demonstrate a practical security impact:

- Issues affecting unsupported firmware versions
- Issues caused by not configuring available security controls, such as web-access password or TLS certificates
- Issues requiring physical access to the device
- Denial-of-service attacks requiring sustained local network flooding
- Vulnerabilities in third-party services not operated by this project
- Vulnerabilities in systems, services, or software outside this firmware, including MQTT brokers, eBUS daemon, and third-party integrations
- Resource-exhaustion reports based solely on expected operation within the documented limits of the constrained ESP32-C series, including limited RAM, flash storage, CPU capacity, connection capacity, or message-buffer capacity
- Denial-of-service reports requiring traffic, request rates, message sizes, or connection counts beyond documented or reasonably expected local-network use, unless they cause persistent malfunction, unsafe behaviour, data exposure, or a security-control bypass
- Missing mitigations that cannot reasonably be implemented on the supported hardware due to its resource constraints, where no practical security impact is demonstrated

## Security Advisories

Confirmed vulnerabilities and available mitigations will be published through GitHub Security Advisories and/or the project release notes.

## Product Security Incident Handling

If an actively exploited vulnerability or a severe security incident is identified, we will assess notification obligations, notify affected users where appropriate, and follow applicable regulatory reporting requirements.
