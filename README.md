# 💍 RingSathi

![RingSathi Banner](public/logo.png)

RingSathi is a modern, production-ready web and mobile application built with Next.js and Prisma. It features an AI-powered verification engine, community reporting capabilities, fuzzy search, and regional detection, establishing a robust and trustworthy platform.

## 🌟 Features

- **AI-Powered Verification Engine**: Automated scraping and intelligent verification mechanisms to maintain high trust levels.
- **Community Reporting**: Empowering users to report and maintain community guidelines.
- **Advanced Search**: Integrated `fuse.js` for blazing-fast, fuzzy search capabilities.
- **Regional Detection**: Smart regional detection for localized experiences.
- **Cross-Platform**: Modern web application deployed on Vercel/Firebase and a dedicated Android application.
- **Robust Tech Stack**: Built on Next.js 15, React 19, Prisma with SQLite (`@libsql/client`), Tailwind CSS, and Framer Motion.

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm, yarn, pnpm, or bun

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/pronzzz/ringsathi.git
   cd ringsathi
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up the database and run migrations:

   ```bash
   npm run postinstall
   ```

4. Seed the database (optional but recommended):

   ```bash
   npm run tsx prisma/seed.ts
   ```

5. Start the development server:

   ```bash
   npm run dev
   ```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## 📱 Android App

The repository includes a dedicated Android application version of the web project, located in the `/android-app` directory. Refer to the specific README in that directory for mobile-specific build instructions.

## 📚 Documentation

- [Technical Guide](GUIDE.md): Detailed architectural and technical overview of the project.
- [Contributing](CONTRIBUTING.md): Guidelines for contributing to RingSathi.
- [Code of Conduct](CODE_OF_CONDUCT.md): Our expectations for community interactions.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
