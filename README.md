# Hacking Game on Copilot for Security

## Challenge 1 Goal

In this challenge, we invite you to step into the role of a Attacker (hacker). Your first objective will be to access to a corporate network by infiltrating a user's machine. Once you have gained access to this machine, your ultimate goal will be to gain control over the company's domain.   

Are you ready? 

>**Note**: We encourage participants of the CoHack to utilize their own subscription or Bring Your Own Subscription (BYOS) to ensure they can fully engage with and effectively tackle the challenges presented. As of April 2024, we would like to inform you that demo environments are not available for this event. Additionally, Copilot for Security is not designed for use by customers using US government clouds. We appreciate your understanding and are here to support you throughout the experience. For cost details please see: https://azure.microsoft.com/en-us/pricing/details/microsoft-copilot-for-security

## Environment 

There are 3 VMs: Hack-vm (Windows10), Workstation-vm (Windows10) and Dc-vm (Windows Server 2016) 


![archi](./images/archi.png)

## Hacking Steps

1. Connect to the Hack-vm using RDP. Your coach will provide you with the Public IP address and credentials.

2. Use nmap to discover the private IP address of the Workstation-vm.

3. Use hydra to find the login and password that will allow you to connect to the Workstation-vm using RDP.

4. Connect to the Workstation-vm using RDP and the login and password found in step 3.

5. Discover the IP address of the domain controller Dc-vm (nslookup).  

6. Use mimikatz, (a) to find the login and password hash of the Domain Admin then (b) to connect to the domain controller using RDP.


  >**Note**: Each tool should be used one time  

## Toolbox
1. Mimikatz
    - https://github.com/ParrotSec/mimikatz
    - https://techyrick.com/mimikatz-tutorial/
    - https://edermi.github.io/post/2018/native_rdp_pass_the_hash/

2. Nmap 
    - https://nmap.org/download.html

3. Hydra 
    - https://github.com/maaaaz/thc-hydra-windows
    - https://medium.com/@cuncis/hydra-a-powerful-tool-for-password-cracking-and-network-security-testing-cheat-sheet-6573b74071ee
    - https://github.com/adeldjama/Hacking-Game/blob/37fa336979bbdabf53f53ce07d7832900f47b2c4/resources/username.txt
    - https://github.com/adeldjama/Hacking-Game/blob/37fa336979bbdabf53f53ce07d7832900f47b2c4/resources/password.txt
  
## Challenge 2 Goal

Now you are a security Defender trying to fix what the Attacker has done to stop further unauthorized access to the environment. The primary objective is to protect the corporate network from any potential threats. Your management wants a central location to check on all incidents and threats. They have asked to enable tools like Generative AI and Machine Level defenses. 

Below is a suggested response to approach the situation. These do not have to be used as there are many ways of accomplishing the goal:

  **Investigation:**

  1. **User's Machine Infiltration:** I would first investigate the user's machine for any signs of unauthorized access. This could involve checking for unusual network traffic, unfamiliar processes running on the system, or unexpected changes in system files.

  2. **Network Access:** If the attacker has gained access to the corporate network, I would use network monitoring tools to identify any unusual activity. This could include unexpected data transfers, connections to unfamiliar IP addresses, or unusual patterns of network traffic.

  3. **Domain Control:** Gaining control over a company's domain is a serious threat. I would check the domain controller for any signs of unauthorized access or changes. This could involve checking logs for unexpected administrative actions, or looking for changes in user permissions or group memberships.

  **Tools:**

  - **Generative AI:** I would use Generative AI to simulate potential attack scenarios and test the robustness of our defenses. This could help identify vulnerabilities and improve our response to real attacks.

  - **Machine Level Defenses:** I would employ machine-level defenses such as antivirus software, firewalls, and intrusion detection systems to protect individual machines and the network as a whole.

  **Remediation:**

  - Upon identifying the threat, I would take immediate action to mitigate the damage. This could involve isolating affected systems, removing malicious software, and reversing any unauthorized changes. I would also work to strengthen our defenses to prevent similar attacks in the future.

  **Incident Summary:**

  - Finally, I would prepare a summary of the incident for management. This would include details of the attack, the steps taken to mitigate the damage, and recommendations for preventing similar incidents in the future. It's crucial to learn from these incidents and continually improve our security posture.

**Additional Suggestion:**

 - **Prompts:** To create effective prompts give Generative AI adequate and useful parameters to generate a valuable response. The following suggestion are elements should be included when writing a prompt.

   ![archi](./images/Prompts.png)

## Resources

1. Unified Security Operations Platform
   - https://learn.microsoft.com/en-us/azure/sentinel/microsoft-sentinel-defender-portal
   - https://learn.microsoft.com/en-us/copilot/security/get-started-security-copilot
