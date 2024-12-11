# Anime & Manga Tracker App

## Table of Contents
1. [Overview](#overview)
2. [Product Spec](#product-spec)
    1. [User Stories](#user-stories)
    2. [Screen Archetypes](#screen-archetypes)
    3. [Navigation](#navigation)
3. [Wireframes](#wireframes)
4. [Schema](#schema)
    1. [Models](#models)
    2. [Networking](#networking)

---

## Overview

### Description
The **Anime & Manga Tracker App** is an iOS application designed to help anime and manga enthusiasts easily track their progress across their favorite series and volumes. The app integrates seamlessly with the **MyAnimeList API**, allowing users to search for anime and manga titles, view detailed descriptions, and rate their watched anime or read manga. It provides a user-friendly interface built with **SwiftUI** and utilizes **Firebase** for secure user authentication and real-time data storage.

---

### App Evaluation

- **Category**: Entertainment
- **Mobile**: Mobile-only application
- **Story**: Users track and rate their anime and manga collections.
- **Market**: Anime and manga fans of all ages, from casual viewers to dedicated fans.
- **Habit**: Occasional use; users will interact with the app periodically.
- **Scope**: Narrow; focused primarily on anime and manga tracking and rating.

---

## Product Spec

#### **Required Must-have Stories**  
These are the essential features for the app to be functional.

- [ x] **User can register an account**  
  Users must be able to sign up for an account using an email and password.

- [ x] **User can log in to the app**  
  Users must be able to log in to the app after registering, with email/password authentication.

- [ x] **User can search for anime and manga by title**  
  Users must be able to enter a search query and view results for anime and manga titles.

- [ x] **User can view details of an anime or manga**  
  When users select an anime or manga from the search results, they should be able to view detailed information (e.g., title, description, genre, rating).

- [ ] **User can rate an anime or manga**  
  Users can rate an anime or manga on a scale from 1-10 after watching or reading.

- [ ] **User can add an anime to their watched list or manga to their read list**  
  Users must be able to mark anime or manga as watched or read and track their progress.

- [ ] **User can view their profile with tracked anime and manga**  
  Users must be able to see a list of all anime they have watched and manga they have read, along with their ratings and progress.

---

#### **Optional Nice-to-have Stories**  
These features are additional enhancements that could improve user experience but are not essential for the core functionality.

- [ ] **User can see their progress over time**  
  Display stats like the total number of anime watched or manga chapters read, and show a percentage of progress for each title.

- [ ] **User can see trending anime and manga**  
  Display a list of currently popular or trending anime and manga based on ratings or recent views.

- [ ] **User can share anime or manga titles on social media**  
  Users should be able to share their favorite titles with friends via social media platforms.

- [ ] **User can see notifications when new episodes/chapter are available**  
  Users can opt-in to receive notifications when a new episode or chapter of a tracked anime/manga is released.

- [x ] **User can tap on a manga/anime title to view more detailed information**  
  Users can navigate to a dedicated page that shows more in-depth information about each anime or manga title, such as staff credits, publisher, and episode/chapter guides.


---

### 2. Screen Archetypes

### **Tab Navigation (Tab to Screen)**

- [ x] **Search Tab**  
  - Leads to the **Search Screen** where users can search for anime/manga titles.

- [ x] **Profile Tab**  
  - Leads to the **Profile Screen** where users can view their tracked anime/manga.

---

### **Flow Navigation (Screen to Screen)**

- [ x] **Login Screen**  
  - Leads to **Home (Search Screen)** after successful login.

- [ x] **Registration Screen**  
  - Leads to **Home (Search Screen)** after successful registration.

- [ x] **Search Screen**  
  - Leads to **Anime Detail Screen** or **Manga Detail Screen** after selecting an anime/manga.

- [x ] **Anime Detail Screen**  
  - Leads back to **Search Screen**.

- [x ] **Manga Detail Screen**  
  - Leads back to **Search Screen**.

- [ x] **Profile Screen**  
  - Leads back to **Search Screen** or other app screens.

---

## Wireframes

[Adobe Scan Dec 10, 2024.pdf](https://github.com/user-attachments/files/18089693/Adobe.Scan.Dec.10.2024.pdf)

---

### [BONUS] Digital Wireframes & Mockups

https://app.uizard.io/p/7de6e9b4
---

### [BONUS] Interactive Prototype

https://app.uizard.io/p/7de6e9b4
---

## Schema

### 1. Models

#### **User**

| Property     | Type   | Description                                       |
|--------------|--------|---------------------------------------------------|
| username     | String | Unique identifier for the user                    |
| password     | String | User’s password for authentication                |
| email        | String | User’s email address                              |
| profilePic   | String | URL to the user’s profile picture (optional)      |

#### **Anime/Manga**

| Property     | Type   | Description                                            |
|--------------|--------|--------------------------------------------------------|
| title        | String | Name of the anime or manga                            |
| description  | String | A brief description of the anime or manga              |
| imageURL     | String | URL to the cover image of the anime or manga           |
| genre        | String | Genre(s) of the anime or manga (e.g., action, comedy)  |
| rating       | Float  | User's rating for the anime or manga (1–10 scale)      |
| progress     | Integer| User's progress (e.g., number of episodes watched)     |

---

### 2. Networking

#### **List of Network Requests by Screen**

- **Login Screen**
  - **POST** `/auth/login` — Authenticate user credentials.
  - **POST** `/auth/register` — Register a new user.

- **Search Screen**
  - **GET** `/anime/search` — Search for anime titles.
  - **GET** `/manga/search` — Search for manga titles.

- **Anime Details Screen**
  - **GET** `/anime/{id}` — Fetch detailed information about a selected anime.

- **Manga Details Screen**
  - **GET** `/manga/{id}` — Fetch detailed information about a selected manga.

- **Rate Anime Screen**
  - **POST** `/anime/rate` — Submit a user rating for an anime.

- **Rate Manga Screen**
  - **POST** `/manga/rate` — Submit a user rating for a manga.

- **Profile Screen**
  - **GET** `/user/profile` — Fetch user’s profile and collection.
  - **POST** `/user/updateProfile` — Update user profile details.

---
**AMS currently name of the app for now for now until app is fully completed. Stands for Anime Manga Search
Sprint 1 Building Progress: Sign in and Sign up view implemented and data is seen in Firebase

**Cat in logo resembles cat from anime movie spirited away

![ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/161c860b-8c7e-495e-9df9-1f09cfae7b74)

Sprint 1: Improved


https://github.com/user-attachments/assets/ad17a581-07a7-4eb7-84cb-40d8803f74d2



Sprint 2: The profile view follows successful login by the user and users are able to search for their favorite animes

![ScreenRecording2024-12-11at12 06 26AM-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/cb535019-a409-48ef-9d21-1f2703549905)

Sprint 2: Improved

https://github.com/user-attachments/assets/4be0a462-85ed-4c87-ae65-35cfc8274f64



