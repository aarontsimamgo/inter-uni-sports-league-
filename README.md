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

## Sample Test Data for Candid UI

### User Registration
- Name: "John Doe"
- Email: "john.doe@example.com"
- Address: "123 Sports Street"
- Role: { StudentAthlete: null } // Can also use { Coach: null }, { Administrator: null }, or { LeagueOfficial: null }

### Create Team
- Name: "Red Dragons"
- SportType: { Football: null } // Can also use { Basketball: null } or { Volleyball: null }

### Add Member to Team
- TeamId: "<use team id from Create Team response>"
- MemberId: "<use student athlete id from User Registration response>"

### Assign Coach to Team
- TeamId: "<use team id from Create Team response>"
- CoachId: "<use coach id from User Registration response>"

### Create League
- Name: "Premier League"
- SportType: { Football: null }

### Create Tournament
- Name: "Summer Championship"
- Structure: { RoundRobin: null } // Can also use { Knockout: null }
- TeamIds: ["<team_id_1>", "<team_id_2>"] // Use team IDs from Create Team responses
- SportType: { Football: null }

### Schedule Match
- HomeTeamId: "<use team id from Create Team response>"
- AwayTeamId: "<use different team id from Create Team response>"
- ScheduledDate: "2024-12-25T15:00:00.000Z" // Use future date

### Submit Match Result
- MatchId: "<use match id from Schedule Match response>"
- Result: "<use either home team id or away team id>"

### Get Leaderboards
- SportType: { Football: null }

### Query Methods Test IDs
- For getUser: "<use any user id from registration response>"
- For getTeam: "<use any team id from team creation response>"
- For getLeague: "<use any league id from league creation response>"
- For getTeamByCoach: "<use any coach id from user registration response>"






