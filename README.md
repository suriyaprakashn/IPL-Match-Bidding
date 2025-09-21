# IPL Match Bidding - Pie-in-the-Sky

A mobile application for legal bidding on IPL cricket matches where users can predict match outcomes, earn points, and compete on a leaderboard.

## 📱 App Overview

Pie-in-the-Sky is a bidding platform that allows registered users to:
- Bid on IPL matches before they begin
- Predict match winners until toss time
- Earn points based on accurate predictions
- Track their position on leaderboards
- View team standings and match schedules

## ✨ Key Features

### For Bidders
- 📅 View all match schedules (teams, date, time, location)
- 🎯 Bid on teams before match start
- 🔄 Change bids until toss occurs
- ❌ Cancel bids without penalty
- 📊 View personal points and leaderboard position
- 🏆 See top 3 leaders and team standings

### For Admins
- 🏟️ Tournament management (duration, description)
- 👥 Team and player management
- 📋 Match scheduling and rescheduling
- 📈 Update match statistics and results
- 🎯 Declare winners and update points
- 👀 View bidder distributions per team

## 🎯 Point System

The dynamic point system rewards strategic predictions:
- **Start of tournament**: 2 points for correct prediction
- **Point difference ≤ 6**: 
  - 2 points for predicting higher-ranked team
  - 3 points for predicting lower-ranked team
- **Point difference > 6**:
  - 2 points for predicting higher-ranked team
  - 5 points for predicting lower-ranked team

## 🗄️ Database Schema

### Tables Structure

#### User Management
- `IPL_User` - User accounts and authentication
- `IPL_Bidder_Details` - Bidder personal information
- `IPL_Bidder_Points` - Bidder points and statistics

#### Tournament Structure
- `IPL_Tournament` - Tournament information
- `IPL_Team` - Team details
- `IPL_Player` - Player information
- `IPL_Team_players` - Team-player relationships
- `IPL_Team_Standings` - Team performance metrics

#### Match Management
- `IPL_Stadium` - Venue information
- `IPL_Match` - Match details and outcomes
- `IPL_Match_Schedule` - Scheduling information

#### Bidding System
- `IPL_Bidding_Details` - Bid records and status

## 🔧 SQL Queries

The application requires the following data retrieval operations:

1. **Win Percentage**: Show percentage of wins for each bidder (highest to lowest)
2. **Stadium Matches**: Display number of matches conducted at each stadium
3. **Toss Impact**: Percentage of wins by team that won the toss in a given stadium
4. **Bid Statistics**: Total bids along with bid team and team name
5. **Match Winners**: Show team ID who won the match as per win details
6. **Team Performance**: Display total matches played, won, and lost by each team
7. **Player Roles**: Display bowlers for Mumbai Indians team
8. **All-rounders Count**: Show teams with more than 4 all-rounders in descending order

## 🚀 Installation & Setup

1. **Database Setup**:
   ```sql
   -- Run the provided database script to create tables
   -- Execute insert statements to populate sample data
   -- Verify successful execution by selecting sample rows
   ```

2. **Application Setup**:
   ```bash
   # Clone the repository
   git clone [repository-url]
   
   # Install dependencies
   npm install
   
   # Configure database connection
   # Update config/database.js with your credentials
   
   # Start the application
   npm start
   ```

## 📋 Prerequisites

- SQL database (MySQL/PostgreSQL)

## 🎮 Usage

1. **Registration**: Users register with mobile number, email, and password
2. **Bidding**: Select matches and place bids before start time
3. **Tracking**: Monitor points and leaderboard position in real-time
4. **Administration**: Admins manage matches, update results, and maintain system

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 🆓 Free Forever

This application is designed for legal bidding entertainment and does not involve real money transactions.

---

**Note**: This application is for entertainment purposes only and complies with all relevant regulations regarding sports betting in permitted jurisdictions.
