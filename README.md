
# Network Merger and Implementation Plan

## Objective
The Network Merger and Implementation Plan project focused on integrating two separate corporate networks into a unified, secure, and efficient infrastructure. The goal was to design a detailed implementation plan that ensures minimal downtime, mitigates security risks, and optimizes network performance. This project provided hands-on experience with network architecture, risk assessment, and strategic planning for enterprise-scale network mergers.

## Skills Learned
- Designing scalable and secure network architectures.
- Conducting network assessments and identifying potential vulnerabilities.
- Planning network integration with minimal service disruption.
- Understanding routing, switching, VLAN segmentation, and firewall rules in a merger context.
- Risk analysis, mitigation planning, and creating comprehensive implementation documentation.
- Collaboration and communication with stakeholders to align technical and business requirements.

### Tools Used
- Network simulation and diagram tools (e.g., Cisco Packet Tracer, Microsoft Visio).
- Network monitoring and analysis tools (e.g., Wireshark, SolarWinds).
- Documentation tools (e.g., Microsoft Word, Excel, or Confluence) for implementation planning.
- Security and compliance checklists to identify risks and ensure best practices.

   Ref 1: Network Diagram
-  Documented the existing network architectures of both organizations.
-  Identified overlapping IP ranges, hardware configurations, and potential security gaps.
<img width="663" height="485" alt="Screenshot 2025-10-17 at 3 16 06 AM" src="https://github.com/user-attachments/assets/7e495a12-4703-4958-92f0-ae5d08472884" /> <img width="533" height="576" alt="Screenshot 2025-10-17 at 3 17 03 AM" src="https://github.com/user-attachments/assets/60ef5325-7567-497b-ad08-1cea0c99e1ff" />

## Steps

`A. Current Network Security and Infrastructure Problems`

    Company A, a global financial organization, has recently acquired Company B, a small technology firm that provides specialized software to medical providers and, as a payment option, accepts credit cards. As a cybersecurity professional at Company A, the task is to evaluate both companies' existing network topologies, identify known vulnerabilities, assess the likelihood of potential risks, and recommend a secure, compliant, and hybrid network architecture that meets these requirements. 

    This report includes assessments of current technological needs of the merged organizations, considering budgetary restraints and risks targeting the merged network. The risk analysis provided by both companies, along with outside sources, supported the network topology proposal included in this report. The report considers security compliance and regulatory obligations that directly impact both companies' business objectives, such as PCI DSS and HIPAA. The aim is to enhance efficiency and implement multiple layers of defense to strengthen overall security.

    Each company is facing network security and infrastructure problems. The issues discussed in this report pose significant compliance and security risks, as high-priority concerns have been identified and need to be addressed prior to the merger.

    Company A's internal risk analysis reveals network security and infrastructure issues that may interfere with the integration with Company B. The two key issues are, first, the presence of multiple open ports, and second, the use of weak-character passwords for all users. Open ports expose the organization's surface to attack, allowing malicious unauthorized access through services such as RDP or FTP. Weak password policies compromise account security, which increases the risk of brute-force attacks. 

    Lack of proper account management and the current use of end-of-life equipment are among the infrastructure problems detailed in the internal risk analysis. Company A emphasizes that "user accounts no longer required are not removed" and that "all users have local administrative privileges. Such could lead to insider-threat risks and violation of least privilege principles. There are legacy systems within Company A's inventory, such as Windows 7 laptops and Windows Server 2012. These systems are outdated and no longer receive vendor support, such as updates and patches, which could expose the company to security vulnerabilities and attacks. To combat these issues, Company A needs to reassess and strengthen its account management and access policies while leveraging cloud-based solutions to replace its legacy systems, if applicable. 

    Company B's vulnerability report identified and detailed the network and infrastructure problems within its organization. Among the various problems, the two primary network security issues are the publicly accessible database interface and its associated weak security, as well as the remote-code execution vulnerabilities within different services. The port accessible from the internet is the PostgreSQL administrative port, and it has weak passwords, which expose sensitive data to external threats. This database contains sensitive data, including financial and medical information, making this issue more critical. The Apache Tomcat AJP and Java RMI are identified as exploitable services and would likely invite hackers to execute unexpected or malicious code remotely. Availability and confidentiality can be affected due to the potential system downtime or data loss that this issue may cause. 

    Company B's infrastructure shortcomings include the use of end-of-life operating systems, such as Windows XP and 7, as well as an underdeveloped device management system and inadequate security governance. End-of-life systems can be easy targets for exploitation attacks due to the vendor's lack of patches and update support. Another problem within Company B is poor usage of mobile devices and limited documentation of its network inventory. These gaps could potentially hinder the integration with Company A's more mature environment. Implementing best practices and enforcing better policies can create a smoother merger between the two organizations. 

