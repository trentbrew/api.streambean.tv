# Streambean API

Streambean's backend is built with [Hono](https://hono.dev/) and deployed on Vercel, enabling seamless Twitch stream integrations.

## Getting Started

### Requirements

- Twitch Developer Account
- NPM v18.x or higher
- Vercel Account

### Installation

1. **Install Dependencies:**

   ```bash
   npm install
   npm run start # runs vercel dev
   ```

2. **Configure Vercel Project:**
   Follow the setup guide to link your Vercel project.

3. **Access the API:**
   Open [http://localhost:3000/api](http://localhost:3000/api) in your browser to view the API.

4. **Customize the API:**
   Modify `api/index.ts` to tailor the API functionality. Refer to the [Hono API documentation](https://hono.dev/api/hono) for more details.

## Deploy on Vercel

Deploy your Hono app effortlessly using the [Vercel Platform](https://vercel.com/templates?search=hono).

## API Documentation

The Streambean API offers a variety of endpoints to interact with Twitch data and manage stream interactions effectively. Below is a brief overview of the primary endpoints available:

### Endpoints

1. **Home Page (`GET /`)**:

   - Returns an HTML page embedded with a Twitch player.
   - Useful for quick tests and demonstrations.

2. **Twitch Player (`GET /player/:channel_name`)**:

   - Dynamically generates an HTML page with a Twitch player for the specified channel.
   - Replace `:channel_name` with the actual Twitch channel name to view.

3. **Fetch Streams (`GET /streams/:category`)**:

   - Retrieves streams from Twitch based on the specified category.
   - Categories like 'gaming', 'irl', and 'just-chatting' can be used in place of `:category`.

4. **Fetch Categories (`GET /categories`)**:
   - Returns a JSON object listing all available categories and their details.

### Usage Examples

- Accessing the home page:

  ```
  curl http://localhost:3000/api
  ```

- Fetching streams for gaming:

  ```
  curl http://localhost:3000/api/streams/gaming
  ```

- Getting Twitch player for a channel:

  ```
  curl http://localhost:3000/api/player/twitch_channel_name
  ```

- Listing all categories:
  ```
  curl http://localhost:3000/api/categories
  ```

For more detailed information and advanced configurations, refer to the source code in `api/index.js`.
