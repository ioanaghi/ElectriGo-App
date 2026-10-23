# ElectriGo

React Native and Expo prototype for EV charging discovery and vehicle management; Innovation Labs semifinalist project.

## Product

A mobile prototype exploring how EV drivers discover charging locations and manage their vehicles. Developed as a team project for Innovation Labs, where the project reached the semifinals.

## What is in the repository

- Map, location-search, and charging-location screens.
- Vehicle registration and vehicle-profile screens.
- Authentication, account, wallet, and charging-flow interfaces.
- React Navigation, Firebase configuration, Clerk integration, and Expo device APIs.

The presence of a screen does not imply a live payment or charging-network integration. Treat this version as a prototype.

## Architecture

`App/Screen/` contains feature screens, `App/Context/` provides shared state, `App/Navigations/` defines navigation, and `App/Utils/` contains service/configuration helpers.

## Run locally

```sh
git clone https://github.com/ioanaghi/ElectriGo-App.git
cd ElectriGo-App
npm ci
npm start
```

The manifest targets Expo SDK 50 and React Native 0.73. Use a compatible development client/emulator; the current Expo Go release may not support this older SDK. Configure your own Firebase, Clerk, and map-service projects where required. Installation alone does not provision those services.

## Security and deployment considerations

Use restricted development API keys and sample accounts. Firebase client configuration is not an authorization boundary: enforce access through service-side rules and authentication. Keep server credentials out of mobile bundles. Wallet and charging flows need separate backend validation before handling real transactions.

## Project context

Team hackathon/startup prototype. The repository demonstrates the shared implementation; individual ownership of each feature is not specified. Next steps are a reproducible configuration guide, a documented demo flow, and validation of external-service integrations.
