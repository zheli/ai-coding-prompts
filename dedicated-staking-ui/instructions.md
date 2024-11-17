# Generate project boiler plate
Project Boilerplate Specification

Please generate a frontend project boilerplate that adheres to industry best practices and incorporates the following technologies and tools:
Tech Stack

    Framework: Next.js (latest stable version)
    Language: TypeScript
    Package Manager: pnpm
    CSS Framework: Tailwind CSS (latest stable version)
    State Management: React Context API or an equivalent lightweight solution
    Environment: Docker and Docker Compose for containerization

Project Requirements

    Folder Structure:
        Follow Next.js conventions for pages, components, and API routes.
        Include a src directory for all custom code, with subdirectories for components, pages, styles, and utils.
        Separate configuration files (e.g., .env.local, tailwind.config.js, and TypeScript config files).

    Tailwind CSS:
        Include a preconfigured tailwind.config.js file with basic customizations and the ability to extend themes.
        Enable JIT mode and optimize for production using purge in the config.

    TypeScript:
        Fully typed configuration and boilerplate code.
        Include tsconfig.json tailored for Next.js.

    Docker/Docker Compose:
        A Dockerfile to build the frontend container using a multi-stage build (development and production).
        A docker-compose.yml file for easy local development.

    Linting & Formatting:
        Integrate ESLint with a robust set of rules for React and TypeScript.
        Add Prettier for code formatting.
        Include preconfigured .eslintrc.json and .prettierrc files.

    Development Features:
        Hot-reloading enabled.
        Support for environment variables via .env.local.
        Preconfigured scripts for pnpm to handle development, build, and production.

    Production Optimization:
        Optimize Next.js build for production.
        Include a lightweight nginx server in the production stage of the Dockerfile to serve the built static assets.

    CI/CD Readiness:
        Preconfigured Dockerfile to enable integration with popular CI/CD pipelines.
        Add pnpm install and pnpm build as steps in the pipeline.

    ReadMe:
        A README.md file explaining:
            How to set up and run the project locally.
            Docker instructions for development and production.
            How to add additional dependencies with pnpm.

    Extras:
        Preinstall common dependencies like axios or fetch for API requests and classnames for easier conditional class management.
        Include a simple landing page to validate the setup.
        Include a gitignore file

Make sure the project setup is clean, modular, and easy to scale for future development. Provide a well-commented readme file explain the rationale behind the chosen configurations. Make sure you don't use the code quote `````` in the markdown file.

# Generate project
## Prompt for ChatGPT
Generate a prompt for cursor to create a frontend project for a staking service. Use next.js, typescript, pnpm, docker, docker-compose and follow all the best practice. The service is called dedicate staking and it's for a company called "Stakeway" to provide Ethereum/Gnosis staking service. A user can connect to their wallet using WalletConnect or Metamask and stake ETH or GNO into the service, a user can mint staked ETH/GNO into osETH or osGNO, a user can unmint osETH or osGNO, a user can also unstake ETH. There should also be a dashboard showing total staked ETH/GNO from the user and their historical rewards. Some features will need the frontend service to call backend APIs.

When generate markdown files, make sure we don't use the code quote feature as that is not working in cursor right now.

## Output

Here’s a prompt tailored for Cursor to create the frontend project:

---

### **Project Specification: Frontend for Dedicate Staking Service**

#### **Project Overview**
You are tasked to create a frontend project for a staking service called **"Dedicate Staking"**. This service is provided by **Stakeway**, offering Ethereum and Gnosis staking. Users will interact with the platform using features like staking, minting, unminting, and unstaking, as well as viewing their staking statistics and historical rewards.

The frontend will be built using **Next.js** with **TypeScript**, and it will follow all best practices, including optimization for performance, security, and maintainability. The project will use **pnpm** for package management and will be containerized with **Docker** and **Docker Compose** for seamless deployment.

---

#### **Features and Functionalities**
1. **Wallet Connection**
   - Enable users to connect their wallets using **WalletConnect** or **Metamask**.

2. **Staking and Minting**
   - Allow users to:
     - Stake **ETH** or **GNO**.
     - Mint staked ETH into **osETH** or staked GNO into **osGNO**.

3. **Unminting and Unstaking**
   - Allow users to:
     - Unmint **osETH** or **osGNO** back into ETH/GNO.
     - Unstake **ETH** and withdraw it from the service.

4. **Dashboard**
   - Display:
     - Total staked ETH/GNO for the connected user.
     - Historical rewards for staking activity.

5. **API Integration**
   - Implement frontend logic to interact with backend APIs for:
     - Fetching user staking data.
     - Executing staking, minting, unminting, and unstaking operations.
     - Retrieving historical rewards data.

---

#### **Tech Stack**
- **Frontend Framework:** Next.js
- **Language:** TypeScript
- **Package Manager:** pnpm
- **Containerization:** Docker and Docker Compose
- **Wallet Integration:** WalletConnect, Metamask
- **Styling:** Tailwind CSS or CSS Modules (preferred for a consistent design system)

---

#### **Folder Structure**
- Follow the standard Next.js project structure with the following adjustments:
  - **`/components`**: Reusable UI components (e.g., Button, Modal, WalletConnect).
  - **`/pages`**: Next.js routes for home, staking, and dashboard views.
  - **`/services`**: API interaction functions (e.g., `stakeETH`, `fetchRewards`).
  - **`/utils`**: Helper functions (e.g., wallet connection utilities).
  - **`/styles`**: Global and module-specific styles.
  - **`/hooks`**: Custom React hooks for state management and API interactions.

---

#### **Features to Highlight**
- Follow **best practices** for Next.js projects:
  - **Static Optimization** for pages wherever possible.
  - **Dynamic Rendering** for personalized dashboard data.
  - Implement **error boundaries** and graceful fallbacks for API errors.
- Use **ESLint** and **Prettier** for code consistency.
- Add **unit tests** with Jest or React Testing Library.
- Ensure **responsiveness** for all devices using Tailwind CSS.

---

#### **Deployment and Local Development**
- Provide a `docker-compose.yml` file to enable running the project locally.
- Use environment variables for API endpoints and wallet provider configurations.
- Include a `README.md` with detailed instructions on:
  - How to set up the project locally.
  - How to build and deploy the Docker containers.
  - How to integrate backend APIs for testing.

---

#### **Deliverables**
1. A fully functional frontend for **Dedicate Staking** with all specified features.
2. A clean and organized folder structure with reusable components and hooks.
3. Integration with backend APIs using a modular service-based approach.
4. Responsive and accessible UI that follows modern design principles.
5. Dockerized project for both local development and production.

---

#### **Notes**
- Avoid using the Markdown code quote feature (` ``` `) in documentation files. Use plain text for code snippets instead.
