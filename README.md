## Introduction
<br>In this lab I will be using Nessus Vulnerability Scanner to assess the vulnerabilities of a vm and remediate them. The focus will be on reducing the number of critical through low level vulnerabilities discovered in the scan.</br>

## Scan Before Hardening
<b>Vulnerabilities</b>
<br>Here we can see a very vulnerable system specifically because of an outdated version of Firefox, Windows OS, and Internet Explorer.</br>
<br>![image](https://github.com/ChrisHaugaard/NessusVM/assets/140214520/5f33dfd3-a961-4954-88fb-6a13c59fc45d)</br>
<br>
| Metric                   | Count
| ------------------------ | -----
| Critical                 | 6
| High                     | 3
| Medium                   | 1
| Low                      | 0
| Info                     | 107
</br>

<b>Recommended Remediation</b>
<br>We can see there are 2 recommended remediations for this VM. I will be applying the changes and seeing the effect on the total vulnerabilities the vm contains.</br>
<br>![image](https://github.com/ChrisHaugaard/NessusVM/assets/140214520/ab6acb65-d6bb-46bf-98f2-e1a57cf8799a)</br>

## Scan After Hardening
<b>Vulnerabilities</b>
<br>As we can see after hardening the system and remediating the vulnerabilities we are left with Info level alerts. For this lab I will be letting the info alerts stay as the goal was to remediate critical through low level vulnerabilities. </br>

<br>![image](https://github.com/ChrisHaugaard/NessusVM/assets/140214520/9baa9971-2682-4485-9a18-e38ce7808b77)</br>
<br>
| Metric                   | Count
| ------------------------ | -----
| Critical                 | 1
| High                     | 1
| Medium                   | 1
| Low                      | 0
| Info                     | 81
</br>
<b>Remediations Applied</b>
<br>While it does still indicate that there are vulnerabilities at each level of critical, high, and medium I have made sure to remediate them. Below I attached screenshots for the remedies covering WinVerifyTrust Signature Validation and SMB Signing not required. I also uninstalled and removed Internet explorer from the system which was the cause of the critical vulnerability. </br>

<br>High: WinVerifyTrust Signature Validation</br>
<br>![image](https://github.com/ChrisHaugaard/NessusVM/assets/140214520/9e05b92d-d876-4d36-8b4c-64949327fd32)</br>

<br>![image](https://github.com/ChrisHaugaard/NessusVM/assets/140214520/bc709a6b-138a-41f2-85be-fa88279c4212)</br>

<br>Medium: SMB Signing</br>
<br>![image](https://github.com/ChrisHaugaard/NessusVM/assets/140214520/0cc7eecf-998b-4c0f-835f-0cab9504201a)</br>


## Conclusion
<br>Through the use of updates, uninstalls, and registry changes I was left with a vm that only contains info level alerts. </br>
