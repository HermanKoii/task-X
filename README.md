# Twitter Searcher CLI

## Project Overview

The Twitter Searcher is a powerful Command-Line Interface (CLI) tool designed for advanced social media research and data gathering using web automation. It enables users to perform targeted searches on Twitter/X and extract information through a systematic, configurable approach.

### Key Features
- Automated Twitter/X search with advanced query configurations
- Headless browser-based data extraction
- Configurable search depth and limits
- Integration with Koii Network's decentralized task framework
- Supports archival and research use cases

### Use Cases
- Academic and research social media analysis
- Content archival and backup
- Social media trend tracking
- Community coordination and information gathering

⚠️ **Ethical Usage Notice**: This tool is intended for legitimate research and archival purposes. Ensure compliance with Twitter's Terms of Service and respect user privacy.

## Installation

### Prerequisites
- Node.js (v16+ recommended)
- Yarn or npm
- Git

### Install from GitHub
```bash
# Clone the repository
git clone https://github.com/your-org/twitter-searcher.git

# Navigate to the project directory
cd twitter-searcher

# Install dependencies
yarn install
# or
npm install
```

## Usage

### Basic Search
```bash
# Perform a basic Twitter search
yarn start
```

### Configurable Search
Edit the `twitter-task.js` to customize your search:

```javascript
let query = {
    limit: 100,           // Maximum number of records
    searchTerm: "#koii",  // Keyword or hashtag
    query: "https://x.com/search?q=#koii&src=typed_query",
    depth: 3,             // Search recursion depth
    recursive: true       // Enable recursive searching
}
```

### Running Tests
```bash
# Run a single round test
yarn test

# Full test suite
yarn test:full
```

## Command Reference

| Command | Description | Options |
|---------|-------------|---------|
| `yarn start` | Run default Twitter search | - |
| `yarn test` | Run single round test | - |
| `yarn webpack` | Build task executable | - |
| `yarn deploy` | Deploy to Koii Network | Requires Koii CLI |

## Configuration

### Environment Variables
Create a `.env` file with the following optional configurations:

```ini
TWITTER_API_KEY=your_api_key
SEARCH_DEPTH=3
MAX_RECORDS=100
```

## Project Structure
- `index.js`: Main entry point
- `twitter-task.js`: Core search logic
- `adapters/twitter/twitter.js`: Twitter interaction adapter
- `tests/`: Comprehensive test suite

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

### Running Tests
```bash
yarn test
yarn test:full
```

## Deployment

Deploy to Koii Network using the official CLI:
```bash
yarn webpack
npx @_koii/create-task-cli@latest
```

## License
This project is licensed under the ISC License.

## Additional Resources
- [Koii Network Documentation](https://docs.koii.network)
- [Twitter API Guidelines](https://developer.twitter.com/en/docs)

---

**Disclaimer**: Ensure ethical and legal compliance when using this tool. Always respect platform terms of service and user privacy.