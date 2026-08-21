# 3mtt-wifi-security-assessment
Capstone project
# 3MTT Cybersecurity Capstone Project

## Security Assessment of an MTN ZLT 4G MiFi Router

### Project Overview

This project was completed as part of the **3MTT Cybersecurity Program Capstone Project**.

The project involved a security assessment of an authorized MTN ZLT 4G MiFi router to evaluate its network exposure, wireless security configuration, traffic behavior, and web-based administrative interface.

The assessment was performed in a controlled environment using industry-standard cybersecurity tools.

## Objectives

The primary objectives of this assessment were to:

* Identify exposed network services.
* Analyze network traffic between the host and the MiFi router.
* Review the router's wireless and administrative security configuration.
* Assess the security of the router's web management interface.
* Identify potential security weaknesses.
* Provide practical security-hardening recommendations.


## Scope

### Target

**Device:** MTN ZLT 4G MiFi Router

**Assessment Interface:** Local router management interface

**Environment:** Authorized personal/lab environment (using kali Linux inside virtualbox0

The assessment was limited to the router and devices within the authorized test environment.

## Methodology

The assessment followed a structured security-testing process:

### 1. Network Reconnaissance

**Tool:** Nmap

Nmap was used to identify accessible ports and services associated with the target environment.

The results were reviewed to determine whether unnecessary or potentially risky services were exposed.

### 2. Network Traffic Analysis

**Tool:** Wireshark

Wireshark was used on the host machine to observe and analyze traffic exchanged between the host and the MiFi router.

The purpose was to understand:

* Network communication patterns
* Protocols in use
* DNS activity
* ARP activity
* TCP connections
* HTTP communication where applicable

### 3. Wireless Security Review

The router's wireless configuration was manually reviewed.

The following configuration was observed:

* **Security mode:** WPA2-PSK
* **Encryption:** AES
* **Default administrator password:** Changed
* **Firmware version:** 3.06.05
* **Connected users/devices during assessment:** 2
* **WPS:** No WPS functionality was identified on the device/interface

### 4. Web Interface Assessment

**Tool:** OWASP ZAP

OWASP ZAP was configured as a local proxy and used to assess the router's web-based management interface.

The assessment focused on identifying issues such as:

* Missing HTTP security headers
* Information disclosure
* Outdated client-side components
* Other passive web-security observations

## Tools Used

| Tool      | Purpose                                        |
| --------- | ---------------------------------------------- |
| Nmap      | Network reconnaissance and service enumeration |
| Wireshark | Network traffic analysis                       |
| OWASP ZAP | Web application security assessment            |


## Key Findings

The assessment identified areas that could be improved in the router's security posture, particularly around the web management interface.

Examples of observations included:

* Missing Content Security Policy (CSP)
* Missing security-related HTTP headers
* Use of an outdated JavaScript library
* Information/timestamp disclosure
* Other low-risk web-interface observations

The findings are documented in greater detail in the full assessment report.

## Security Controls Observed

Several positive security controls were also identified:

* WPA2-PSK with AES encryption was enabled.
* The default administrator password had been changed.
* No WPS functionality was identified.
* The router firmware version was documented as 3.06.05.

These controls reduce some common risks associated with poorly configured wireless routers.

## Recommendations

Based on the assessment, the following recommendations are proposed:

1. Keep the router firmware updated where vendor updates are available.
2. Continue using strong wireless authentication and encryption.
3. Use a strong, unique administrator password.
4. Review connected devices periodically.
5. Disable unnecessary services where the router provides that option.
6. Improve HTTP security headers on the administrative interface.
7. Replace outdated JavaScript libraries where technically feasible.
8. Minimize unnecessary information disclosure from the management interface.
9. Restrict administrative access to trusted devices and networks.
10. Avoid exposing the router's management interface directly to the public Internet.

## Deliverables

The complete project report is available in:

report/3MTT_Capstone_Security_Assessment.pdf

The repository contains the assessment methodology, supporting evidence, screenshots, findings, and recommendations.

## Ethical and Legal Considerations

This assessment was conducted only against equipment and systems within the authorized test environment.

No unauthorized access to third-party systems was attempted.

The techniques and tools documented in this project are presented for cybersecurity education, assessment, and defensive security purposes.


## Conclusion

The assessment demonstrated the practical application of network reconnaissance, packet analysis, and web security testing against a consumer networking device.

The MiFi demonstrated several positive baseline security controls, including WPA2-PSK/AES wireless encryption and a changed administrator password. However, observations from the web management interface indicate opportunities for further hardening.

Implementing the recommended controls would improve the overall security posture of the device and reduce unnecessary exposure.


## Author

Author: Ismaeel Ekundayo
Program: 3MTT Cybersecurity
Project: Wi-Fi Security Assessment
Assessment Target: MTN ZLT M305 Pro MiFi
