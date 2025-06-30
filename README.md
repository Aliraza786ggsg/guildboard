# GuildBoard

**GuildBoard** is a modern, scalable frontend application built with Angular for managing and displaying World of Warcraft guild data in real time.

![GuildBoard Preview](https://placehold.co/800x200?text=GuildBoard+Dashboard)

## Table of Contents

* [Features](#features)
* [Tech Stack](#tech-stack)
* [Getting Started](#getting-started)
* [Configuration](#configuration)
* [Available Scripts](#available-scripts)
* [Contributing](#contributing)
* [Security](#security)
* [License](#license)

## Features

* Real-time data synchronization with Blizzard API and Raider.io
* Battle.net OAuth2 authentication
* Guild roster and member statistics
* Raid progression with segmented boss progress bars
* Top Mythic+ dungeon runs and affix tracking
* Responsive design for desktop and mobile

## Tech Stack

* **Frontend**: Angular 17, TypeScript
* **Styling**: TailwindCSS, shadcn/ui
* **State Management**: RxJS observables
* **Backend**: NestJS + Supabase (separate repository)
* **CI/CD**: GitHub Actions, Vercel (frontend)

## Getting Started

### Prerequisites

* Node.js 16+ and npm (or yarn)
* Angular CLI globally installed: `npm install -g @angular/cli`

### Installation

1. Clone the repo:

   ```bash
   git clone https://github.com/TomasPlatero/guildboard.git
   cd guildboard
   ```
2. Install dependencies:

   ```bash
   npm install
   ```
3. Configure environment:

   * Copy `src/environments/environment.example.ts` to `src/environments/environment.ts`
   * Add your Blizzard API credentials and Raider.io key.
4. Serve locally:

   ```bash
   ng serve
   ```
5. Open [http://localhost:4200](http://localhost:4200) in your browser.

## Configuration

Environment variables live in `src/environments/environment.ts`:

```ts
export const environment = {
  production: false,
  blizzard: {
    clientId: 'YOUR_BLIZZARD_CLIENT_ID',
    clientSecret: 'YOUR_BLIZZARD_CLIENT_SECRET',
  },
  raiderioApiKey: 'YOUR_RAIDERIO_API_KEY',
  apiBaseUrl: 'https://api.guildboard.dev'
};
```

## Available Scripts

* `ng serve` – run dev server
* `npm run lint` – run ESLint
* `npm run format` – run Prettier
* `npm test` – run unit tests

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines and code standards.

## Security

* Report vulnerabilities to `taplatero@outlook.es`.
* See [SECURITY.md](SECURITY.md) for policy.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
