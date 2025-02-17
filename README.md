# IS-IA-Veracrypt 
This project demonstrates the use of VeraCrypt, a contemporary security tool for encrypting a folder to ensure data confidentiality.

Tools & Technologies Used
  -VeraCrypt: Open-source encryption software for creating and managing encrypted volumes.
  -Operating System: Windows 

Project Implementation
1. Installation of VeraCrypt: 
   Download VeraCrypt from the official website: https://www.veracrypt.fr
2. Creating an Encrypted Volume: 
   1. Launch VeraCrypt and select "Create Volume."
   2. Choose "Create an encrypted file container" (or encrypt a non-system partition as per requirement).
   3. Choose encryption options:
     Encryption Algorithm: AES
     Hash Algorithm: SHA-512
   4. Set a volume size and a strong password.
   5. Format the volume and mount it as a virtual disk.
3. Mounting and Using the Encrypted Volume
    1. Open VeraCrypt, select a drive letter, and click Mount.
    2. Enter the password and access files as needed.
    3. When done, click Dismount to secure your data.

Automating VeraCrypt with Command-Line
1.  Creating an Encrypted Volume via CLI: 
   - veracrypt -t -c --volume /path/to/encryptedfile.vc \
          --size 100M --encryption AES --hash sha512 \
          --filesystem FAT --password YourStrongPassword \
          --pim 0 --keyfiles "" --random-source /dev/urandom

2. Mounting an Encrypted Volume: 
   veracrypt -t /path/to/encryptedfile.vc /mnt/veracrypt1 --password YourStrongPassword
   
3. Dismounting an Encrypted Volume: 
   veracrypt -t -d /mnt/veracrypt1


