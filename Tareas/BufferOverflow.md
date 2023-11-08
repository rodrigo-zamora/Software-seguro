# BufferOverflow

## [Shellshock (CVE-2014-6271)](https://success.trendmicro.com/dcx/s/solution/1105233-trend-micro-products-and-the-shellshock-linux-bash-vulnerability-bash-bug-cve-2014-6271-and-cve?language=en_US&sfdcIFrameOrigin=null#:~:text=What%20is%20Shellshock%3F,certain%20specially%20crafted%20environment%20variables.)

In 2014, a vulnerability known as Shellshock was discovered in the Bash shell, a common Unix and Linux command-line interface. This vulnerability allowed attackers to execute arbitrary code by exploiting a buffer overflow in the way Bash processed environment variables. It had the potential to impact a wide range of systems and services.

## [EternalBlue (MS17-010)](https://nordvpn.com/blog/what-is-eternalblue/#:~:text=EternalBlue%20is%20a%20Microsoft%20exploit,Windows%20XP%20and%20Windows%207.)

EternalBlue is an exploit associated with the WannaCry ransomware attack in 2017. It targeted a buffer overflow vulnerability in the Microsoft Windows Server Message Block (SMB) protocol. By exploiting this vulnerability, the malware could spread rapidly across vulnerable Windows systems, causing widespread disruption.

## [BlueKeep (CVE-2019-0708)](https://msrc.microsoft.com/update-guide/en-US/vulnerability/CVE-2019-0708)

The BlueKeep vulnerability was discovered in the Remote Desktop Protocol (RDP) implementation in Windows. It allowed for remote code execution by exploiting a buffer overflow in the RDP service. If successfully exploited, an attacker could gain control over the affected system without user interaction.

## [Zerologon (CVE-2020-1472)](https://www.crowdstrike.com/blog/cve-2020-1472-zerologon-security-advisory/)

Zerologon is a vulnerability in the Netlogon authentication process in Windows, allowing attackers to perform a privilege escalation attack. It involved a buffer overflow in the cryptographic authentication mechanism, and if exploited, it could grant an attacker administrative control over a Windows domain controller.

## [MS08-067: Vulnerability in Server service could allow remote code execution](https://support.microsoft.com/en-us/topic/ms08-067-vulnerability-in-server-service-could-allow-remote-code-execution-ac7878fc-be69-7143-472d-2507a179cd15)

This is a remote code execution vulnerability. An attacker who successfully exploited this vulnerability could take complete control of an affected system remotely. On Microsoft Windows 2000-based, Windows XP-based, and Windows Server 2003-based systems, an attacker could exploit this vulnerability over RPC without authentication and could run arbitrary code. If an exploit attempt fails, this could also lead to a crash in Svchost.exe. If the crash in Svchost.exe occurs, the Server service will be affected. The Server service provides file, print, and named pipe sharing over the network.

The vulnerability is caused by the Server service, which does not correctly handle specially crafted RPC requests.