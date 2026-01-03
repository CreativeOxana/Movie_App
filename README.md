# Movie App

A modern mobile application for browsing movies built with React Native and Expo Router. The app uses TMDB API to fetch movie data and Appwrite for saving favorite movies.

## Features

- **Movie Search** - Search for movies by title
- **Trending Movies** - Display currently popular movies
- **Detailed Information** - Complete information about each movie
- **Saved Movies** - Save favorite movies
- **User Profile** - Manage user account
- **Responsive Design** - Optimized for mobile devices and tablets

## Technologies

- **React Native** - Cross-platform mobile framework
- **Expo Router** - File-based routing system
- **TypeScript** - Type-safe JavaScript
- **NativeWind** - Tailwind CSS for React Native
- **TMDB API** - Movie and TV show database
- **Appwrite** - Backend-as-a-Service for data storage
- **React Native Reanimated** - Advanced animations

## Requirements

- Node.js (version 18 or higher)
- npm or yarn
- Expo CLI
- TMDB API key
- Appwrite instance

## Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd movie_app
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:

   ```env
   EXPO_PUBLIC_MOVIE_API_KEY=your_tmdb_api_key_here
   EXPO_PUBLIC_APPWRITE_ENDPOINT=your_appwrite_endpoint
   EXPO_PUBLIC_APPWRITE_PROJECT_ID=your_appwrite_project_id
   ```

4. **Start the application**
   ```bash
   npm start
   ```

## Running on Device

### Android

```bash
npm run android
```

### iOS

```bash
npm run ios
```

### Web

```bash
npm run web
```

## Project Structure

```
movie_app/
├── app/                    # Expo Router pages
│   ├── (tabs)/            # Tab navigation
│   │   ├── index.tsx      # Home page
│   │   ├── search.tsx     # Search
│   │   ├── saved.tsx      # Saved movies
│   │   └── profile.tsx    # User profile
│   ├── movies/
│   │   └── [id].tsx       # Movie detail
│   └── _layout.tsx        # Root layout
├── components/            # Reusable components
│   ├── MovieCard.tsx      # Movie card
│   ├── TrendingCard.tsx   # Trending movie card
│   └── SearchBar.tsx      # Search bar
├── services/              # API and data services
│   ├── api.ts            # TMDB API functions
│   ├── appwrite.ts       # Appwrite configuration
│   └── useFetch.ts       # Custom hook for data fetching
├── constants/             # Constants and configuration
│   ├── icons.ts          # Icons
│   └── images.ts         # Images
├── interfaces/            # TypeScript types
│   └── interfaces.d.ts   # Type definitions
└── assets/               # Static files
    ├── images/           # Images
    └── icons/            # Icons
```

## Configuration

### TMDB API

1. Sign up on [TMDB](https://www.themoviedb.org/settings/api)
2. Get API key
3. Add the key to `.env` file

### Appwrite

1. Create an Appwrite project
2. Set up a database for storing favorite movies
3. Add endpoint and project ID to `.env` file

## Usage

### Home Page

- Displays trending movies
- List of latest movies
- Search bar

### Search

- Search movies by title
- Filter results
- Navigate to movie details

### Movie Detail

- Complete movie information
- Budget and revenue
- Genres and production companies
- Ratings and reviews

### Saved Movies

- List of favorite movies
- Option to remove from favorites

## Design

The app uses modern design with:

- Dark theme
- Gradient backgrounds
- Animations and transitions
- Responsive layout
- Intuitive navigation

## Testing

```bash
npm run lint
```

## Build

### Android APK

```bash
expo build:android
```

### iOS IPA

```bash
expo build:ios
```

## Development

For local development:

1. Clone the repository
2. Install dependencies: `npm install`
3. Set up environment variables
4. Run: `npm start`

## Author

Created with React Native and Expo

## Useful Links

- [Expo Documentation](https://docs.expo.dev/)
- [React Native Documentation](https://reactnative.dev/)
- [TMDB API Documentation](https://developers.themoviedb.org/)
- [Appwrite Documentation](https://appwrite.io/docs)

## Known Issues

- [ ] Offline mode is not implemented
- [ ] Push notifications are not set up
- [ ] Social sharing functionality is missing

## Roadmap

- [ ] Implement offline mode
- [ ] Add push notifications
- [ ] Social sharing functionality
- [ ] Dark/Light mode toggle
- [ ] Advanced search filters
- [ ] Movie reviews and ratings
