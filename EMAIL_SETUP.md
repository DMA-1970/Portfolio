# Email Notifications Setup

Your Portfolio repository is configured to send email notifications to **david@abiodun.co.uk**.

## Required GitHub Secrets

To enable email notifications, you need to add the following secrets to your GitHub repository:

1. Go to: `https://github.com/DMA-1970/Portfolio/settings/secrets/actions`
2. Click "New repository secret"
3. Add these secrets:

### Required Secrets:

- **`SMTP_SERVER`** - Your SMTP server address
  - Gmail: `smtp.gmail.com`
  - Outlook: `smtp-mail.outlook.com`
  - Custom: Your SMTP server address

- **`SMTP_PORT`** - SMTP port number
  - Gmail: `587` (TLS) or `465` (SSL)
  - Outlook: `587`
  - Custom: Your SMTP port

- **`SMTP_USERNAME`** - Your email address or SMTP username
  - Example: `your-email@gmail.com`

- **`SMTP_PASSWORD`** - Your email password or app-specific password
  - For Gmail: Use an [App Password](https://support.google.com/accounts/answer/185833)
  - For Outlook: Use your password or app password

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

