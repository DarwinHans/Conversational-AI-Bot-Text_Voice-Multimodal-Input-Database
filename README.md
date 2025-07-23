# Conversational-AI-Bot-Text_Voice-Multimodal-Input-Database

Este proyecto implementa un **asistente virtual inteligente** integrado con Telegram, desarrollado en la plataforma de automatización **n8n**. Permite a los usuarios interactuar en lenguaje natural (texto o voz), interpretando sus solicitudes mediante inteligencia artificial y gestionando su calendario de manera autónoma y eficiente.

<img width="1210" height="399" alt="Captura de Pantalla 2025-07-23 a la(s) 09 38 53" src="https://github.com/user-attachments/assets/76108caa-9380-4f62-a398-33e4cc6c9d46" />

---

## 📌 Características del flujo

- ✅ Entrada por texto o audio desde Telegram.
- 🧠 Interpretación de lenguaje natural mediante modelo GPT-4o-mini.
- 🗓️ Conexión con Google Calendar para:
  - Crear eventos
  - Modificar horarios
  - Eliminar reuniones
  - Consultar disponibilidad
- 🔄 Transcripción automática de mensajes de voz (OpenAI Whisper).
- 🔊 Generación de respuesta en voz natural (ElevenLabs).
- 🧠 Memoria contextual con PostgreSQL para interacciones continuas.
- 🧠 Soporte para consultas semánticas vía vector store (Supabase).

---

## 🧠 Lógica de decisión: ¿Texto o Audio?

La respuesta al usuario se entrega en **texto o audio**, según las siguientes reglas:

1. **Primera respuesta siempre en texto.**
2. **Si el usuario lo pide explícitamente**, se respeta su preferencia.
3. **Respuestas largas o explicativas** → se entregan en **audio**.
4. **Respuestas con datos numéricos, fechas o enlaces** → en **texto**.
5. **Otros casos** → se alterna aleatoriamente (50% texto / 50% audio).

---

## 🧰 Tecnologías y servicios utilizados

| Herramienta / Servicio        | Función principal |
|------------------------------|--------------------|
| **n8n**                      | Orquestación del flujo |
| **Telegram Bot API**         | Entrada/salida de mensajes |
| **OpenAI GPT-4o / Whisper**  | Procesamiento y transcripción de lenguaje |
| **Google Calendar API**      | Gestión de eventos |
| **ElevenLabs API**           | Generación de voz a partir de texto |
| **PostgreSQL (Supabase)**    | Memoria de conversación |
| **Supabase Vector Store**    | Consulta semántica (opcional) |

---

## 📦 Requisitos para implementación

- Cuenta de [n8n](https://n8n.io) (Cloud o self-hosted)
- Bot de Telegram con token habilitado
- API Key de [OpenAI](https://platform.openai.com)
- API Key de [ElevenLabs](https://www.elevenlabs.io/)
- Cuenta de Google Calendar con OAuth2 configurado
- Base de datos PostgreSQL (recomendada: [Supabase](https://supabase.com))

---

## 🚀 Posibles mejoras

- 🌍 Soporte multilingüe
- 💬 Integración con WhatsApp o Slack
- 📊 Reportes automáticos semanales
- 🧩 Personalización del asistente por usuario
- 🖥️ Interfaz web para gestión avanzada

---
