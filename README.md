# Sports League Management System

This is a Sports League Management System implemented using Azle, a WASM-based framework for building Internet Computer (IC) canisters. It provides functionality for managing users, teams, leagues, tournaments, and matches.

## Key Features

1. **User Management**:
   - Register and fetch user information
   - Update user details
   - Assign user roles (Student Athlete, Coach, Administrator, League Official)

2. **Team Management**:
   - Create and fetch team information
   - Add members to teams
   - Assign coaches to teams

3. **League Management**:
   - Create and fetch league information
   - Create tournaments within a league

4. **Tournament Management**:
   - Create and fetch tournament information
   - Associate teams with a tournament

5. **Match Management**:
   - Schedule matches between teams
   - Submit and fetch match results

6. **Leaderboards**:
   - Get leaderboard for a specific sport type based on match results

## Usage

To use this Sports League Management System, you can deploy the Azle canister to the Internet Computer (IC) and interact with it using the available functions.

Here's an example of how to use the `registerUser` function:

```javascript
const result = await sportLeagueCanister.registerUser({
  name: "John Doe",
  email: "john@example.com",
  address: "123 Main St",
  role: { StudentAthlete: null },
});

if ("Ok" in result) {
  console.log("User registered successfully:", result.Ok);
} else {
  console.error("Error registering user:", result.Err);
}

## Getting Started

### Prerequisites

To run the Loan Management System locally, you need:

- [Node.js](https://nodejs.org/) installed on your machine.
- An Internet Computer development environment set up (e.g., using DFX).

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/aarontsimamgo/inter-uni-sports-league-.git
   ```

2. Install dependencies:

   ```bash
   cd inter-uni-sports-league-
   npm install
   ```

## Usage

1. Start the local development environment:

   ```bash
   dfx start --background --clean``
   ```

2. Deploy the canister smart contracts:

   ```bash
   dfx deploy
   ```

3. Interact with the dApp using the provided API or user interface.