`B.  Vulnerability Analysis
1. Describe two existing vulnerabilities for each company.
2. Explain the impact, risk, and likelihood associated with each described vulnerability from part B1 as it relates to each company.`

    Let us delve deeper into the known vulnerabilities and discuss the impact, risk, and likelihood associated with each respective vulnerability. To start with, Company A's open ports for FTP and RDP are usually targets for brute-force and other malware attacks. There should be policies in place, such as using VPN configurations or firewalls, to ensure security. Unauthorized remote access and data exfiltration are potential consequences of having these open ports, which can result in regulatory penalties under the PCI DSS and damage the organization's reputation. According to the risk analysis conducted by Company A, this vulnerability was scored as high risk and had a high likelihood of vulnerability. Due to these confirmed, open, and easily exploitable ports, critical and internal systems are prone to exploitation. Such vulnerabilities threaten the confidentiality and integrity of customer information, as well as the impact on availability if attackers succeed in disrupting services.

    The second vulnerability is the weak eight-character password policy. Here, the impact can vary. From credential reuse, account compromise, to privilege escalation, weak password policies are a gateway to financial losses as well as noncompliance with regulations such as the PCI DSS. The risk and likelihood of this, seemingly simple vulnerability, are both high, affecting all users. There is no complexity in the credential requirements or multi-factor authentication enforcement in place, leaving Company A susceptible to account takeover, brute-force, and ransomware attacks. Chipping away at the CIA triad, this vulnerability also undermines the confidentiality and integrity of customer user accounts. The priority will be to focus on strengthening authentication policies and implementing complex password requirements. 

    Its end-of-life operating systems and unpatched remote-execution limitations are Company B's primary weak points. The few impacts caused by these flaws include service disruptions, potential ransomware, and remote code execution, which affect the availability and confidentiality of the security principles. Additionally, these types of attacks or disruptions may lead to violations of HIPAA and PCI DSS regulations by exposing sensitive payment and health data. The likelihood of this is moderate to high, making early detection and remediation crucial due to the existence of public exploits. In other words, when older systems remain online, it increases the likelihood of their compromise using public exploits. To mitigate this weakness, replacing systems or patching them at the very least should be prioritized. This measure will ensure a smooth merger between the organizations' networks. 

    Finally, the second vulnerability identified by Company B is the publicly available PostgreSQL administration interface, along with weak passwords. Graded with a high likelihood of compromise, this weakness allows direct access to sensitive systems. Its weak credential requirements, paired with its internet-facing feature, will make gaining access effortless. This risk can have numerous impacts, including database takeover, which may result in the exposure of PII and payment data, thereby violating both HIPAA and PCI DSS. Business impacts, including financial loss, reputational damage, data breaches, or service downtime, will compromise the confidentiality, integrity, and availability of the CIA triad. To ensure the likelihood of this vulnerability remains low, it is necessary to implement strong authentication requirements and restrict database access, possibly through network segmentation.

    `C.	Create a network topology diagram with details of the proposed merged network requirements.`

