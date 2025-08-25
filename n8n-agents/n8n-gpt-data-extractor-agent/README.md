# n8n GPT Data Extractor Agent

An intelligent n8n workflow that extracts structured data from emails using GPT and stores the results in a database.

## Overview

This agent automates the process of extracting structured information from email content using OpenAI's GPT models. It processes incoming emails, identifies and extracts relevant data points, and stores the structured results in a database for further analysis and use.

## Features

- **Email Processing**: Automatically processes incoming emails
- **AI-Powered Extraction**: Uses GPT-4 to intelligently extract structured data
- **Database Integration**: Stores extracted data in PostgreSQL database
- **Flexible Configuration**: Easily customizable for different data extraction needs

## Workflow Components

1. **Email Trigger**: Monitors for new emails
2. **GPT Data Extractor**: Processes email content and extracts structured data using GPT-4
3. **Database Insert**: Stores the extracted data in PostgreSQL database

## Use Cases

- **Lead Generation**: Extract contact information and business details from inquiry emails
- **Order Processing**: Parse order details from customer emails
- **Support Ticket Analysis**: Extract key information from support requests
- **Invoice Processing**: Extract billing information from supplier emails
- **Survey Response Processing**: Structure feedback and survey responses

## Setup Requirements

- n8n workflow automation platform
- OpenAI API key for GPT-4 access
- PostgreSQL database connection
- Email service integration (Gmail, Outlook, etc.)

## Configuration

1. Import the `data_extractor_agent.json` workflow into your n8n instance
2. Configure the OpenAI credentials for GPT-4 access
3. Set up PostgreSQL database connection
4. Configure email trigger with appropriate filters
5. Customize the GPT prompt based on your specific extraction needs

## Database Schema

The agent expects a PostgreSQL table named `extracted_data` with the following structure:

```sql
CREATE TABLE extracted_data (
    id SERIAL PRIMARY KEY,
    email_subject VARCHAR(255),
    sender_email VARCHAR(255),
    extracted_json JSONB,
    processing_timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## Customization

Modify the GPT prompt in the workflow to extract specific data fields relevant to your use case. The agent is designed to be flexible and can be adapted for various email processing scenarios.

## Contributing

Feel free to customize and extend this workflow for your specific needs. If you make improvements, consider sharing them back to the community.

## License

This workflow is provided as-is for educational and development purposes.
