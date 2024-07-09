# Federated_Learning_Project

we're introducing a privacy-preserving system that uses federated
learning to analyze medical data securely. Using the MURA dataset, which contains a
large number of bone X-rays, our goal is to train the DL model to identify normal and
abnormal X-ray images without compromising patient privacy. The system works by
having each participant train models on their data locally, then encrypt and share their
model weights using Fernet encryption, which relies on AES and HMAC for security and
key derivation. These encrypted weights are sent to a federated server via a STFP (Secure file transfer protocol), the keys are shared via a secure channel like an encrypted email. The server then decrypts,
averages, and redistributes the weights, creating a shared model without ever exposing
the sensitive data. This approach builds on existing research but emphasizes data
security and patient privacy throughout the learning process.
