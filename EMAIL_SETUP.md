# Email Notifications Setup

Your Portfolio repository is configured to send email notifications to **david@abiodun.co.uk**.

## Required GitHub Secrets

To enable email notifications, you need to add the following secrets to your GitHub repository:

1. Go to: `https://github.com/DMA-1970/Portfolio/settings/secrets/actions`
2. Click "New repository secret"
3. Add these secrets:

### Required Secrets:

- **`SMTP_SERVER`** - Your SMTP server address for david@abiodun.co.uk
  - **If using Gmail/Google Workspace**: `smtp.gmail.com`
  - **If using Outlook/Microsoft 365**: `smtp-mail.outlook.com` or `smtp.office365.com`
  - **If using custom email provider**: Check with your email hosting provider
  - **Common providers**:
    - cPanel/WHM: Usually `mail.yourdomain.com` or `smtp.yourdomain.com`
    - Zoho: `smtp.zoho.com`
    - FastMail: `smtp.fastmail.com`

- **`SMTP_PORT`** - SMTP port number
  - **Gmail/Google Workspace**: `587` (TLS) or `465` (SSL)
  - **Outlook/Microsoft 365**: `587` (TLS) or `465` (SSL)
  - **Most providers**: `587` (TLS/STARTTLS) or `465` (SSL)

- **`SMTP_USERNAME`** - Your email address
  - **Use**: `david@abiodun.co.uk`

- **`SMTP_PASSWORD`** - Your email password or app-specific password
  - **Gmail/Google Workspace**: Use an [App Password](https://support.google.com/accounts/answer/185833) (not your regular password)
  - **Outlook/Microsoft 365**: Use your regular password or app password
  - **Custom providers**: Usually your regular email password

## Email Notifications Configured

### 1. Traffic Monitor Reports
- **Frequency**: Every 6 hours
- **Content**: Traffic statistics, site health, page accessibility
- **When**: Scheduled runs and manual triggers

### 2. Workflow Failure Alerts
- **Trigger**: When any workflow fails
- **Content**: Workflow name, status, and link to details
- **When**: Immediately after failure

### 3. Quality Check Failures
- **Trigger**: When quality checks fail
- **Content**: Summary of failed checks
- **When**: After quality check workflow completes with errors

## Alternative: Using Email Services

If you prefer not to use SMTP, you can use email services like:

- **SendGrid** (Free tier: 100 emails/day)
- **Mailgun** (Free tier: 5,000 emails/month)
- **AWS SES** (Pay as you go)

To use these services, you would need to modify the workflows to use their APIs instead of SMTP.

## Testing

After adding the secrets, you can test email notifications by:

1. Going to Actions → Traffic Monitor
2. Click "Run workflow"
3. Check your email (david@abiodun.co.uk) for the report

## Troubleshooting

- **No emails received**: Check that all secrets are correctly set
- **Authentication errors**: Verify SMTP credentials
- **Port issues**: Try different ports (587 for TLS, 465 for SSL)
- **Gmail**: Make sure to use an App Password, not your regular password

