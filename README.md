Windows Investigation – SOC Analyst Report

Platform: TryHackMe
Room: Investigating Windows
Category: Digital Forensics & Incident Investigation
Status: Completed

1. Investigation Overview

Conducted a Windows investigation to identify suspicious activities, investigate system compromise, analyze persistence mechanisms, and identify attacker infrastructure using Windows artifacts and event logs.

2. Investigation Findings & Evidence

Q1. What's the version and year of the Windows machine?

Answer: Windows Server 2016

Evidence – Screenshot 01:

<img width="400" height="403" alt="Screenshot 2026-11-20 155733" src="https://github.com/user-attachments/assets/1e1adb1e-485b-4cfb-816d-1e9ef59476c2" />


Q2. Which user logged in last?

Answer: Administrator

Evidence – Screenshot 02:

<img width="343" height="259" alt="Screenshot 2026-11-20 160050" src="https://github.com/user-attachments/assets/8ef4497f-f872-4acf-a839-9cf5478e333b" />


Q3. When did John log onto the system last?

Answer: 03/02/2019 5:48:32 PM

Evidence – Screenshot 03:

<img width="343" height="371" alt="Screenshot 2026-11-20 160119" src="https://github.com/user-attachments/assets/0b00e8f4-ee32-4915-99a2-2765fe8baccb" />


Q4. What IP does the system connect to when it first starts?

Answer: 10.34.2.3

Evidence – Screenshot 04:

<img width="585" height="128" alt="Screenshot 2026-11-20 162614" src="https://github.com/user-attachments/assets/122af666-bad1-41d1-aaae-6e75303c8b59" />


Q5. What two accounts had administrative privileges (other than Administrator)?

Answer: Guest, Jenny

Evidence – Screenshot 05:

<img width="440" height="125" alt="Screenshot 2026-11-20 160804" src="https://github.com/user-attachments/assets/56cb3da7-af84-497e-a105-4a885f802f56" />


Q6. What's the name of the scheduled task that is malicious?

Answer: Clean file system

Evidence – Screenshot 06:

<img width="779" height="389" alt="Screenshot 2026-11-20 160957" src="https://github.com/user-attachments/assets/055a9ad0-f773-4cf9-ba11-7a26f332e027" />


Q7. What file was the task trying to run daily?

Answer: nc.ps1

Evidence – Screenshot 07:

<img width="506" height="266" alt="Screenshot 2026-11-20 161047" src="https://github.com/user-attachments/assets/da01f84c-552b-4aed-89f2-501a4e26bf06" />


Q8. What port did this file listen locally for?

Answer: 1348

Evidence – Screenshot 08:

<img width="506" height="266" alt="Screenshot 2026-11-20 161047" src="https://github.com/user-attachments/assets/155a126b-ae98-4093-9db5-9fe9de9bc5c8" />


Q9. When did Jenny last logon?

Answer: Never

Evidence – Screenshot 09:

<img width="313" height="227" alt="Screenshot 2026-11-20 161214" src="https://github.com/user-attachments/assets/7463ccf2-0903-4c92-b5c3-409a05e528ab" />


Q10. At what date did the compromise take place?

Answer: 03/02/2019

Q11. During the compromise, at what time did Windows first assign special privileges to a new logon?

Answer: 03/02/2019 4:04:49 PM

Evidence – Screenshot 11:

<img width="407" height="275" alt="Screenshot 2026-11-20 171858" src="https://github.com/user-attachments/assets/b5009540-bb0f-4125-a268-62bc0f4e55af" />


Q12. What tool was used to get Windows passwords?

Answer: Mimikatz

Evidence – Screenshot 12:

<img width="611" height="351" alt="Screenshot 2026-11-20 164053" src="https://github.com/user-attachments/assets/b5ac464e-f639-4306-82bd-08f6488891e1" />


Q13. What was the attacker's external command and control server IP?

Answer: 76.32.97.132

Evidence – Screenshot 13:

<img width="450" height="307" alt="Screenshot 2026-11-20 164335" src="https://github.com/user-attachments/assets/13d47e7f-48f0-4f0f-a696-cbd9b75fd8d9" />


Q14. What was the extension name of the shell uploaded via the server's website?

Answer: .jsp

Evidence – Screenshot 14:

<img width="500" height="109" alt="Screenshot 2026-11-20 164402" src="https://github.com/user-attachments/assets/a86aeead-f3ac-4195-9bca-2d709fe80ce9" />


Q15. What was the last port the attacker opened?

Answer: 1337

Evidence – Screenshot 15:

<img width="778" height="368" alt="Screenshot 2026-11-20 164625" src="https://github.com/user-attachments/assets/84d62db8-28a1-4d2a-9835-ab0c7bb08907" />


Q16. Check for DNS poisoning, what site was targeted?

Answer: google.com

Evidence – Screenshot 16:

<img width="386" height="233" alt="Screenshot 2026-11-20 164745" src="https://github.com/user-attachments/assets/44895dab-2c59-4a63-8876-c8745577a6e5" />


3. Conclusion

The investigation identified multiple indicators of compromise, including suspicious scheduled task activity, unauthorized administrative accounts, credential theft using Mimikatz, web shell activity, and external command and control infrastructure.

The lab provided practical experience in Windows Event Log analysis, Registry investigation, persistence detection, credential theft investigation, and network forensics.

Lab Status: Completed
Platform: TryHackMe
