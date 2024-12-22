# Track-PNL

## Description

The `Track-PNL` script is a Google Apps Script designed to extract financial data from Gmail messages and log it into a Google Sheet. Specifically, it retrieves the "Available Margin" and "Total" values from emails that match specified criteria, such as the sender's email address and the subject line. The extracted data is then organized in a Google Sheet for easy tracking and analysis.

## Features

- Automatically fetches emails based on specified sender and subject.
- Extracts "Available Margin" and "Total" values from the email body. **Note:** The text labels for these values may vary in different emails. Be sure to modify the regular expressions in the `extractMarginFromHTML` and `extractTotalFromHTML` functions to match the specific text labels used in your emails.
- Logs the extracted data into a Google Sheet with formatted dates.
- Supports profit and loss calculations based on the extracted total.

## How to Upload and Use the Code

1. **Open Google Sheets**:
   - Create a new Google Sheet or open an existing one.

2. **Access Apps Script Editor**:
   - Click on `Extensions` in the menu.
   - Select `Apps Script`.

3. **Copy and Paste the Code**:
   - Delete any existing code in the script editor.
   - Copy the provided code and paste it into the script editor.

4. **Modify the Code**:
   - Update the following variables in the `extractAvailableMargin` function:
     - `var emailAddress = "";` 
       - Replace with the email address of the sender you want to track.
     - `var subject = "";` 
       - Replace with the subject line you want to filter by (e.g., "Confirmation").
   - Adjust the regular expressions in the `extractMarginFromHTML` and `extractTotalFromHTML` functions if necessary to match the structure of the email body you are working with.

5. **Save the Script**:
   - Click on the disk icon or `File > Save` to save your script.

6. **Run the Script**:
   - Click on the play (▶️) button to run the `extractAvailableMargin` function.
   - You may need to authorize the script to access your Gmail and Google Sheets.

7. **Check the Google Sheet**:
   - After running the script, check the specified sheet (named "Table") in your Google Sheet to see the extracted data.

## Important Notes

- Ensure that the email format you are extracting from matches the regular expressions used in the script. You may need to adjust the regex patterns based on the actual HTML structure of the emails.
- The script currently logs data for the current date only. If you want to track data for different dates, you will need to modify the date comparison logic.
- The script assumes that the "Table" sheet already exists in your Google Sheet. If it does not, create a new sheet and name it "Table".

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
