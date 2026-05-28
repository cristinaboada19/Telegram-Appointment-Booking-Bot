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
