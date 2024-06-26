# URL Shortening Service

## Overview
This project is a URL shortening service that allows users to create shortened URLs with custom prefix codes. The service is designed to be highly performant and reliable, leveraging Cloudflare's suite of tools and services.

## Features
- **Custom Prefix Codes:** Create shortened URLs with custom prefixes.
- **High Performance:** Built on Cloudflare Pages and Workers for optimal performance.
- **Reliability:** Utilizes Cloudflare's KV namespace for robust data storage.
- **Enhanced Security:** Integrated with Turnstile for security measures.

## Technologies Used
- **Cloudflare Pages:** Hosting the static site.
- **Cloudflare Workers:** Serverless function execution.
- **KV Namespace:** Key-value storage for shortened URLs.
- **Turnstile:** Security integration to prevent abuse.
- **Svelte:** Front-end framework for building the user interface.

## Getting Started

### Prerequisites
To run this project, you need:
- A Cloudflare account
- Node.js installed on your local machine

### Installation

1. **Clone the Repository**
   ```sh
   git clone https://github.com/your-username/url-shortening-service.git
   cd url-shortening-service
   ```

2. **Install Dependencies**
   ```sh
   npm install
   ```

### Configuration
1. **Set Up Cloudflare**
    - Create a new Cloudflare Pages project.
    - Set up Cloudflare Workers and KV namespace according to your account.

2. **Environment Variables**
    - Create a `.env` file and add your Cloudflare credentials and configuration details:
      ```sh
      CLOUDFLARE_ACCOUNT_ID=your_account_id
      CLOUDFLARE_API_TOKEN=your_api_token
      KV_NAMESPACE_ID=your_kv_namespace_id
      ```

### Deployment
1. **Build the Project**
   ```sh
   npm run build
   ```

2. **Deploy to Cloudflare Pages**
    - Follow the instructions on Cloudflare Pages to deploy your project.

## Usage
Once deployed, users can shorten URLs by navigating to the web interface. They can enter a long URL and optionally specify a custom prefix for the shortened URL. The service will generate a shortened URL that can be shared and accessed easily.

## Contributing
If you would like to contribute to this project, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For any questions or feedback, please open an issue on the repository or contact [admin@drasta.one](mailto:admin@drasta.one).

---

Feel free to modify this template according to your specific project details and preferences.
