*Intuz — Your automation partner, one workflow at a time.*

<p align="center">
  <picture>
    <img alt="Banner Image" src="https://github.com/user-attachments/assets/210f97fc-0fce-404a-b647-7dfe1302cd37" />
  </picture>
</p>

[Intuz](https://www.intuz.com) helps organizations orchestrate AI, automation, and enterprise systems through scalable workflows. Our repository showcases proven implementations across healthcare, operations, customer support, document processing, sales, and back-office functions, enabling teams to accelerate automation initiatives without starting from scratch.

[N8N Creator](https://n8n.io/creators/intuz/) · [AI Agent Development Company](https://www.intuz.com/ai-agents-for-business-automation/) · [n8n Workflow Automation](https://www.intuz.com/workflow-automation-services/) · [For Custom Workflow Automation](https://www.intuz.com/get-started/)

# Chat with PDFs on Telegram using Google Gemini and Pinecone

## Quick overview

This workflow lets users upload PDFs or ask questions in Telegram, indexes PDF content in Pinecone using Google Gemini embeddings, and answers follow-up questions with a Google Gemini chat model using retrieval-augmented generation formatted for Telegram HTML.

## How it works

1. Triggers when a new Telegram message is received by your bot.
2. Checks whether the message includes a document; if it does, it downloads the file from Telegram and forces the binary metadata to application/pdf.
3. Splits the PDF text into overlapping chunks, generates embeddings with Google Gemini, and inserts the vectors into a Pinecone index.
4. Sends a Telegram confirmation message indicating how many PDF pages were saved to Pinecone.
5. If the message is a text question, retrieves relevant context from the Pinecone index and uses the Google Gemini chat model to generate an answer constrained to that context.
6. Sends the generated answer back to Telegram using HTML parse mode formatting.

## Setup

1. Create a Telegram bot with BotFather and add Telegram credentials in n8n for the Telegram Trigger and Telegram nodes.
2. Add a Google Gemini (PaLM) API credential for both the embeddings and chat model nodes.
3. Set up a Pinecone account, create (or select) an index named `telegram`, and add your Pinecone credentials in n8n.
4. Activate the workflow and start a chat with your Telegram bot to upload a PDF for indexing and then send text questions to query it.

## Requirements

- n8n Instance & Required Nodes: An active n8n account (Cloud or self-hosted).
- Telegram Account: A Telegram bot created via the BotFather, along with its API token.
- Google Gemini AI Account: A Google Cloud account with the Vertex AI API enabled and an associated API Key.
- Pinecone Account: A Pinecone account with an API key.

## FAQ

**What does this workflow do?**  
It allows users to upload PDFs or ask questions in Telegram, indexes PDF content in Pinecone using Google Gemini embeddings, and answers questions with a Google Gemini chat model.

**What services are required to use this workflow?**  
You need a Telegram bot, Google Gemini API credentials, a Pinecone account, and an active n8n instance.

**How does the workflow handle PDF files?**  
It downloads PDFs from Telegram messages, splits the text into chunks, generates embeddings with Google Gemini, and stores them in a Pinecone index.

## Related n8n templates from Intuz

- [Utilities to Manage AWS Snapshots](https://github.com/Intuz-production/Utilities-to-Manage-AWS-Snapshots)
- [RealMWrapper is a simple component, which lets you use the Realm Database with a class that operate all the functions of the database in your project](https://github.com/Intuz-production/RealMWrapper-IOS)
- [Automatically generate GitHub pull requests and update the linked JIRA ticket directly from Git commits, for a single repository.](https://github.com/Intuz-production/Automate-GitHub-PRs-Jira-Updates-from-Git-Commits)

[See all of Intuz's free n8n templates](https://www.intuz.com/n8n-workflow-automation-templates/)

## Connect with us

Intuz is a USA-based AI & workflow automation company with 16+ years of experience building custom AI-enabled workflow automations for SMBs and Enterprises, specializing in agentic AI, LLM integrations, and CRM/ERP sync across Healthcare, FinTech, eCommerce, Manufacturing, and Real Estate.

* **Website:** [https://www.intuz.com](https://www.intuz.com)
* **Email:** [getstarted@intuz.com](mailto:getstarted@intuz.com)
* **LinkedIn:** https://www.linkedin.com/company/intuz/
* **Get Started:** https://n8n.partnerlinks.io/intuz

## For Custom Workflow Automation

[Click here - Get Started](https://www.intuz.com/get-started/)
