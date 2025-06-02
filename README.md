# Answers
## 1. Can you describe how you’d structure an automated Make workflow that reads from our EMR via API and sends WhatsApp messages using pre-approved templates?
To outline the structure effectively, I’d need a few key clarifications:
- Which EMR system are you using? I’d need to review its API documentation and check if it supports webhooks for event-based triggers. If webhooks are not available, I can implement a polling mechanism to regularly fetch new data.
- What solution are you currently using for WhatsApp messaging? If you're using the official WhatsApp Business Cloud API, Make provides native modules for integration (e.g., WhatsApp Cloud via Make). If you're using a third-party provider, I'd need to assess their API capabilities, which is not a problem (I worked with a few).
- What’s the logic behind sending messages? If the message rules are straightforward (e.g., based on status or field values), I can implement them with filters and routers in Make. If decision-making depends on analyzing unstructured inputs (e.g., determining the correct template based on free-text notes entered by staff), I can incorporate lightweight AI models (such as GPT-4.1 mini or nano) to handle that logic cost-effectively.
This type of flow is similar to a recent project I completed: "AI Email Support Assistant (Make, OpenAI, Zoho)" — only here, the trigger source would be your EMR instead of email.


## 2. How do you minimize token costs when using GPT-4 API for summarizing patient charts?
I apply a few strategies:
- Pre-process data to remove irrelevant or repetitive information before passing it to the model.
- Use cheaper and smaller GPT-4 models (e.g., GPT-4.1 mini) for straightforward summarization tasks (we need to test how it goes in your situation).
- Limit context size dynamically based on the patient chart type and requested output.
- Cache (store somewhere) and reuse summaries wherever possible to avoid extra API calls.

## 3. Have you built any dashboards or alert systems that flag missed appointments or non-responsive staff?
- Yes, I’ve built numerous dashboards using Looker Studio, Power BI, and Google Sheets. These included triggers and alerts for missed calls, low review scores, budget overruns, etc.

## 4. Are you open to learning and applying WhatsApp compliance rules (template categories, message windows, utility vs. marketing)?
Of course, this will be another experience for me.

## 5. How comfortable are you working closely with our staff to train us on what you build and being there for future paid maintenance work?
No problem at all. If you’d like to bring maintenance in-house, I can provide documentation, onboarding sessions, and training for your staff. I’m also happy to remain available for ongoing paid support and improvements as needed.
