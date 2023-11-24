## Multipurpose Internet Mail Extension (MIME)
### Definition
- MIME is extension for [[Electronic Mail]]'s [[SMTP]] protocol
- MIME works on SMTP
- MIME is a framework to handle attachments
	- support formats other than ASCII such as audio, video, images, and application programs
### Properties
- Provide reliable delivery across various environments
- New message header included to RFC 822 header:
	1. **MIME-Version**:
		- Indicates the version of MIME that's being used. 
	2. **Content-Type**: 
		- Description fır the data (text, audio, video, image...)
	3. **Content-Transfer-Encoding**: 
		- Specifies the encoding used to safely transmit the content over SMTP, which handles only 7-bit ASCII text. 
		- [[MIME Transfer Encoding]]
	4. **Content-Description**: 
		- Plain text description fır the object in the body
		- Optional field -> if explanation for the attachment is need it will used
- Content Types:
	- **Text**
		- Unformatted plain text.
		- ASCII or ISO 8859 charset.
		- Alternative charsets can be specified in the Content-Type header field.
	- **Multipart**
		- Contains multiple, independent parts, each of a different type.
		- Separated by a defined boundary in the Content-Type header field.
		- Four subtypes:
			- Mixed: Parts bundled in a specific order.
			- Parallel: Order of parts is not significant.
			- Alternative: Same content in alternative representations.
			- Digest: Collection of messages.
	- **Message/RFC822**
		- An entire message as content, including headers and body.
		- Despite the name, embedded messages can be of any MIME type.
		- Mostly used during forwarding and e-mail
	- **Image**
	- **Video**
	- **Audio**
	- **Application**
		- Binary data for processing by an application.
		- Used for any file type as an attachment.
		- The subtype indicates the format, 
			- e.g., msword, postscript, pdf ...
