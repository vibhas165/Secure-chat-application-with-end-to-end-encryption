# Secure-Chat-Application-With-End-to-End-Encryption


This project involves developing a Secure-Chat-Application-With-End-to-End-Encryption from scratch, inspired by applications like WhatsApp and Signal, with end-to-end encryption. The application provides features for secure, multi-user communication using various encryption modes.


Features

      1. Multi-User Group Chat: Users can participate in group chats in real time.
      2. Encryption Modes:
          Single Key Encryption: Data Encryption Standard (DES).
          Two-Key Encryption: RSA and El Gamal algorithms.
          Third Trusted Party (TTP): Facilitates interactions between parties with trusted intermediaries.
      
      
      Technology Stack
            Programming Language: Python
            UI Framework: Tkinter
            Real-Time Messaging: Python’s Socket Library


System Design

      Workflow:
            1. Server starts on a designated HOST IPv4 and PORT.
            2. Client connects to the server.
            3. Server accepts the connection and generates a session key for the client.
            4. Clients send usernames and initiate a listener thread.
            5. Messages are encrypted using the chosen encryption mode before being sent.
            6. Server broadcasts encrypted messages to all connected clients.
            7. Clients decrypt the received messages.

![image](https://github.com/user-attachments/assets/b468d7f0-136d-46c3-98f0-4fd1c5b059b9)


Server Responsibilities:

Handle client connections.
Distribute encrypted messages.
Exchange keys and metadata for secure communication.


Encryption Techniques

1. Data Encryption Standard (DES):

      A symmetric block cipher that encrypts data in 64-bit blocks.

      Steps:
            Initial Permutation (IP).
            16 Rounds of Encryption (Left and Right halves).
            Final Permutation (FP).
            Ensures 64-bit ciphertext output per block.


2. Rivest-Shamir-Adleman (RSA):

      Asymmetric cryptography using public and private keys.

      Key Generation:
            Select prime numbers p and q.
            Calculate n = p * q and Euler’s totient.
            Choose public key e (coprime with totient).
            Compute private key d.
      
      Encryption: C = (M^e) mod n.
      Decryption: M = (C^d) mod n.


3. El Gamal Cryptography:

      Asymmetric encryption based on Diffie-Hellman key exchange.

      Key Generation:
            Choose a prime number q and primitive root a.
            Generate private key XA.
            Compute public key YA = a^XA mod q.
      
      Encryption: Generates ciphertext pairs (C1, C2).
      Decryption: Recovers plaintext using C1, C2, and private key.

Server Console:
      Displays active connections and logs sent/received messages.

Client Console:
      Allows message sending, encryption mode selection, and decryption.


Server Prompt ( SEND , RECV Messages)
![image](https://github.com/user-attachments/assets/52ba7801-7ca6-46c6-aa74-05d03d8b3040)


Clients Prompt ( SEND , RECV, ENCRYPT, DECRYPT )
![image](https://github.com/user-attachments/assets/4eac9136-925c-4724-b257-a7fffba8f72e)
