# Defense in Depth

## Building sec concenceness*

### Anatomy

- Human errors
  - Reused creds
  - Confused deputies
  - Shortcuts in procedures
- A festering wound
  - Foot in the door
  - Building bigger breaches on smaller ones
  - Lack of early detection

#### What is not typical breach

- Cracking modern hashes
- Using secret vulnerabilities that don't have fixes

## Frame of mind

In mindset from beginning. Not retrospective.

Middle ground between ignorance and security.


### CIA
CIA security triad

- C.onfidentiality
- I.ntegrity - never ever trust a user. Set permissions correctly.
- A.vailability - balance out usability.

### What does hacked mean?

- Defacement
- DoS
- Data Breach

### Defense in Depth

You'll never have perfect security.
Limit exposure.

#### Unhardened SSH
Protect SSH passwords. SSH keys are not just safe. Exploit for ff, pdf viewer could read keys off the home dir. `~/.ssh`. Put passphrases on SSH keys.

Consider using smartcards.

## Are you vulnerable?

- US Cert/Cert-Eu
- LWN
- D.o
- Security only updates with apt-get/yum
- Twitter

## Compliance Regs.

Private laws vary by country. EU Data protection regulation. PCI data sec standards. (PCI DSS)

## EU Data Protection Regs

1. New data protection regs law this year
2. Everyone who holds data on EU citizens are affected. Even if not in EU.
3. Fines for non-compliance cost millions
4. Do not persist data.

## Keep a backup.

Segment backups permissions so the same key can not used to delete and create backups.

## Federated logins

Use social and enterprise logins.
- FB
- Twitter
- GH

### Use secure passwords

Don't have needlessly strict passwords. Use:
- LastPass
- KeePassX

Don't use same password over and over again. The best password is one that you don't know.

### Two factor auth

Consider using two factor auth for additional, more dangerous operations.
Cobination of something you know and something you have. e.g password and phone.

https://www.digitalocean.com/community/tutorials/how-to-protect-ssh-with-two-factor-authentication

### If you don't need it - hands off.

Use payment gateways that pass thru data.

## Secure OS

- Install security updates
- Automate Configuration
- Invest in ability to safely, quickly update servers
- Definitely manage:
  - iptables
  - SSH (no root, no passwords)
  - sudoers
- Detect compromise
  - Rootkit detection

## Webserver

- Send headers down to browser, X-FRAME-OPTIONS, STRICT TRANSPORT SEC.
- Make use of logs (logrotate)
- Disable server headers
- Prevent access to private directories
- Deploy a web application firewall with mod_security.

## Database

- Change default password.
- Lock down access to required hosts
- Secure backups.

## Data encryption

No way to encrypt data in Drupal in core.

### Modules:

- encrypt
- key
- encrypt user
- field encryption
- encrypted files

### Key management
- Store and manage keys on a different server.
- Dont share your API keys with developers that dont need access them. (Principle of least privilege)
- Use development keys or dummy keys.

Key module in drupal?

Offsite key storage. https://lockr.io for pantheon.

## Drupal core sec
- Keep it updated
- Keep permissions simple

## Contrib
- Active, popular plugins have higher security scrutiny.
- Just because its on D.o does not make it secure.

## Secure your team.
- Create policy bottleneck/SSO
- Enforce 2FA, strong passwords
- Secure devices.
- Build security consciousness

## What to do

- Rollback
- Review
- Reach out
