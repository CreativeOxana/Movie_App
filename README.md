# Movie App

Moderní mobilní aplikace pro prohlížení filmů postavená s React Native a Expo Router. Aplikace využívá TMDB API pro získávání dat o filmech a Appwrite pro ukládání oblíbených filmů.

## Funkce

- **Vyhledávání filmů** - Vyhledejte filmy podle názvu
- **Trending filmy** - Zobrazuje aktuálně populární filmy
- **Detailní informace** - Kompletní informace o každém filmu
- **Uložené filmy** - Ukládání oblíbených filmů
- **Profil uživatele** - Správa uživatelského účtu
- **Responzivní design** - Optimalizováno pro mobily a tablety

## Technologie

- **React Native** - Cross-platform mobilní framework
- **Expo Router** - File-based routing systém
- **TypeScript** - Type-safe JavaScript
- **NativeWind** - Tailwind CSS pro React Native
- **TMDB API** - Databáze filmů a TV pořadů
- **Appwrite** - Backend-as-a-Service pro ukládání dat
- **React Native Reanimated** - Pokročilé animace

## Požadavky

- Node.js (verze 18 nebo vyšší)
- npm nebo yarn
- Expo CLI
- TMDB API klíč
- Appwrite instance

## Instalace

1. **Klonujte repozitář**
   ```bash
   git clone <repository-url>
   cd movie_app
   ```

2. **Nainstalujte závislosti**
   ```bash
   npm install
   ```

3. **Nastavte environment proměnné**
   Vytvořte soubor `.env` v root adresáři:
   ```env
   EXPO_PUBLIC_MOVIE_API_KEY=your_tmdb_api_key_here
   EXPO_PUBLIC_APPWRITE_ENDPOINT=your_appwrite_endpoint
   EXPO_PUBLIC_APPWRITE_PROJECT_ID=your_appwrite_project_id
   ```

4. **Spusťte aplikaci**
   ```bash
   npm start
   ```

## Spuštění na zařízení

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

## Struktura projektu

```
movie_app/
├── app/                    # Expo Router stránky
│   ├── (tabs)/            # Tab navigace
│   │   ├── index.tsx      # Hlavní stránka
│   │   ├── search.tsx     # Vyhledávání
│   │   ├── saved.tsx      # Uložené filmy
│   │   └── profile.tsx    # Uživatelský profil
│   ├── movies/
│   │   └── [id].tsx       # Detail filmu
│   └── _layout.tsx        # Root layout
├── components/            # Reusable komponenty
│   ├── MovieCard.tsx      # Karta filmu
│   ├── TrendingCard.tsx   # Trending film karta
│   └── SearchBar.tsx      # Vyhledávací pole
├── services/              # API a data služby
│   ├── api.ts            # TMDB API funkce
│   ├── appwrite.ts       # Appwrite konfigurace
│   └── useFetch.ts       # Custom hook pro data fetching
├── constants/             # Konstanty a konfigurace
│   ├── icons.ts          # Ikony
│   └── images.ts         # Obrázky
├── interfaces/            # TypeScript typy
│   └── interfaces.d.ts   # Definice typů
└── assets/               # Statické soubory
    ├── images/           # Obrázky
    └── icons/            # Ikony
```

## Konfigurace

### TMDB API
1. Zaregistrujte se na [TMDB](https://www.themoviedb.org/settings/api)
2. Získejte API klíč
3. Přidejte klíč do `.env` souboru

### Appwrite
1. Vytvořte Appwrite projekt
2. Nastavte databázi pro ukládání oblíbených filmů
3. Přidejte endpoint a project ID do `.env` souboru

## Použití

### Hlavní stránka
- Zobrazuje trending filmy
- Seznam nejnovějších filmů
- Vyhledávací pole

### Vyhledávání
- Vyhledejte filmy podle názvu
- Filtrování výsledků
- Navigace na detail filmu

### Detail filmu
- Kompletní informace o filmu
- Budget a revenue
- Žánry a produkční společnosti
- Hodnocení a recenze

### Uložené filmy
- Seznam oblíbených filmů
- Možnost odebrat z oblíbených

## Design

Aplikace používá moderní design s:
- Tmavým tématem
- Gradient pozadí
- Animacemi a přechody
- Responzivním layoutem
- Intuitivní navigací

## Testování

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

## Vývoj

Pro lokální vývoj:

1. Klonujte repozitář
2. Nainstalujte závislosti: `npm install`
3. Nastavte environment proměnné
4. Spusťte: `npm start`

## Autor

Vytvořeno s pomocí React Native a Expo

## Užitečné odkazy

- [Expo Documentation](https://docs.expo.dev/)
- [React Native Documentation](https://reactnative.dev/)
- [TMDB API Documentation](https://developers.themoviedb.org/)
- [Appwrite Documentation](https://appwrite.io/docs)

## Známé problémy

- [ ] Offline režim není implementován
- [ ] Push notifikace nejsou nastaveny
- [ ] Social sharing funkcionalita chybí

## Roadmap

- [ ] Implementace offline režimu
- [ ] Přidání push notifikací
- [ ] Social sharing funkcionalita
- [ ] Dark/Light mode toggle
- [ ] Pokročilé filtry vyhledávání
- [ ] Recenze a hodnocení filmů
