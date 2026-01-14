🎙️ AI-Powered Voice Assistant for Automated Client Conversations

   Vanessa – Voice AI Acquisitions Agent

   Vanessa is an AI-powered voice assistant designed to autonomously call homeowners, detect seller intent, and 
   seamlessly transfer qualified leads to human acquisition agents. The project demonstrates how conversational AI, 
   telephony APIs, and workflow automation can be combined into a functional outbound voice agent.

   The system focuses on natural multi-turn conversations, fast lead qualification, and 
   automated CRM updates — all within short, controlled call durations.

   Some Conversation Examples:
   https://storage.vapi.ai/0199da1a-a246-7555-8b24-6d1306ae11de-1760300889547-b3dc1413-9450-452c-be08-251831bb451a-mono.wav
   https://storage.vapi.ai/0199da1e-24ca-766c-82b6-9f613f1b7fbb-1760301086730-e217b630-14ac-4e8e-9ecd-b3a4bcc80ac2-mono.wav
   https://storage.vapi.ai/0199da21-b2db-7dd9-824a-dda2ec77a0a3-1760301301251-a7f9be83-a1bb-42cf-85b6-ac9df679e01d-mono.wav

✨ Features

- Automated outbound calls to homeowners
- Natural, multi-turn voice conversations (non-robotic)
- Seller intent detection within ~90 seconds
- Live call transfer to human acquisition agents for qualified leads
- Structured data capture:
  - Owner status
  - Price range
  - Timeline to sell
  - Property condition
- Intelligent call branching:
  - Qualified Seller → live transfer
  - Call Back Later
  - Not Interested
  - Do-Not-Call / Removal Requested
  - Not Connected
- Automatic call summaries and lead classification
- Call recording storage and CRM logging

🧠 Tech Stack

- Voice & Telephony: Vapi.ai, Twilio
- Speech Synthesis: ElevenLabs
- Automation: n8n
- LLM Analysis: OpenAI (GPT-4o-mini)
- Data Store / CRM: Google Sheets

🏗️ System Architecture (High-Level)

1. Leads are stored in Google Sheets with status Not Connected
2. n8n triggers outbound calls via Vapi + Twilio
3. Vanessa conducts a natural, persona-based conversation
4. Seller intent is detected in real time
5. Qualified sellers are transferred live to a human agent
6. The call transcript is analyzed using an LLM
7. Structured summary and lead status are written back to Google Sheets

📞 Conversation Design

Vanessa acts as a friendly acquisitions assistant:
 - Warm, upbeat, confident tone
 - Light assertiveness — never pushy
 - Handles short conversational branches gracefully
 - Politely exits when: 
   - Owner is not interested
   - Callback is requested
   - DNC is requested

Calls remain under 180 seconds unless transferred to a human agent.

📊 Lead Classification

Each call is classified into one of the following:
 - Qualified Seller (Transferred Live)
 - Call Back Later
 - Not Interested
 - DNC / Removal Requested
 - Not Connected

⚙️ Workflow Details

- n8n orchestrates:
  - Lead batching and looping
  - Call initiation via Vapi API
  - Real-time call monitoring
  - Live transfer to human agents
  - Post-call transcript analysis
- OpenAI analyzes transcripts and returns strict JSON summaries
- Google Sheets is updated with:
  - Call summary
  - Lead status
  - Timestamp
  - Recording URL

🔮 Future Enhancements
- Advanced sentiment & confidence scoring
- CRM integrations (HubSpot / Airtable)
- Cost-aware dialing and throttling
- Multi-language voice support

🎯 Purpose

This project is demonstrating the ability to:
- Build voice-first AI systems
- Integrate telephony APIs
- Design conversational flows
- Orchestrate AI workflows with automation tools
-
- Blend AI autonomy with human-in-the-loop escalation
