# Send Thank-You Email When Google Forms Response Received

## Overview

This Zap automatically sends a personalized thank-you email to respondents whenever someone submits a response to your "Future Technologies Webinar" Google Form.

## How It Works

1. **Trigger:** A new response is submitted to the "Future Technologies Webinar" form in Google Forms
2. **Action:** An automated thank-you email is sent to the respondent's email address with a personalized greeting

## Workflow Steps

### Step 1: Google Forms - New Form Response
- **Form:** Future Technologies Webinar
- **Trigger Type:** Reads all new form submissions in real-time
- **Output Fields Used:**
  - `respondentEmail` - Respondent's email (auto-captured by Google Forms)
  - `4afcc3c2` (Email Address) - Email address entered in the form
  - `028f15ea` (Name-Surname) - Respondent's name for personalization

### Step 2: Gmail - Send Email
- **From:** totalainityyyainityyy@gmail.com
- **To:** Dynamically populated from form field `4afcc3c2` (Email Address)
- **Subject:** "About Future Technologies Webinar"
- **Body:** Personalized greeting with respondent's name

Hi {{respondent_name}},

Thank you for submitting your response. We appreciate your time and will review your submission shortly.

Best regards


## Requirements

### Connected Accounts
- ✅ **Google Forms:** Connected to your account
- ✅ **Gmail:** Connected to send emails from totalainityyyainityyy@gmail.com

### Form Configuration
- The Google Form must have:
  - An email collection field (ID: 4afcc3c2 - "Email Address")
  - A name field (ID: 028f15ea - "Name-Surname")

## Setup Instructions

1. **Connect Google Forms:** Ensure your Google Forms account is authenticated
2. **Connect Gmail:** Ensure your Gmail account is authenticated and can send emails
3. **Verify Form ID:** Confirm the "Future Technologies Webinar" form is selected as the trigger
4. **Test the Zap:** Submit a test form response to verify emails are being sent

## Testing

1. Submit a test response to your Google Form with:
   - A valid email address in the "Email Address" field
   - Your name in the "Name-Surname" field
2. Check the recipient's inbox for the thank-you email within 1-2 minutes
3. Verify the email is personalized with the respondent's name

## Email Mapping

| Field | Source | Format |
|-------|--------|--------|
| To | `4afcc3c2` | {{355578740__4afcc3c2}} |
| From | Static | totalainityyyainityyy@gmail.com |
| Subject | Static | About Future Technologies Webinar |
| Name in greeting | `028f15ea` | {{355578740__028f15ea}} |

## Important Notes

⚠️ **Email Field Required:** The "Email Address" form field (4afcc3c2) MUST contain a valid email address for the Zap to send successfully.

⚠️ **Form Responses Only:** This Zap only processes new form submissions. It does not retroactively send emails for previously submitted responses.

✅ **Dynamic:** The email is sent dynamically to each respondent based on their submitted email address—works for unlimited responses.

## Troubleshooting

### Issue: "Recipient address required" error
**Cause:** The email field in the form is empty or doesn't contain a valid email address.
**Solution:** Verify that form respondents are entering valid email addresses in the "Email Address" field.

### Issue: Email not received
**Cause:** The email may have been filtered to spam or blocked by Gmail.
**Solution:** 
- Check the recipient's spam/junk folder
- Verify the email address is correctly entered in the form
- Check the Zap's run history for error details

### Issue: Subject line not showing correctly
**Cause:** Subject line might be cut off or filtered.
**Solution:** The current subject is "About Future Technologies Webinar" - adjust in the Zap if needed.

## Customization

To modify this Zap:

1. **Change Email Subject:** Update the "Subject" field in the Gmail step
2. **Customize Email Body:** Edit the "Body" field to change the thank-you message
3. **Add More Fields:** Map additional form fields to the email body (e.g., company, phone number)
4. **Change Sender Email:** Update the "From" field to use a different Gmail address

## Performance

- **Trigger Frequency:** Real-time (within 1-2 minutes of form submission)
- **Task Usage:** 1 task per form response
- **Reliability:** Standard Zapier reliability with error retry

## Support

For issues or questions:
1. Check the Zap run history for detailed error logs
2. Verify all connected accounts are properly authenticated
3. Test with a new form submission
4. Review the troubleshooting section above

---

**Zap Status:** ✅ Published and Active  
**Created By:** Arda Ege Tunç  
**Last Updated:** 2025-01-16

This README provides:

✅ Clear overview of what the Zap does
✅ Step-by-step workflow explanation
✅ Requirements and setup instructions
✅ Testing procedures
✅ Field mapping reference table
✅ Troubleshooting guide
✅ Customization options
✅ Performance details
