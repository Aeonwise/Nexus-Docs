# Verify Installer

## **How to Verify Installer's Integrity:**

For better security, you can verify the integrity of the installer you’ve downloaded to make sure it’s original and hasn’t been tampered with. In order to do so, check the SHA-512 hash of the installer by following the instructions and compare the result you got with the correct hash provided below. If the hashes don’t match, please let Nexus team know about that.

## **How to get SHA-512 hash of a file**

### **On Windows**

1. Open Command Prompt (press _Windows + R_, type **cmd** into the textbox, then press _Enter_)
2.  Type this command:

    `certUtil -hashfile pathToFile SHA512`

    and press _Enter_ (replace \`pathToFile\` with the path to the file that you’ve downloaded)

### **On MacOS (OS X) and Linux**

1. Open Terminal
2.  Type this command:

    `shasum -a512 pathToFile`

    and press _Enter_ (replace \`pathToFile\` with the path to the file that you’ve downloaded)

### **SHA-512 Hashes – Nexus Wallet v3.0.6**

* Windows Installer\
  `91cc121e0f96191216ab1b9ecfecdb6e00c34b382bfa1f6089eee86ec4f6457ba6aebb3acabb387b0207265185c42bc815fd9b822025b66a8cae80abedd3c427`
* Windows Zip\
  `bf7266a62004f9c96f9353e6ab5c31bb9b756d6113183ce0c5acdfca6e0b773f7268477351dd214b2ed178dd9aa84df21aa85b9901b7fb4a50b63d30889a9f97`
* Mac OSX Installer\
  `38a1b4e9c467fe5899d22c8ae55b79f9dfac41ed9c415bb3221b296ca67064bffdb8942a54c15d933c38876ca446d231c78832bd0dd62c2bef60646abd959875`
* Mac OSX Unpacked\
  `b61c5afe174a0c6f1beb98213829f3233290757cb0a1edaad776020d1b60f4d588a5a3817880b8bc86234ddf4abde0c6e2f181f0dc0650726c7db3bc77420808`
* Linux Deb\
  `578fe99b9504bedb6a2202101a8f477013a3b289b38c3c847ba6c9dc5ecf76beee9656ab81c78d6a85d76a4f81124d4e1df475ad0f056789db6e666e4155c2bd`
* Linux AppImage\
  `77310d09385a179d55de09272db4c379de8f76bddc601bd3e446b6a8cfa4034f51e70bc4651d25559d6486ee0308985b3368685313bf1c529633ccf2b3c6af25`
* Linux Snap\
  `cb80e57632bd63e861cffcc525fa60ebad7dd0cfc00c55cb091fc37f143e65a63964e961f45c2143f440904a30195d0943e8c4576ec2a88f8e946f755d331acf`
