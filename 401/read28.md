#  Configuring Django Settings: Best Practices
---
### Managing Django Settings: Issues


- Different environments. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. Each environment can have its own specific settings (for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc).
- Sensitive data. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter.
- Sharing settings between team members. You need a general approach to eliminate human error when working with the settings.
- Django settings are a Python code. This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.

---

### Django Settings: Best practices : 


- Keep settings in environment variables.
- Write default values for production configuration (excluding secret keys and tokens).
- Don’t hardcode sensitive settings, and don’t put them in VCS.
- Split settings into groups: Django, third-party, project.
- Follow naming conventions for custom (project) settings.

---

### How Does SSH Work ?

### What is SSH ? 

#### SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. The service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner.

### How Does SSH Work ! 

### If you’re using Linux or Mac, then using SSH is very simple. If you use Windows, you will need to utilize an SSH client to open SSH connections. The most popular SSH client is PuTTY, which you can learn more about here.

```
ssh {user}@{host}
```

### Understanding Different Encryption Techniques

#### The significant advantage offered by SSH over its predecessors is the use of encryption to ensure secure transfer of information between the host and the client. 


- Symmetrical encryption
- Asymmetrical encryption
- Hashing.

###  Symmetric Encryption

#### Symmetric encryption is a form of encryption where a secret key is used for both encryption and decryption of a message by both the client and the host. Effectively, any one possessing the key can decrypt the message being transferred.

---
### Hashing

#### One-way hashing is another form of cryptography used in Secure Shell Connections. One-way-hash functions differ from the above two forms of encryption in the sense that they are never meant to be decrypted. 

### Conclusion :

#### Gaining an in-depth understanding of the underlying how SSH works can help users understand the security aspects of this technology. Most people consider this process to be extremely complex and un-understandable, but it is much simpler than most people think. If you’re wondering how long it takes for a computer to calculate a hash and authenticate a user, well, it happens in less than a second. In fact, the maximum amount of time is spent in transferring data across the Internet.