<img width="975" height="696" alt="image" src="https://github.com/user-attachments/assets/37996750-e02e-4d68-a9b5-6cd7d85f0ef0" />

`E.  Explain the rationale for adding, deleting, or repurposing network components in the newly merged network topology diagram, including details of how each component addresses budgetary constraints.`

  
    The security team focused on the logical consolidation of the merger because the companies were to remain in their respective physical locations. In other words, the new topology added components that adhered to this logical consolidation. For example, the site-to-site VPN, standardized Wi-Fi, and centralized DMZ created the capacity for the merged network to allow unified authentication and secure connectivity and access to off-site, shared servers and applications for users of both companies. These amendments did not require significant hardware additions or purchases, as the new topology utilized existing components such as routers and firewalls. 

      The Azure cloud services integrated into the new topology include Azure VPN, firewall, and Azure Active Directory. These services, combined, will provide centralized security and unified identity management, strengthen the company's overall security posture while improving scalability and reducing hardware costs and maintenance. These additions ensure efficient allocation of the $50,000 budget. The total estimated cost is $ 1,443. Azure Entra ID costs approximately $6 per user per month, and VpnGw1 costs $152 per month.

      To compensate for redundancy, the new design removed some components. For instance, physical firewalls and external servers were strategically removed from the design, cutting the cost of hardware, administration, maintenance, and licensing.

      Firewalls and switches were among the components repurposed to unify the network of the merged companies, serving as segmentation tools for their respective physical locations and centralizing service hosts.


`F.  Explain two secure network design principles that are used in the proposed network topology diagram.`
The two network design principles used in the proposed network topology diagram were defense-in-depth and network segmentation. 

    Through both internal and external firewalls, as well as secure cloud connections, the new topology achieves a defense-in-depth approach. The firewalls separated traffic to the DMZ from the internet, and then internal firewalls filtered the traffic from the DMZ to the internal network. Azure isolates its resources through its secure connections. Defense-in-depth is a core network principle that provides any organization with the confidence that, if one layer fails, additional layers of security are in place. Advanced persistent threats and denial-of-service attacks are primary examples of the types of attacks a defense-in-depth solution can defend against.

    Additionally, this solution enhances overall security by creating a layered defense against attackers attempting to access the resources they aim to compromise. Attackers come with the time and passion to compromise data and systems and will work hard to bypass checkpoints. Strong, multiple-layer defenses will deter their efforts. Failing to prepare these defenses, however, will make the organization susceptible to repeated attacks.

    The proposed topology incorporates network segmentation for user workstation networks, server VLANs, wireless networks, DMZ, and cloud environment. Segmentation is a principle that allows zones to operate independently, thereby preventing threats by enforcing the concept of containment for regular operations. For instance, if a user workstation becomes compromised, attackers will not be able to access sensitive data from other operational zones, giving IT professionals time to intercept the attack before it spreads to other areas of the network. Combined with the defense-in-depth solution, this principle enhances security by protecting critical servers with internal firewalls and allowing only necessary traffic to flow between segmented zones.
 

  
`G.  Explain how the proposed merged network topology diagram addresses two regulatory compliance requirements that are relevant to the newly merged company, including the following in your explanation:
•   the name of the regulatory compliance requirement
•   why the regulatory requirement is relevant to the newly merged company
•   how the proposed merged network topology diagram meets the regulatory requirement`

    One of the regulatory compliance requirements that is relevant to the merged topology diagram is PCI DSS. Company A operates in the financial industry, handling customer billing and online transactions. The merged topology retains most of the pre-merger infrastructure of both companies, including web services, application servers, data storage, and e-commerce functions, which are likely to include customer billing information. Given this, the merged network must ensure compliance with the PCI DSS. The merged network meets these regulatory requirements through controls such as network segmentation, firewalls, and access control, as well as secure remote access via VPN. A layered architecture ensures the confidentiality of customer data by authorizing access to sensitive servers. 

     The second regulatory compliance requirement relevant to this is HIPAA. In addition to financial data, the merged network will retain data containing medical and healthcare-related information. Any system that handles PHI must comply with HIPAA regulations and maintain the confidentiality, integrity, and availability of the data. In addition to network segmentation of sensitive data, the merged network will meet HIPAA requirements by implementing a firewall that protects internal servers and enforces controlled access and auditability.

