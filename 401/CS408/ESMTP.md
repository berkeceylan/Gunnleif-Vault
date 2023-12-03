## ESMTP (Extended Simple Mail Transfer Protocol):

- **Function**:
	- ESMTP is an extension of the original [SMTP](SMTP.md) (Simple Mail Transfer Protocol). 
	- It allows for the sending of email messages with added features not available in the original SMTP.
- **Crucial Additions**:
	- **Enhanced Authentication**:
		- Provides mechanisms for server and client authentication
		- Increase security
		- RFC 2554
	- **Support for Multimedia**:
		- With [MIME](MIME.md) (Multipurpose Internet Mail Extensions)
	- **Additional Commands**:
		- ESMTP introduces new commands that provide greater flexibility and functionality in mail transfer.
		- EHLO -> server returns supported extensions and STMP features
	- **Better Error Messages**:
		- Offers more detailed and informative error messages compared to SMTP, making troubleshooting easier.
	- **StartTLS Command**:
		- Allows for encrypting communications, enhancing the security of email transmissions.