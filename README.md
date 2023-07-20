# Birthday Ecard Generator

This PHP code represents a Birthday Ecard Generator, a web application that allows users to create and send personalized birthday ecards. The application uses WordPress actions and AJAX to handle form submissions and image processing.

## Features

- Allows users to input their title, surname, first name, date of birth, email, phone, and upload personal and family images.
- Dynamically selects a random or predefined template for the birthday ecard.
- Creates a transparent overlay with celebrant details and date of birth on the ecard.
- Resizes and combines personal and family images with the template to generate the final birthday ecard.
- Sends the generated birthday ecard via email to the celebrant if it's their birthday today or if the user is an admin.

## How to Use

1. Ensure that you have WordPress installed and activated the plugin containing this code.
2. The following hooks are available for use in the plugin:
   - `generate_birthday_ecard`: Used to generate a birthday ecard for the current date (if any celebrants have their birthday today).
   - `wp_ajax_birthdayReminder`: Handles the AJAX request for creating and sending the birthday ecard.
   - `wp_ajax_nopriv_birthdayReminder`: Handles the AJAX request for creating and sending the birthday ecard for non-logged-in users.
3. The main function `birthdayReminder()` is responsible for processing the form data and generating the birthday ecard. It performs the following steps:
   - Validates and sanitizes the form inputs.
   - Determines the ecard template to use.
   - Checks for valid image uploads.
   - Saves the uploaded images and celebrant data in the database.
   - Generates and sends the birthday ecard via email.

## Templates

The birthday ecard templates are represented by numbers from 1 to 10. Each template has a unique layout for combining personal and family images with an overlay and celebrant details. The placement of images and text on the templates is configured based on the selected template number.

## Dependencies

This code utilizes the GD extension of PHP for image manipulation. Ensure that GD is enabled on your server to use this application effectively.

## Notes

- The code includes error handling for missing or invalid form data.
- The application sends the generated birthday ecard via email to the celebrant on their birthday. The email is sent to the email address provided in the form.
- The sender's name and email are set to default values but can be overridden through form inputs if desired.

Please ensure that you have a proper understanding of PHP, WordPress, and web development before using this code in a production environment. Make necessary adjustments to fit your specific use case and requirements.

---
*Please note that this is just a comprehensive README. You should still have the necessary environment, setup, and understanding of PHP and WordPress development to make the code functional and secure.*
