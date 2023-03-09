# Jedox Cloud Console
Jedox Cloud Console Reflected XSS

Description:
The Jedox Cloud Console login is vulnerable for unauthenticated reflected XSS, which might allow remote attackers to execute code on their targets.

Evidence:<br>
<strong>Url</strong>: "https://console.cloud.jedox.com/login"
<br><strong>Payload</strong>: "/<img%20type=image%20src=1%20onerror=alert('xss')>"

<br><strong>Proof:</strong><br>
![image](https://user-images.githubusercontent.com/121053557/224050295-a153f229-8b91-4255-95d3-1d90c7729cfa.png)
![image](https://user-images.githubusercontent.com/121053557/224050606-d6357ec3-5a7e-44e3-b3e9-b4cf1a866935.png)


<strong>Impact</strong>:
Malicious JavaScript has access to all the same objects as the rest of the web page, including access to cookies and local storage, which are often used to store session tokens. If an attacker can obtain a user's session cookie, they can then impersonate that user.
Furthermore, JavaScript can read and make arbitrary modifications to the contents of a page being displayed to a user. Therefore, XSS in conjunction with some clever social engineering opens up a lot of possibilities for an attacker.
