# MCP Weather Server

A weather server application built with the Model Context Protocol (MCP) that provides access to real-time weather data and alerts.

## Overview

MCP Weather Server is a TypeScript application that serves as a backend for weather-related applications using the MCP SDK. It provides tools for accessing current weather conditions, forecasts, and weather alerts through the National Weather Service (NWS) API.

## Features

- **US Weather Forecasts**: Get detailed forecast data for any US location via latitude/longitude
- **Weather Alerts**: Retrieve active weather alerts for any US state
- **MCP Integration**: Built as an MCP server for seamless AI assistant integration
- **Command-line Interface**: Easy to install and run as a CLI tool

## Architecture

The application is built using the Model Context Protocol (MCP) framework:

1. **MCP Server Layer**: Handles communication with MCP clients
2. **Weather Tools**: Implements forecast and alert functionality
3. **External API Integration**: Connects to the National Weather Service (NWS) API

### Component Structure

The server includes two primary weather tools:

- **get-forecast**: Retrieves detailed weather forecasts for a location specified by latitude and longitude
- **get-alerts**: Obtains active weather alerts for a specified US state

These tools communicate with the National Weather Service API to provide reliable weather data.

## Tech Stack

- Node.js
- TypeScript
- MCP SDK (@modelcontextprotocol/sdk)
- National Weather Service API
- Zod (for input validation)

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/cskiro/MCP-Weather-Server.git

# Navigate to the project directory
cd MCP-Weather-Server

# Install dependencies
npm install

# Build the project
npm run build

# Make the CLI executable
chmod +x build/index.js

# Install globally (optional)
npm install -g .
```

### Usage

You can use the server in two ways:

1. **Direct invocation**:
```bash
weather
```

2. **Through an MCP-compatible client/assistant**:
Configure your MCP client to use the weather tool for forecasts and weather alerts.

## API Usage

### Get Weather Forecast

```typescript
// Example: Get forecast for San Francisco
{
  latitude: 37.7749,
  longitude: -122.4194
}
```

### Get Weather Alerts

```typescript
// Example: Get alerts for California
{
  state: "CA"
}
```

## Data Sources

This server uses the [National Weather Service API](https://weather.gov/), which provides official weather data for the United States. Due to the limitations of this data source, the application currently only supports US-based locations.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the ISC License - see the LICENSE file for details.
