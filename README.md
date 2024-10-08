# VPN-connection-implementation

### Description
This project aims to establish a secure VPN connection between two networks for safe data transmission. It utilizes OpenVPN on Windows 11 and includes features like VPN setup, data encryption, and access control.

### Features
- **VPN Setup**: Configures a VPN connection between two networks.
- **Encryption**: Ensures secure data transmission using strong encryption protocols.
- **Access Control**: Implements user access controls and permissions to enhance security.

### Technologies Used
- **OpenVPN**: A robust open-source VPN solution.
- **EasyRSA**: A CLI utility for managing a public key infrastructure (PKI).

### Prerequisites
- **Windows 11**: This project is developed and tested on Windows 11.
- **Administrator Privileges**: You may need admin rights to install software and configure network settings.
- **Internet Connection**: Required for downloading OpenVPN and EasyRSA.

### Installation Guide
1. **Download OpenVPN**: Download the latest version of OpenVPN from the [official website] 
    (https://openvpn.net/community-downloads/).
2. **Install OpenVPN**: Follow the installation instructions provided on the website.
3. **Download EasyRSA**: Download EasyRSA from the [OpenVPN GitHub Releases] 
   (https://github.com/OpenVPN/easy-rsa/releases).
4. **Extract EasyRSA**: Unzip the downloaded EasyRSA file into the OpenVPN directory (e.g., 
   C:\Program Files\OpenVPN\easy-rsa`).

### Configuration Steps
1. **Open EasyRSA**: Navigate to the EasyRSA directory and run `EasyRSA-Start.bat` to open the command prompt for EasyRSA.
2. **Initialize PKI**: Run the following command:
   ./easyrsa init-pki
   ![image](https://github.com/user-attachments/assets/b1f3aaa7-1911-4d25-9e35-8af82ba8d83d)
3. **Ca.crt**: Run the following command:
   ./easyrsa build-ca nopass
   ![image](https://github.com/user-attachments/assets/61bbd4e7-4a99-4581-b299-a4b45a274130)
4. **Sever.certificate**: Run the following command:
   ./easyrsa build-server-full Server nopass
   ![image](https://github.com/user-attachments/assets/b2de1ed9-44f1-4216-81c1-d208775549dc)
5. **Client.certificate**: Run the following command:
   ./easyrsa build-client-full Client1 nopass
    ![image](https://github.com/user-attachments/assets/3552b7a3-5b6c-4623-b57d-d863a9d6aa3a)

### Testing the Connection

* Use the OpenVPN GUI to connect the server and client on the same laptop:
        + Open the OpenVPN GUI as an administrator.
        + Right-click on the server configuration file and select "Connect."
        + Right-click on the client configuration file and select "Connect."

* Verify Connection:
        You can verify the connection by checking the OpenVPN logs and ensuring the data     
         transmission is secure.

### Troubleshooting

* If you encounter any issues during installation or connection:
     + Ensure all software is installed correctly.
  
     + Check your firewall settings to ensure they allow OpenVPN traffic.
  
     + Review the OpenVPN log files for error messages.

### Documentation

    Ensure to maintain clear documentation for future reference and updates. You can refer to 
    the OpenVPN and EasyRSA documentation for advanced configuration options.

### Acknowledgments

    Special thanks to the OpenVPN and EasyRSA communities for their invaluable tools and 
    resources.
