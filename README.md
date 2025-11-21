# Create-a-Private-and-Public-Key-Pair
A public key and a private key are the fundamental components of asymmetric encryption, enabling cryptographic operations such as encryption, decryption, and digital signatures. 
## Learning Device
- ### ACIALMA- Alma Linux 9.1 - Stand-alone Linux Server ###
## Let's Get Started
- ### Connect to ACIALMA.
  - Select Activites and click on Terminal on the desktop
  - In the Terminal window, type the following and press Enter: mkdir Module_1 && cd Module_1
  <img width="967" height="156" alt="image" src="https://github.com/user-attachments/assets/8278b3b0-43b9-4c27-8ad3-dd0a76a1ff83" />

  - Type the following and press Enter: mkdir Digital_Signature && cd Digital_Signature
  <img width="1375" height="116" alt="image" src="https://github.com/user-attachments/assets/4c02d17c-2d34-4310-a3b5-d739ae53ce03" />

  - Type the following and press Enter: mkdir Alice Bob
  <img width="1367" height="141" alt="image" src="https://github.com/user-attachments/assets/eb3657c3-f194-4558-9604-dc20a4eccec4" />

  - Type the following and press Enter: cd Alice
  <img width="1359" height="173" alt="image" src="https://github.com/user-attachments/assets/5d898db8-a790-4a62-9f0b-b1415c2c530b" />

  - Type the following and press Enter: openssl genpkey -algorithm RSA -out alice_privatekey.pem
  <img width="1529" height="216" alt="image" src="https://github.com/user-attachments/assets/5353e1cd-82a2-4553-bbf6-d36ef4aa276d" />

 - ### Note: This OpenSSL command creates a private key. The RSA algorithm has been specified as the name of the resulting private key file: alice_privatekey.pem. In Linux, the suffix .pem does not define the file type but is used as a convention to identify the type of file to the user. In this case, the private key is in a PEM format. ###

   - Type the following and press Enter: openssl rsa -in alice_privatekey.pem -out alice_publickey.pem -pubout -outform PEM
   <img width="1747" height="184" alt="image" src="https://github.com/user-attachments/assets/6758a084-6885-43c0-a1af-d4c6781b7cae" />

 - ### Note: This OpenSSL command creates a public key for Alice, which uses the previously created private key as input. This ensures the mathematical connection between the private and public key pair. The public key that is created is also in a PEM format. ###
