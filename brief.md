Version: NAFATH-V3
Track: Networking

## Overview
A government entity is developing a mobile application that helps citizens find information about public services. The application includes an AI chat assistant that answers questions using official government information. Citizens may use it to ask about documents, procedures, eligibility, and application status. The system must provide useful and accurate answers while protecting personal information. It also needs secure mobile connections, reliable network communication, and a maintainable software design. This brief explains how six IT fields contribute to the project: software versioning, retrieval-augmented generation, mobile application security, IPv6 networking, prompt-injection protection, and data privacy. These areas work together to make the service more reliable, secure, and trustworthy for citizens, while IPv6 networking supports connectivity as connected devices grow.
## Software
Semantic Versioning uses three numbers: MAJOR.MINOR.PATCH. A MAJOR increase is required for incompatible API changes. A MINOR increase adds backward-compatible functionality, while a PATCH increase fixes backward-compatible bugs. In the government app, an API change that breaks older mobile clients requires a major version increase. A compatible new feature needs a minor increase, while a backward-compatible bug fix needs a patch increase. This approach helps developers communicate changes and manage compatibility between releases.
Resource: Semantic Versioning 2.0.0 – https://semver.org/
## AI
Retrieval-Augmented Generation (RAG) combines information retrieval with a generative AI model. Before answering a citizen, the assistant retrieves relevant information from an approved knowledge base and uses it to generate a response. This can ground answers in official service information and help keep them up to date. However, RAG cannot guarantee accuracy if retrieved documents are incomplete or irrelevant. The system should use trusted sources, evaluate answers, and avoid unsupported responses when reliable information is unavailable.
Resource: Retrieval-Augmented Generation – https://cloud.google.com/use-cases/retrieval-augmented-generation
## Mobile
App Transport Security (ATS) enforces security requirements for network connections made by apps using standard URL loading. It generally requires HTTPS instead of unencrypted HTTP. If an app attempts to access an HTTP endpoint that violates ATS requirements, the connection is normally blocked unless an applicable exception is configured. HTTPS uses TLS to protect data in transit and authenticate the server. Keeping ATS protections enabled helps safeguard citizens' information when they use the government app.
Resource: Preventing Insecure Network Connections – https://developer.apple.com/documentation/security/preventing-insecure-network-connections
## Networking
IPv4 uses 32-bit addresses, while IPv6 uses 128-bit addresses, providing a much larger address space. This matters as more phones, computers, and other devices connect to online services. IPv6 helps support the continued growth of Internet connectivity. The government application should be tested on networks using IPv4, IPv6, or both, because citizens may use different providers and network configurations. IPv6 alone does not guarantee better performance or security; correct network configuration remains essential.
Resource: Internet Protocol, Version 6 (IPv6) Specification – https://www.rfc-editor.org/rfc/rfc8200.html
## Cybersecurity
Prompt injection is an attack that uses malicious instructions to manipulate an AI system. Direct prompt injection happens when a user enters instructions such as “ignore previous instructions.” Indirect prompt injection happens when malicious instructions are hidden in external content, such as a document retrieved by the assistant. Two ways to reduce the risk are to limit the AI's permissions and separate untrusted content from trusted instructions. Regular security testing can help identify weaknesses.
Resource: LLM Prompt Injection Prevention Cheat Sheet – https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html
## Data
Anonymization removes identifying information so individuals cannot reasonably be identified, while pseudonymization replaces identifiers with codes but may allow re-identification using additional information. Under the GDPR, effectively anonymized data falls outside its scope, but pseudonymized data generally remains personal data. For government chat logs, teams should minimize personal details, restrict access, and assess re-identification risks before sharing stored data.
Resource: General Data Protection Regulation (GDPR), Recital 26 and Article 4(5) – https://eur-lex.europa.eu/eli/reg/2016/679/oj
## Misconception in My Track

## Open Question
