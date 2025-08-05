# Daily AI Article Agent

The `Daily AI Article Agent` is an automated workflow designed to generate and distribute daily AI articles. This agent combines topic research, content generation, and email formatting to deliver concise and impactful updates about the latest developments in the field of Artificial Intelligence. It is implemented using n8n, a workflow automation tool.

## Features

1. **Daily Scheduling**:
   - The workflow triggers every day at 7 AM, ensuring timely delivery of AI news updates.

2. **AI Topic Research**:
   - Utilizes the Perplexity API to find the most interesting and impactful AI-related development from the past 7 days.
   - Focuses on recent advancements that are relevant and engaging.

3. **Content Generation**:
   - Employs advanced AI models like Anthropic's Claude and custom agents to generate well-written, concise, and easy-to-understand articles.
   - Articles are tailored for non-technical audiences while maintaining depth and accuracy.

4. **Email Formatting**:
   - Converts the generated article into a polished email-ready format using Markdown processing.
   - Supports emoji and HTML tag escaping for enhanced readability.

5. **Automated Email Delivery**:
   - Sends the formatted article directly to subscribers via Gmail integration.

## Workflow Components

### 1. Schedule Trigger
   - **Node**: `Schedule Trigger`
   - **Description**: Triggers the workflow daily at 7 AM.
   - **Purpose**: Ensures consistent and timely execution of the workflow.

### 2. Topic Research
   - **Node**: `Perplexity - Blog Topic Research Node`
   - **Description**: Fetches recent and impactful AI developments from the past week.
   - **Purpose**: Identifies the topic for the daily article.

### 3. Content Generation
   - **Node**: `AI Agent (Enhanced)`
   - **Description**: Generates a concise and engaging article using advanced AI language models (e.g., Claude by Anthropic).
   - **Purpose**: Converts complex AI topics into accessible content for a broad audience.

### 4. Email Formatting
   - **Node**: `Convert to Email Format`
   - **Description**: Processes the generated article into a clean email format using Markdown-to-HTML conversion.
   - **Purpose**: Prepares the article for professional email delivery.

### 5. Email Delivery
   - **Node**: `Send Email`
   - **Description**: Sends the formatted article to the subscriber list via Gmail.
   - **Purpose**: Automates the distribution of daily AI updates.

## Workflow Diagram

```
[Schedule Trigger] --> [Topic Research] --> [Content Generation] --> [Email Formatting] --> [Email Delivery]
```

## Technical Details

- **Platform**: [n8n](https://n8n.io/)
- **APIs Used**:
  - Perplexity API for topic research
  - Anthropic API for content generation
- **Email Integration**:
  - Utilizes Gmail OAuth2 for secure and reliable email delivery.
- **Markdown Processing**:
  - Converts content using Markdown-to-HTML with support for emojis and HTML tag escaping.

## How to Use

1. **Setup**:
   - Clone the repository and import the n8n workflow JSON file.
   - Configure API credentials for Perplexity and Anthropic within n8n.
   - Set up Gmail OAuth2 credentials for email delivery.

2. **Run the Workflow**:
   - Deploy the workflow in n8n.
   - Ensure the schedule trigger is set to daily execution at 7 AM.

3. **Receive Updates**:
   - Subscribers will receive daily AI articles directly in their inbox.

## Customization

- **Content**:
  - Modify the topic research prompt in the Perplexity node to target specific AI subfields or themes.
- **Delivery Time**:
  - Adjust the schedule trigger to change the daily delivery time.
- **Formatting**:
  - Customize the Markdown-to-HTML conversion options for a different email style.

## Example Output

Here is a sample of what a subscriber might receive:

> **Subject**: Your Daily AI News Piece!
>
> **Content**:
>
> 🌟 **Breakthrough in AI!**
>
> Scientists have developed a novel AI algorithm that improves the accuracy of weather predictions by 30%. The model uses advanced neural networks trained on global climate data, providing more reliable forecasts than ever before.
>
> Stay tuned for more updates tomorrow!

## License

This project is part of the [Personal AI Agents](https://github.com/daher928/ai-agents-personal-projects) repository and is licensed under the MIT License.

---

For questions or contributions, feel free to open an issue or contact the repository owner.
