# Guide to software security.

Credits Justin Taft.
https://www.oneupsecurity.com/research/five-minute-guide-to-software-security/

# Hacker Mentality

Study and question everything. Break to learn, don't learn to break.

- Don't assume something is secure without testing it.
- Secure specifications are often implemented insecurely.
- Do the unexpected. Knowledge is power.
- Low risk vulnerabilities can lead to major breaches.
- Be cautious and don't underestimate the opponent.

# Threat Modeling and Scoping

Understand your risks and how to mitigate them.

- Identify resources and systems to protect. View customer and business information as a liability.
- Understand who can interact with the system.
- Identify methods to interact with the system.
- Security internal to a system is just as important as the system's boundary security.
- Understand the skill and resources required to successfully exploit attacks vectors.
- Identify who owns the security of the system.
- Review plans for when a breach is attempted and when it occurs.

# Authentication and Authorization

The Achilles heel of many systems. Know who you are communicating with. Limit the actions they can perform based on their identity.

- Deny by default, permit when necessary.
- Be conservative when granting permissions.
- Use vertical permission checks. Prevent lower privileged accounts from performing higher privileged actions.
- Use horizontal permission checks. Prevent same privileged accounts from accessing each other's information. If a user knows the ID of a record to a resource they do not own, then they shouldn't be able to access it.
- Determine and enforce a password policy.
- Ensure use of Anti-CSRF tokens, CORS, and crossdomain.xml policies to prevent an attacker from forcing a user to submit authenticated requests.
- Consider using Multi Factor Authentication. For high security systems stay away from text messages (SMS), as vulnerabilities against SS7 allows SMS messages to be intercepted. Use a two factor authentication application instead.
- Session identifiers should contain at least 128 bits of entropy.
- Ensure session expiration limits are in place. Expire session tokens on the server when a user logs out.
- NEVER DISABLE CERTIFICATE CHECKING. Set up an internal Public Key Infrastructure (PKI) and issue certificates when required.

# Never Trust User Input

Expect the unexpected. Think about edge cases and handle them appropriately. Hackers are quite clever.

- Perform validation on user input. Allowing users to specify negative values used during monetary calculations can be bad.
- Escape, encode, and parameterize user input so it can't be interpreted maliciously. Watch out for NoSQL,SQL,XSS,XXE, and command injections. Use a templating engine to prevent XSS injections.
- Use whitelisting over blacklisting whenever possible.
- Validation must occur on the receiving side of communications. Validation on the sending side is a user experience decision.
- If a stateless architecture being used, use a MAC or an authenticated encryption mode to authenticate input.

# Disclose What's Only Necessary

Attackers will look for any information to learn about a system.

- Report generic error messages to users instead of detailed error messages. Detailed error messages can be recorded in private logs.
- Don't show stack traces to the end user.
- Don't disclose version numbers of dependencies or OS information whenever possible. This does not make a system more secure, but may slow down an attacker.
- Ensure directory and Amazon S3 bucket contents are not listable.
- Do not disclose usernames of a system whenever possible. This often occurs during registration, authentication, and password request processes.
- Under certain scenarios, timing of computations can disclose internal workings of a system, as well as power consumption.

# Log Everything

Monitor for active attacks. Be prepared to investigate breaches.

- Log as much as possible. Timestamp everything.
- Logging of Authentication attempts, Access Control List violations, HTTP requests, and network activity is a good start.
- Protect the integrity of logs. Forward them to another system so they can be archived and can't be modified.
- Do not log sensitive information in plain text, such as user credentials or personal identifying information.

# Cryptography

Encrypt data to keep it secret from prying eyes. Sign or use a MAC to ensure data has not been tampered with. Consult with a professional who is qualified to make recommendations for your particular use of cryptography. Below is a general guideline.

- If cryptography is needed, use libsodium when in doubt. Don't roll your own crypto.
- Never encrypt user passwords, securely hash them. If in doubt, use a password hasing function from libsodium. Password hashing must be slow to deter password cracking attempts. Taking 100ms or more for the hash to be generated is recommended as a minimum. As the hash calculations are CPU intensive, authentication can be scaled to other hosts as needed.
- Protect your keys! Never store symmetric keys, asymmetric private keys, or passwords unencrypted on disk, in databases, or in source code repositories.
- Use Cryptographically Secure Random Number Generator (CSRNG) for cryptographic operations. Non secure random number generators have biases and are predictable.
- Generate keys and passwords using CSRNG. Always rotate a key when it becomes compromised. Generate a new key and do not use the compromised key anymore. Re-encrypt old data with the new key to be safe.
- If verifying the authenticity of a message is only required, and the content of a message must not be kept a secret, using only a MAC without encryption is fine.
- Be careful of endpoints which can be used to encrypt and decrypt arbitrary messages. It's much easier and common to break the way crypto is being used, rather then the crypto itself.
- Watch out for replay attacks. Encrypted messages can often be processed multiple times by resending them.
- Use TLS 1.1 or higher. For recommended cipher suites and parameters, see https://wiki.mozilla.org/Security/Server_Side_TLS and http://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-https-listener.html. Ensure client-renegotiation is disabled to prevent DoS attacks.
  
# Know Your Technology

Much software is insecure by default. Attackers will look for the easiest way in.

- Keep software up to date. Many software updates contain security updates, but are not marked as such. Do not use software if it has reached its end of life.
- Disable XML Doctype parsing for Java Applications when not required. XXE is still common.
- Disable services which are not used. Harden services which are being used. Never use default or easy to guess credentials. Ensure authentication is required for all services (Apache, Jenkins, MongoDB, MySQL, HockeyApp, etc.). **Don't forget to secure non-production services and systems too.**
- Return proper header values for Strict-Transport-Security, CORS, and X-Frame-Options. Set Secure and HTTP Only Cookie Flags.
- Know your programming languages thoroughly. Avoid using undefined behavior, as vulnerabilities may be introduced into your code because of it. Use compiler flags to warn of insecure practices and to enable security mitigations (PIE, Stack Cookies, SafeSEH, etc.)
- Use mitigations (firewalls, antivirus, SE Linux policies, ASLR, Stack Cookies, etc.) to mitigate possible attacks from being successful.

# Miscellaneous

- Phishing scams are effective. Perform in-house testing to educate employees.
- Setup disk encryption on development laptops in case they are lost or stolen.
- Ensure developers are using secure coding practices.
- It's much easier to fix a vulnerability in a single location. Copying and pasting code can lead to wide-spread vulnerabilities.
- Obfustication will slow down an attacker but will not stop them.
- Segregate trusted and untrusted network devices.
- Fuzz your applications to find vulnerabilities.
- Don't overlook race conditions.
- Always perform bounds checking. Don't re-implement insecure functions such as strcpy.
- Avoid running applications as root.
- Configure file permissions on hosts to prevent sensitive files being read or overwritten.
- White box tests uncover more vulnerabilities than black box testing. Be transparent with the security engineers who are testing your system. Assessments are timeboxed while real attacks are not.