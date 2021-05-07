====================================
Project Standards and Best Practices
====================================

This document is a sumation of some of the standards and best practices that are followed in the design and implementation of the project to provide guidance and clarity for implementers and contributors.

===========
Code Styles
===========

Individual projects will have their own conventions for code style, and we don't expect a single best practice to be followed.

Across all of our projects, however, the default approach for new development is that new code will be expected to follow the conventions and style of the code around it.

========
Security
========
Our project baseline security practices should be based on the latest recommendations from the Open Web Security Project (OWASP), which provides practical and evidence based standards for software implementers. If there is a question in approach on system design and OWASP has a stated position on the best approach, it should be expected that the OWASP sanctioned approach will be adopted.

Security Protocols and Cryptography Implementation
--------------------------------------------------

Our projects strive for a high standard of technical and practical security, but it is not the intended purpose of the most of our projects to provide a novel technical approach to security.  Since there is an overwhelming consensus from security researchers and practitioners[1]_,[2]_ that it is a harmful practice for software systems to attempt to implement their own unique security or cryptographic protocols, no such implementations will be adopted by the project.

Specifically, components of the project which externally authenticate users or secure data cryptographically should be:

- Based on a publicly documented specification or approach (Basic Authentication, OAuth, SAML, AES256, etc)
- In broad use in modern software with a practical basis of demonstrated success
- Adopted through the use of externaly implemented libraries or dependencies whenever practically possible

This expectation does not necessarily extend to code which is required for integrations which authenticate against external systems. Those implementations should always follow this approach when possible, and best practices should be maintained when managing secrets for such components.

.. [1] Jakob Jakobsen and Claudio Orlandi "On the CCA (in)security of MTProto." *Cryptology ePrint Archive, Report 2015/1177*

.. [2] Philipp Jovanovic and Samuel Neves "Dumb Crypto in Smart Grids: Practical Cryptanalysis of the Open Smart Grid Protocol." *Cryptology ePrint Archive, Report 2015/428*

