# draft-signal-uicc-secure-chat

A design for a secure chat messenger based on the signal e2e encryption protocol with uicc as the TPM component.

# Issue

In our digital world, we exchange information and messages every day. The majority of our messages are uninteresting and it is enough to protect them from prying eyes, but there is also information that is sensitive or even forbidden to share with others. The number of countries that rely on censorship and control on the Internet is increasing. Fortunately, there are widely used messengers such as WhatsApp / Signal, which allow messages to be securely encrypted end to end. Until today, the Signal protocol is considered one of the most secure chat protocols. Both messengers, however, have a big problem when it comes to storage on the device. WhatsApp and Signal stores the cryptographic keys used for encrypting and decrypting on the device unencrypted.
This means that any person who has physical access or installed malware on the device can potentially read the keys and use them to perform decryption.
It's especially a hassle when police, security agencies, the military, or other political bodies get their hands on these devices.

# Concept

The concept is based on the implementation of a messenger that uses the signal protocol for the secure encryption and decryption of messages. For the management of the cryptographic keys, an applet based on the uicc toolkit is designed, which takes over the tasks of the cryptographic process. In the last step, a remote provisioning for eUICC is implemented.