`H.  Describe two emerging threats that are applicable to the merged organization, including the following in the description:
•   potential network security risks of implementing the topology
•   potential performance impacts on the merged network after implementation of the proposed design
•   how to manage the identified potential security risks`

    Our primary emerging threat, applicable to the merged organization, will primarily impact cloud service integration. Threats to Azure Active Directory, such as privilege escalation in hybrid AD environments and compromised or stolen credentials, are expected. Potential performance impacts include increased latency when accessing applications due to traffic passing through VPN tunnels from server VLANs to cloud services, as well as firewall bottlenecks that may strain CPU resources and slow application performance. Enforced Zero Trust access control for cloud connections and continuous monitoring of user login and access activity. 

    Another potential network security threat is segmented networks targeted by ransomware. Malware has become advanced and can move through Azure synchronization and Azure AD replication, as well as remote access, allowing ransomware to move across zones of the segmented network. The merged network's files maintain the companies' file-sharing systems, specifically SharePoint. If the files and their backups are not properly encrypted, these areas can be vulnerable to file-targeted attacks. The potential performance impacts of malware spreading include firewall overloads during the attack, and data becomes unavailable or slow to retrieve if files and SharePoint are compromised. These loads put overall strain on switches and routers, especially when filtering traffic between compromised and unaffected devices. Strengthening firewall rules and enforcing them, as well as hardening Azure AD, can help combat these emerging threats and mitigate the associated risk. Additionally, it is essential to store our files and backups in off-site locations to avoid the risk of file share loss or theft.

`I.  Summarize your recommendations for implementation of this proposed merged network based on the scenario and budgetary requirements, including the following in the summary:
•   a cost-benefit analysis for on-premises and cloud infrastructure solutions
•   a justification for your recommendations to implement the proposed secure merged network design`

    One of the many cost and operational benefits of on-premises infrastructures are the ability to reuse existing hardware while maintaining local access to critical internal services. On-premises infrastructure also ensures low latency between LAN communications. Some of the limitations include maintenance, management, and patching firewalls and DMZ hardware at each location. Scalability becomes complex as it requires additional hardware purchases.

    Regarding cloud infrastructure solutions, they reduce on-premises hardware, management, and licensing costs, which in turn provide users with centralized monitoring. This solution enhances features such as threat detection and workload offloading. Scalability is also effortless to integrate and does not require additional hardware purchases. Some limitations of cloud solutions include a commitment to monthly subscription fees and the requirement for an internet connection to access functionality. 

    Both solutions have benefits and limitations; therefore, a hybrid topology, as proposed for this merged network design, is ideal. This hybrid topology offers the best of both worlds, helping us mitigate the limitations of both solutions to the best of each solution’s abilities. This topology strikes a good balance between cost savings and scalability, while ensuring the defense-in-depth principle.

`J.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.`

U.S. Department of Health and Human Services. (2021, June 29). HIPAA & your health rights. https://www.hhs.gov/programs/hipaa/index.html

PCI Security Standards Council. (n.d.). PCI DSS: Payment Card Industry Data Security Standard. https://www.pcisecuritystandards.org/standards/pci-dss/

Microsoft. (2023, October 23). Microsoft Entra: Plans and pricing. https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing

Microsoft. (n.d.). Microsoft Azure pricing. https://azure.microsoft.com/en-us/pricing/
	
Lammle, T. (2022). CompTIA Network+ study guide: Exam N10-008. John Wiley & Sons.

















