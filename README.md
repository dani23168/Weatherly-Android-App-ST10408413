# Weatherly – Part 2 Prototype

**Student:** Dan Mbuyi Kabongo  
**Student Number:** ST10408413  
**Module:** OPSC6312 – Open Source Coding (Intermediate)

This project adapts the supplied weather-app prototype into the **Weatherly** Part 2 prototype while keeping the original Kotlin/XML, Retrofit and Lottie structure largely unchanged.

## Implemented Weatherly Prototype Features

- Splash screen and Weatherly branding.
- Sign in and account registration screen with input validation.
- Prototype password protection using a local SHA-256 hash. For the final application, replace this with Firebase Authentication as specified in the planning document.
- City search using the existing OpenWeather REST API integration.
- Current temperature, minimum/maximum temperature, humidity, wind speed, pressure, sunrise and sunset.
- Weather-specific background and Lottie animation.
- Invalid city and network failure messages without crashing the application.
- **What to Wear** feature using the temperature and weather condition to produce clothing/accessory suggestions.
- Settings screen with Celsius/Fahrenheit preference.
- Logout functionality.

## Planning Features Reserved for Later Iterations

The Part 1 design also includes Google/SSO authentication, seven-day forecasting, UV/precipitation-based recommendations, daily check-ins, streaks, badges, eco-quests, Room offline synchronisation, Firebase/Firestore gamification, push notifications and English/isiZulu/Afrikaans support. These can be added incrementally without replacing the current weather foundation.

## Technology

- Kotlin
- Android Studio
- XML / ConstraintLayout
- Retrofit + Gson
- OpenWeather API
- Lottie
- Android SharedPreferences for prototype settings/session data

## API Key

The supplied prototype originally contained an OpenWeather API key. The adapted project reads it through `gradle.properties` and `BuildConfig` instead of placing it directly in `MainActivity.kt`. **Before publishing or pushing the project to a public GitHub repository, replace the key and preferably use a secure secrets mechanism.**

## Running the Project

1. Open the `Weather-App-main` folder in Android Studio.
2. Allow Gradle dependencies to sync.
3. Check `gradle.properties` and set `WEATHER_API_KEY` to a valid OpenWeather API key.
4. Run the app on an Android emulator or Android phone.
5. Register an account on the first launch.
6. Search for a city, open **What to Wear**, or open **Settings**.

## Part 2 Demonstration Flow

1. Show the Weatherly splash screen.
2. Register and sign in.
3. Search for a South African city.
4. Show live weather information from the REST API.
5. Show the weather animation changing with the condition.
6. Open **What to Wear** and explain the recommendation logic.
7. Open **Settings** and change Celsius/Fahrenheit.
8. Test an invalid city and show that the application remains open with an error message.
