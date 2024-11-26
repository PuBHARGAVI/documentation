---
hidden: true
---


# Page 1





FAQs about Inji : MOSIP’s Digital Credentialing Stack

\
\


General Questions on Inji:

\


1. What are Verifiable Credentials (VCs)?

A [verifiable credential](https://www.w3.org/TR/vc-data-model-2.0/#dfn-verifiable-credential) can represent all the same information that a physical [credential](https://www.w3.org/TR/vc-data-model-2.0/#dfn-credential) represents. Adding technologies such as digital signatures can make [verifiable credentials](https://www.w3.org/TR/vc-data-model-2.0/#dfn-verifiable-credential) more tamper-evident and trustworthy than their physical counterparts. In short, VCs are secure digital certificates that can be verified cryptographically. They represent identity documents, degrees, or other trusted information.&#x20;

<!--

2. What are issuers, holders, and service providers?

* Issuers: Organizations that create and issue VCs (e.g., universities, governments).
* Holders: Individuals or entities who manage their credentials (e.g., Inji Wallet users).
* Service Providers (Verifiers): Entities that verify the credentials (e.g., employers, agencies).

3. How does Inji integrate with third-party services?\
   Inji supports integration with third-party services like government, healthcare, and educational platforms through open standards and APIs.
4. What is the modularity of the Inji Stack?\
   Inji Stack is modular, meaning each component can function independently or as part of the broader ecosystem. It also works with other wallets.
5. What is Inji Stack?

Inji Stack is a suite of solutions for managing VCs, including:

* Inji Wallet: Store and manage VCs.
* Inji Verify: VC verification portal.
* Inji Web: Web-based interface for credential management.
* Inji Certify: Credential issuance platform.

6. What is JSON-LD?

JSON-LD is a format used for Verifiable Credentials, enabling linked data that can be interoperable across systems.

7. What is mDoc/mDL?

A data structure that is part of the ISO/IEC 18013-5:2021 standard for mobile driver's licenses (mDL). mDoc is based on the CBOR binary format

8. What is SD-JWT?

A format that allows for selective disclosure of verifiable credentials, which means that the holder can choose to share only specific information. SD-JWT is based on the JSON Web Token (JWT) standard

9. What is BLE?

BLE (Bluetooth Low Energy) is a wireless technology for secure short-range data exchanges, useful for offline VC sharing or verification.

10. How does Inji ensure data security and privacy?\
    Inji uses encryption and global privacy standards, giving users full control over their data, which is only shared when users provide explicit consent.

\


Inji Certify:

1\. What is Inji Certify?

Inji Certify is a backend platform  that enables organizations to issue, manage,bind,sign and revoke Verifiable Credentials (VCs) based on open standards. It ensures data security, authenticity, and interoperability.

\
\


2\. What standards does Inji Certify support?

Inji Certify adheres to W3C Verifiable Credentials Data Model 1.1 and 2.0 standards. It also supports the OpenID specification, ensuring compatibility and interoperability with other compliant systems and platforms.

3\. What credential formats does Inji Certify support?

Inji Certify supports multiple credential formats, including:

* JSON-LD (JavaScript Object Notation for Linked Data)&#x20;
* SD-JWT (Selective Disclosure JSON Web Token)
* Future support is planned for additional formats, including mDoc and mDL (mobile driver's license).

4\. What is the revocation mechanism in Inji Certify?

Inji Certify provides will provide a  robust revocation mechanism to maintain the integrity of issued credentials. This includes:

* A revocation list to track invalidated credentials.
* API interfaces that allow issuers to revoke credentials and verifiers to check their status.
* A Discovery API for accessing the latest revocation data to ensure accurate verification.

5\. How does Inji Certify ensure interoperability with other platforms?

Inji Certify follows OpenID specifications and integrates with decentralized identity systems, ensuring that verifiable credentials issued via Inji Certify can be used and verified by other compliant systems. This makes it interoperable with various ecosystems, promoting wide adoption of verifiable credentials.

6\. What plugin support does Inji Certify offer?

Inji Certify supports custom plugins to integrate additional functionality. Currently supported plugins include:

* Sunbird Plugin
* Mock IDA Plugin
* MOSIP Identity Plugin

Users can integrate custom plugins by following the guidelines provided in the Inji Certify [Repository](https://github.com/mosip/inji-certify/tree/v0.9.0?tab=readme-ov-file#properties-for-custom-use-case).

7\. Can multiple issuers be onboarded on a single Inji Certify instance?

Yes, Inji Certify supports a multi-tenancy model, allowing multiple issuers to be onboarded and operate on a single instance. Each issuer can securely issue and manage credentials, while the platform ensures data security and segregation between different issuers.

8\. What is the role of eSignet VCI in Inji Certify?

eSignet VCI, now known as Inji Certify Core, is a microservice for secure  issuance of verifiable credentials. It ensures compliance with OpenID Connect protocols, enhancing secure credential issuance and verification across systems.

9\. How does the segregation of eSignet VCI benefit Inji Certify?

The segregation of eSignet VCI into Inji Certify Core provides several advantages:

* Specialization: Each module focuses on its primary function—Inji Certify on credential issuance and eSignet on secure authentication and verification.
* Scalability: Both components can scale independently, ensuring better performance under varying loads.
* Maintenance: Updates and security patches can be applied independently, minimizing downtime.

10\. How does Inji Certify handle database integration for issuing credentials?

* Inji Certify allows issuers to connect with their existing databases, provided the database has a primary key for each record and user authentication data (e.g., phone number, email). Credentials are issued based on this data, following the configured credential schema.

12\. How can organizations customize credential schemas in Inji Certify?

* Issuers can configure their own credential schemas within Inji Certify, allowing for flexibility in issuing various types of credentials. These schemas align with the W3C VC v1.1 standards, ensuring that credentials are interoperable and verifiable by other systems.

13\. Does Inji support decentralized identifiers (DIDs)?

* Yes, Inji Certify support  web-based DID, or did:web, is a decentralized identifier (DID) that's created and resolved using a web server. DIDs are globally unique identifiers that can be used to identify individuals, companies, and devices. They're a new type of identifier that allows for verifiable, decentralized digital identities.

\


Inji Wallet:

1. What is Inji Wallet?
2.
   * Inji Wallet is a self-sovereign wallet for storing, managing, and sharing verifiable credentials (VCs) across sectors like healthcare, education, and government services.
3. How does Inji Wallet ensure interoperability with other wallets?
4.
   * Inji Wallet follows global standards like W3C Verifiable Credentials and OpenIDVCI,OpenIDVP, ensuring compatibility with other digital wallets.
5. Can Inji Wallet be used without smartphones or internet access?
6.
   * Yes, Inji supports both digital and paper credentials, allowing access without smartphones or stable internet connectivity.
7. How does Inji Wallet support secure offline verification?
8.
   * Inji Wallet allows for offline sharing of VCs via Bluetooth Low Energy (BLE), ensuring secure transactions without an internet connection.
9. What is data backup, and why should I take a backup?
10.
    * Data backup creates a copy of your verifiable credentials in cloud storage (Google Drive/iCloud), safeguarding them against data loss.
11. What types of credentials can Inji Wallet store?\
    Inji Wallet supports a wide range of verifiable credentials including identity documents, educational certificates, health records, and more.
12. How to add a card?
13.
    * Instructions for downloading verifiable credentials (VCs) into the wallet can be found within the [app's guide](https://docs.mosip.io/inji/inji-wallet/functional-overview/end-user-guide).
14. What is Mimoto?
15.
    * Mimoto is a BFF(Backend for Frontend) for Inji Wallet. It's being used to get default configuration, download verifiable credentials (VC) and activate VC.
    * It provides all necessary APIs to the Inji Wallet and acts as a proxy for resident services. Mimoto gets the request from Inji Wallet, performs all the validations and forwards it to respective services. To get more detailed understanding please click[ here](https://docs.mosip.io/inji/inji-wallet/technical-overview/backend-services/mimoto)
16. What are components are integrated with Inji Wallet?
17.
    * Tuvali - Sharing via BLE
    * Face Match
    * Secure Keystore
    * BLE Verifier
    * PixelPass

To get more detailed understanding please click [here](https://docs.mosip.io/inji/inji-wallet/technical-overview/integration-guide).

\
\
\
\


#### Inji Web:

1\. What is Inji Web?

* &#x20;Inji Web is a user-friendly web-based platform designed to allow users to securely download, store, manage, and share Verifiable Credentials (VCs). Like a digital wallet, it empowers users to access their credentials through a simple and intuitive web interface. It's especially useful for users who may not have access to smartphones but still need to manage their digital credentials.

2\. How do I access Inji Web?&#x20;

* To access Inji Web, simply visit the designated [portal](https://injiweb.collab.mosip.net/) using any browser. Once there, you can authenticate yourself using relevant information such as a National ID, registration number, or other personal details, and then download or manage your credentials.

3\. What types of credentials can be managed on Inji Web?

* &#x20;Inji Web allows users to download, store, and share various types of verifiable credentials, such as identity documents, academic credentials, employment verification, and more. It is designed to accommodate a wide range of use cases for both individuals and organizations.

4\. How does the credential download process work?&#x20;

* After selecting an issuer and credential from the portal, users authenticate themselves with personal information. Upon successful validation, the Verifiable Credential is downloaded as a PDF file that includes a QR code for easy verification.

5\. Can I share my credentials through Inji Web?&#x20;

* Yes, you can share your credentials with third parties (relying parties) through various methods, such as providing a physical copy of the credential, scanning the QR code, or uploading the PDF to a verifier's site for instant verification.

6\. What technologies power Inji Web?

* &#x20;Inji Web is built using the React framework and employs [Mimoto](https://docs.mosip.io/inji/inji-wallet/technical-overview/backend-services/mimoto) as the Backend for Frontend (BFF). The credentials generated and managed by Inji Web comply with the Verifiable Credentials (VC) Data Model.

7\. Can I use Inji Web with multiple identity providers (IdPs)?&#x20;

* Yes, Inji Web is designed to be compatible with the OpenID protocol, which allows users to onboard various identity providers (IdPs). This gives users more flexibility and options when choosing VC issuers and managing their credentials.

8 . Does Inji Web support QR code-based verification?&#x20;

* Yes, each credential downloaded from Inji Web comes with a QR code, which can be scanned by service providers for verification, making the process faster and more secure.

9\. Can I use Inji Web without a smartphone?&#x20;

* Yes, one of Inji Web's primary goals is to empower individuals to manage and share their credentials even without access to a smartphone, making it an inclusive tool for various users.

10\. How does Inji Web ensure the validity of my credentials?&#x20;

* Inji Web ensures the integrity of digital signatures provided by issuers for each ID before Verifiable Credentials are downloaded as PDFs within the system

11\. How can I download a credential in Inji Web?

* Step 1: Search and choose an issuer, then select a credential type.
* Step 2: On the authentication page, provide required details.
* Step 3: Download the verifiable credential in PDF format.

12\. What details do I need to provide to download my credential?

* Required details such as UIN/VID or other identifiers like policy number, name, and date of birth, depending on the type of credential.

Inji Verify:

1\. What is Inji Verify?

* Inji Verify is a portal that allows users to validate and verify credentials through QR codes. Users can scan QR codes or upload QR code images to retrieve detailed credential information in real-time. The platform employs advanced algorithms and cryptographic techniques to ensure the authenticity and integrity of the credentials.It is coming up with verifiable presentation request.

2\. How do I use Inji Verify to scan a QR code?

* Users can scan a QR code using the camera on their smartphone or computer, making it versatile across devices. Once scanned, the credential information is retrieved and displayed instantly.

3\. Can I upload a QR code image for verification instead of scanning it?

* Yes, Inji Verify allows users to upload images containing QR codes. You can upload formats like JPEG, JPG, PNG, and PDFs with embedded QR codes. The system will decode the QR code using the PixelPass library and verify the credential.

4\. What information does Inji Verify display after scanning or uploading a QR code?

* After successfully scanning or uploading a QR code, Inji Verify displays detailed information about the credential, such as the name, date of birth, gender, expiration date, and any associated claims to a particular credentials. All this information is presented in a secure and user-friendly interface.

5\. What devices are compatible with Inji Verify?

* Inji Verify is compatible with a wide range of devices, including desktops, laptops, and mobile devices. It features a mobile-responsive version with back camera support for smartphones, and tablet support is currently under development.

6\. How does Inji Verify ensure the authenticity of a credential?

* Inji Verify uses advanced cryptographic algorithms and the PixelPass library to validate that a QR code has not been tampered with. The system provides real-time verification feedback, giving users confidence in the integrity of the credential.

7\. Does Inji Verify support CBOR-encoded QR codes?

* Yes, Inji Verify can now decode CBOR-encoded QR codes using the PixelPass library.

8\. How secure is Inji Verify?

* Inji Verify employs encryption techniques to ensure that all credential data and sensitive information are securely transmitted to the verifier. The platform prevents unauthorized tampering and guarantees that the credential is legitimate before displaying it.

9\. Can Inji Verify be used on mobile devices?

* Yes, Inji Verify is optimized for mobile use, with a mobile-responsive version that allows users to scan QR codes using their smartphone's back camera. This ensures that users can verify credentials conveniently on the go.

10\. What happens if the credential is invalid or has been tampered with?

* If the credential is invalid or the QR code has been tampered with, Inji Verify will provide instant feedback, alerting the user that the credential cannot be verified. This ensures the integrity of the credential data.

11\. How does the new user flow for sharing credentials work?

* The updated flow allows users to download a VC as a PDF or have a physical copy from Inji Web. When scanning the QR code through Inji Verify, the user is redirected to Inji Web for authorization. Inji Web then retrieves the VC in Verifiable Presentation (VP) format and Inji Verify completes the verification process.

\
\


12\. What error handlings have been introduced for Verifiable Presentations (VPs)?

* Comprehensive error handling scenarios, based on the OpenID4VP specification, have been implemented to ensure a robust experience during VP transactions. These scenarios gracefully handle issues like invalid credentials, expired tokens, or other transaction-related errors, providing informative messages to guide users.

\
\
\
\




Test after markdown file deletion&#x20;

-->