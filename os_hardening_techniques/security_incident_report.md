# Security Incident Report

1. Identify the network protocol involved in the incident

DNS and HTTP were both used during this incident.

2. Document the incident

Approximately around 2:18pm, we've identified a threat actor that uploaded malicious code which redirected yummyrecipesforme.com to greatrecipesforme.com. The initial request to the DNS to yummyrecipesforme.com pointed correctly to the IP but a few milliseconds later, there was a Data Push flag to download code to redirect the client to greatrecipesforme.com. We suspect that the threat actor was able to gain access to the admin panel and added changes for the redirect.

3. Recommend one remediation for brute force attacks
   To prevent threat actors from accessing the admin panel, we would use a strong secure (encrypted) password and rotate it every 30 days. We can also preventmore brute force attacks by limiting the amount of times they can try to gain access and lock them out using their IP address.
