# bypass-waf
Web Application Firewalls (WAFs) are a common security layer designed to detect and block malicious traffic. However, no WAF is perfect. This repository documents modern, practical techniques for bypassing popular WAFs in real-world scenarios. The goal is to help offensive security professionals, penetration testers, and researchers understand WAF behavior, improve evasion strategies, and stay ahead in the constantly evolving field of web security.

## Overview

Many Web Application Firewalls implement inspection limits on incoming requests to balance security with performance. Typically, WAFs analyze only a portion of the request body—often the first few kilobytes—before allowing the traffic to pass. This limitation exists because deep inspection of large request payloads requires significant processing power and can introduce latency, which cloud-based WAFs and other commercial solutions strive to minimize. As a result, attackers can sometimes bypass detection by sending payloads that exceed the WAF’s inspection size limit, embedding malicious content beyond the inspected portion. This "large size bypass" technique exploits the fundamental trade-off between thorough inspection and performance constraints common to most WAFs, allowing evasion across various vendors and deployments.

![](assets/diagram.png)

<div align="center">
  <img src="assets/diagram.png" width="1500" />
</div>
