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

- [ ] **User can register an account**  
  Users must be able to sign up for an account using an email and password.

- [ x] **User can log in to the app**  
  Users must be able to log in to the app after registering, with email/password authentication.

- [ x] **User can search for anime and manga by title**  
  Users must be able to enter a search query and view results for anime and manga titles.

- [ ] **User can view details of an anime or manga**  
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

- [ ] **User can tap on a manga/anime title to view more detailed information**  
  Users can navigate to a dedicated page that shows more in-depth information about each anime or manga title, such as staff credits, publisher, and episode/chapter guides.


---

### 2. Screen Archetypes

#### **Login Screen**
- **Required User Feature**: User can log in or sign up using Firebase Authentication.

#### **Search Screen**
- **Required User Feature**: User can search for anime and manga titles and view search results with relevant details.

#### **Anime Details Screen**
- **Required User Feature**: User can view detailed information about an anime, including description, cover image, and ratings.

#### **Manga Details Screen**
- **Required User Feature**: User can view detailed information about a manga, including description, cover image, and ratings.

#### **Rate Anime Screen**
- **Required User Feature**: User can rate an anime title they’ve watched.

#### **Rate Manga Screen**
- **Required User Feature**: User can rate a manga title they’ve read.

#### **Profile Screen**
- **Required User Feature**: User can view and manage their anime and manga collections, along with their ratings and progress.

---

### 3. Navigation

#### **Tab Navigation (Tab to Screen)**

- **Home Feed** (Search Screen)
- **Profile** (Profile Screen)

#### **Flow Navigation (Screen to Screen)**

- **Login Screen**  
  → Leads to **Search Screen** (After successful login)

- **Search Screen**  
  → Leads to **Anime Details Screen** (When selecting an anime title)  
  → Leads to **Manga Details Screen** (When selecting a manga title)

- **Anime Details Screen**  
  → Leads to **Rate Anime Screen** (User rates the anime)

- **Manga Details Screen**  
  → Leads to **Rate Manga Screen** (User rates the manga)

- **Profile Screen**  
  → Leads to **Search Screen** (User can return to search from their profile)

---

## Wireframes

*Insert hand-sketched wireframes here to illustrate the layout and structure of the app screens.*
[Adobe Scan Dec 10, 2024.pdf](https://github.com/user-attachments/files/18089693/Adobe.Scan.Dec.10.2024.pdf)

---

### [BONUS] Digital Wireframes & Mockups
*Include digital wireframes or mockups (e.g., using tools like Figma or Adobe XD) to provide a clearer visualization of the app's UI.*
https://app.uizard.io/p/7de6e9b4
---

### [BONUS] Interactive Prototype
*Link to an interactive prototype or provide an embedded version (e.g., using tools like Figma or InVision).*
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

This **README** provides a comprehensive and organized overview of your Anime & Manga Tracker app. It includes essential information on the app's structure, user stories, navigation flow, and networking, as well as details about wireframes and schema. The markdown format is clean and easily readable, ensuring developers and stakeholders can understand the app's functionality and structure at a glance.
