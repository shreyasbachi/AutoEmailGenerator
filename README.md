# AutoEmailGenerator
This project is an automatic email response generator tailored for content creators, designed to streamline their workflow by efficiently handling collaboration requests via email. Leveraging a custom dataset, the system intelligently processes incoming emails to identify potential collaboration opportunities. Upon detection, it automatically crafts and sends personalized responses, ensuring timely and relevant communication with potential collaborators. This solution not only saves time but also enhances the engagement process, allowing content creators to focus more on their creative work while maintaining productive partnerships.

## Description
This Python-based project aims to streamline email handling by automatically checking for new unread emails, processing these emails to extract key information (such as sender details, subject, and body), and generating responses based on specific criteria. It leverages various Python libraries including `imaplib`, `smtplib`, `email`, `re`, `json`, `openai`, and `dotenv` for email interaction, data processing, and utilizing OpenAI's GPT models for crafting email responses.

## Getting Started
Install the source code, the user data set, and both the prompt .txt files in your directory.

### Dependencies
* Python 3.x
* A Gmail account or any IMAP/SMTP compatible email service. Configure SMTP settings according to your email provider's requirements if not using Gmail.
* An OpenAI API key (Note: Access to OpenAI's API is required for generating responses. Be aware that obtaining an OpenAI API key may incur costs.)

### Required Libraries
Install the required libraries using pip:
pip install openai==0.28 python-dotenv
You can also run this command in the code provided.

### Setting up Environment Variables
Create a .env file in the project's root directory.
**Note:** Since Google changed its security policy, for SMTP and IMAP libraries to access your email, you need to enable 2FA for your Gmail account and generate an app password.
That app password can be used in the .env file.
Add your OpenAI API key and email credentials:

OPENAI_API_KEY='your_openai_api_key_here'
EMAIL_USER='your_email_address_here'
EMAIL_PASS='your_email_password_here'

## Usage
Email Reading and Processing: The script checks the email inbox for unread emails, and processes any found to extract key information.
Response Generation: For emails that meet specified criteria, the script uses OpenAI's GPT model to generate a response.
Sending Emails: If classified as requiring a response, the script crafts and sends a reply.

## Customization
You can modify the email selection criteria, the user's data set, the template for generating responses, and SMTP settings to fit your project's needs.
Email Selection Criteria: Adjust the criteria variable and the process_email function to change how emails are selected for processing.
Response Generation: Customize the prompt.txt and prompt2.txt templates to alter the email responses generated by the script.

## Contributing
Contributions to this project are welcome! Please fork the project and submit a pull request with your improvements.

## License
This project is licensed under the Apache 2.0 License - see the LICENSE.md file for details.



