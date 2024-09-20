# Social Media Generator for Obsidian

## Introduction

Welcome to the **Social Media Generator** tool for Obsidian! This DataviewJS script leverages AI to create engaging social media content directly from a note. Whether you're crafting posts for LinkedIn, Instagram, YouTube, or generating image descriptions, this tool streamlines content creation, saving you time and enhancing your online presence.

## Prerequisites

Before setting up the Social Media Generator, ensure you have the following:

- **Obsidian**: Installed on your device. [Download Obsidian](https://obsidian.md/)
- **Dataview Plugin**: Essential for running DataviewJS scripts.
- **API Key (Supported AI Provider Account)**:
  - **OpenRouter**
  - **Anthropic**
  - **Gemini**
  - **LM Studio** (Local Server)

## Installation

### a. Install the Dataview Plugin

1. **Open Obsidian** and navigate to **Settings** (gear icon).
2. In the left sidebar, click on **Community Plugins**.
3. Toggle **Safe Mode** to **OFF** to allow third-party plugins.
4. Click on **Browse**.
5. Search for **Dataview**.
6. Click **Install**, then **Enable** once the installation completes.
7. **Enable JavaScript Queries** and **Enable inline Javascript queries**:
   - Go to **Settings** > **Dataview**.
   - Toggle **Enable Javascript Queries** and **Enable inline Javascript queries** to **ON**.

### b. Add the Social Media Generator Script

1. **Locate the Markdown File**: Find the `.md` file containing the Social Media Generator code block from the provider you prefer.
2. **Copy the Entire Code Block**: Ensure you include the backticks and `dataviewjs` tag. It should look like this:

   ```dataviewjs
   // Social Media Generator script goes here
   ```

4. **Paste into Your Note**: Open the Obsidian note where you want to use the Social Media Generator and paste the entire code block.

## Configuration

### Insert Your API Key

At the top of the pasted DataviewJS code block, you'll find a placeholder for your API key. Replace the placeholder with your actual API key from your chosen provider.

**Example:**

```javascript
const OPENROUTER_API_KEY = "YOUR_OPENROUTER_API_KEY_HERE";
// Replace "YOUR_OPENROUTER_API_KEY_HERE" with your actual OpenRouter API key
```

**Note:** If you're using **LM Studio**, refer to the [LM Studio Configuration](#lm-studio-configuration) section below.

## Customization

### Updating Prompts

The effectiveness of the Social Media Generator largely depends on the prompts provided. The prompt provided is for Synaptic Labs, so you will want to customize them to fit your specific content creation needs.

1. **Locate the Prompt Section**: Within the script, find the switch-case blocks for different social media platforms.
2. **Modify Prompts**: Adjust the instructions to better suit the specific social media platform's tone and requirements.

**Example: Customizing LinkedIn Prompt**

```javascript
case 'LinkedIn':
    prompt = `Professor Synapse, I need your help creating a LinkedIn post for Synaptic Labs. Ensure the content is professional, insightful, and encourages engagement.

    Text:
    ${content}`;
    break;
```

### Adding New Platforms

If you wish to support additional social media platforms, add new cases within the `generateSocialMedia` function.

```javascript
case 'Twitter':
    prompt = `Professor Synapse, craft a concise and engaging Twitter thread based on the following content.

    Text:
    ${content}`;
    break;
```

## Usage

### Adding the Social Media Generator to a Note

1. **Open a Note**: Navigate to the note where you want to use the Social Media Generator.
2. **Ensure DataviewJS Block is Present**: The script should be within a DataviewJS code block as described in the [Installation](#installation) section.

### Generate Social Media Content

1. **Click Generate Button**: A **Generate Social Media** button (typically styled with your chosen colors) appears at the top or within the DataviewJS block.
2. **Initiate Generation**:
   - Click the **Generate Social Media** button.
   - The button changes to indicate processing (e.g., "Generating...").
3. **Review Generated Content**:
   - A modal appears displaying generated content for each platform (e.g., LinkedIn, Instagram, YouTube).
   - Each section contains editable text areas allowing you to refine the content as needed.
4. **Insert Content**:
   - **Add Text**: Click to insert all generated content into your note, typically under a designated section like `# Social Media`.
   - **Revise**: Click to regenerate content with new instructions.
   - **Cancel**: Dismiss the modal without making changes.

## Example Prompt for LLM

If you wish to customize or extend the script using an LLM (e.g., ChatGPT), here's how you can proceed:

**Prompt Example:**

> "I have a DataviewJS script for a Social Media Generator in Obsidian. The script includes API integrations with OpenRouter, Anthropic, Gemini, and LM Studio. At the top of each script, there's a placeholder to insert the API key. I want to update the social media prompts to align more closely with our brand's voice and add functionality to schedule posts. Please modify the script accordingly, ensuring that the API key section remains clearly defined and provide comments where changes were made."

**Steps:**

1. **Feed the Dataview Code Block and Prompt**: Provide the existing script along with the above prompt to the LLM.
2. **Review Changes**: The LLM will update the prompts and add the requested scheduling feature.
3. **Implement Updates**: Copy the modified script back into your Obsidian note within the DataviewJS code block.

## Support and Contributions

We welcome your contributions and feedback!

- **Discussion Forum**: Join the conversation on our discussion section.
- **Issues and Feature Requests**: Submit them via the GitHub Issues page.
- **Contribute**: Fork the repository, make your changes, and submit a pull request. We're excited to collaborate and improve together!
