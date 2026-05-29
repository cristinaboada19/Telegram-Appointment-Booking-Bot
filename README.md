# Clínica Aurora — Telegram Appointment Booking Bot

Clínica Aurora is a fictional clinic appointment booking system designed to simulate how a real business could manage client inquiries and appointment requests through an automated Telegram bot.
The goal of this project is to build a real-world automation workflow using Telegram, n8n, Supabase/PostgreSQL, SQL, an AI agent, and external knowledge documents.

This project simulates a client-facing bot for a clinic, medical office, beauty center, or wellness business.

## Project Goal

The main goal is to create a Telegram bot that allows clients to:

- Check available services
- View service prices and duration
- Ask general questions about appointments and policies
- Request an appointment
- Check their own appointment information
- Eventually cancel or reschedule their own appointment

This project is focused only on the client experience.

Clients can ask about:

- Services
- Prices
- Duration
- Availability
- Appointment requests
- General policies
- Cancellation and rescheduling information
- Basic care instructions
- General conditions of service

The bot must not provide internal or administrative information.

## Security and Access Rules

The public client bot must not reveal sensitive or internal information, such as:

- Full appointment schedule
- Total number of appointments
- Reports
- General appointment status
- Cancelled or rescheduled appointments from other clients
- Most requested services
- Other clients’ information
- Administrative data

## Tech Stack

This project uses:

- Telegram Bot
- n8n
- Supabase
- PostgreSQL
- SQL
- AI Agent inside the workflow
- Cohere API
- Embeddings
- Vector Store
- GitHub RAW files for RAG document loading

## How It Works

### RAG Document Loading Workflow

This project includes a first RAG loading workflow in n8n. It uses `.txt` files stored in GitHub and reads them through RAW URLs, allowing n8n to download and process the documents.

The goal of this workflow is to provide the AI agent with general clinic information, such as FAQs, terms and conditions, appointment policies, cancellations, rescheduling rules, payment details, and care instructions.

For now, this RAG flow is only used for static or general information. Dynamic information like services, clients, appointments, and real availability will be handled separately through Supabase/PostgreSQL.

### Test Chat Workflow

A second workflow was created to test the bot conversation inside n8n before connecting it to Telegram.

This workflow includes a chat trigger, an AI Agent, a Cohere chat model, simple memory, and the Simple Vector Store connected to the RAG documents loaded in the first workflow.

So far, the agent is responding well to general clinic-related questions. It can use the uploaded documents to answer about appointment requests, confirmation rules, cancellations, rescheduling, and general policies.

PostgreSQL/Supabase is not connected to this workflow yet. The current focus is to test the agent behavior and make sure the RAG knowledge base works correctly before adding real appointment and client data.
