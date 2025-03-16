# AI Assistant Boilerplate

A comprehensive boilerplate for creating AI assistants with multiple client integrations.

## Architecture

This project is organized into two main components:

1. **AI Service** (`/ai`): A Python API built with FastAPI and Smolagents that handles AI processing
2. **Clients** (`/clients`): Multiple client implementations that connect to the AI service
   - WhatsApp Client: Uses Baileys for WhatsApp integration

## Getting Started

### Prerequisites

- Node.js 18+ and npm
- Python 3.10+
- Poetry

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/luisotee/ai-assistant-boilerplate.git
   cd ai-assistant-boilerplate
   ```

2. Set up environment variables:

   ```bash
   cp ai/.env.example ai/.env
   cp clients/.env.example clients/.env
   ```

3. Install dependencies:
   ```bash
   npm run setup
   ```

### Running the Services

#### Development Mode

1. Start the AI service:

   ```bash
   npm run dev:ai
   ```

2. In a separate terminal, start the WhatsApp client:
   ```bash
   npm run dev:whatsapp
   ```

#### Production Mode

1. Start the AI service:

   ```bash
   npm run start:ai
   ```

2. Build and start the WhatsApp client:
   ```bash
   npm run build:whatsapp
   npm run start:whatsapp
   ```

## Configuration

### AI Service

The AI service can be configured through the `.env` file in the `ai` directory:

- API settings (HOST, PORT)
- API Keys (OpenAI, Azure, etc.)
- Bot configuration
- Database settings (Supabase)

### WhatsApp Client

The WhatsApp client can be configured through the `.env` file in the `clients` directory:

- AI API URL
- WhatsApp API port
- Reaction settings

## Adding New Clients

To add a new client:

1. Create a new directory under `clients/`
2. Implement the client using the provided AI API
3. Add appropriate scripts to the root `package.json`

## Documentation

- The AI service API documentation is available at `http://localhost:40000/docs` when running
- WhatsApp API Swagger documentation is available at `http://localhost:3000/api-docs`

## License

MIT
