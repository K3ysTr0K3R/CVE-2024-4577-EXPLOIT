# CVE-2024-4577 - PHP CGI Argument Injection Remote Code Execution (RCE)

In certain versions of PHP (8.1.* before 8.1.29, 8.2.* before 8.2.20, and 8.3.* before 8.3.8), a critical vulnerability exists when using PHP with Apache and PHP-CGI on Windows. If the system is configured to use specific code pages, Windows' "Best-Fit" behavior may replace characters in command lines given to Win32 API functions. This behavior can cause the PHP-CGI module to misinterpret these characters as PHP options, potentially allowing an attacker to pass options to the PHP binary. This could lead to the exposure of script source code or the execution of arbitrary PHP code on the server.

## Proof of Concept (PoC)

I have developed a proof of concept (PoC) exploit for this vulnerability to demonstrate its potential impact.

**Disclaimer:** This PoC is provided for educational purposes and to aid in the development of security measures. It should not be used for malicious purposes. Use it responsibly and only on systems where you have explicit permission to do so.
