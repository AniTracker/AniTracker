Anime & Manga Tracker App
Table of Contents
Overview
Product Spec
Wireframes
Schema
Overview
Description
The Anime & Manga Tracker App is an iOS application designed to help anime and manga enthusiasts easily track their progress across their favorite series and volumes. The app integrates seamlessly with the MyAnimeList API, allowing users to search for anime and manga titles, view detailed descriptions, and rate their watched anime or read manga. It provides a user-friendly interface built with SwiftUI and utilizes Firebase for secure user authentication and real-time data storage.

This app is perfect for anime and manga fans who want to keep track of the anime they’ve watched and the manga they’ve read, as well as share their ratings with others in the anime community.

App Evaluation
Category:
Entertainment: The app is aimed at anime and manga fans, providing a streamlined way to track and explore new content.
Mobile:
Mobile-only: The app is designed exclusively for iOS devices, making use of mobile-specific features like authentication and real-time syncing.
Story:
Tracking Your Journey: The app allows users to keep track of the anime and manga they've watched or read, rate them, and discover new titles based on personal preferences.
Market:
Target Audience: This app targets anime and manga fans of all ages, from casual viewers to dedicated fans. It appeals to people who want to organize their media library and share recommendations.
Habit:
Occasional Use: Users will interact with the app periodically to add new anime or manga to their lists and update their progress.
Scope:
Moderate: The app is focused on tracking and rating anime and manga, with features like searching, viewing details, and sharing ratings. It does not attempt to cover the entire anime ecosystem but focuses on providing an organized way for users to manage their collections.
Product Spec
1. User Stories (Required and Optional)
Required Must-have Stories
User Authentication:

User can securely log in using Firebase Authentication.
User can create a new account.
Anime/Manga Search:

User can search for anime or manga titles using the MyAnimeList API.
View Anime/Manga Details:

User can view detailed information about an anime or manga title, including a description, cover image, and other metadata.
Rate Anime/Manga:

User can rate anime and manga on a separate screen, based on what they've watched or read.
Profile Management:

User can view and manage their personal profile, including their anime and manga collection and ratings.
Optional Nice-to-have Stories
Search History:

User can view a history of previously searched anime and manga titles.
Recommendations:

Based on the user’s ratings and collection, the app could suggest new anime or manga titles.
Community Sharing:

Users can share their ratings and collections with others in the app.
Review System:

User can leave written reviews alongside ratings for anime and manga titles.
2. Screen Archetypes
Login Screen
Required User Feature: User can log in or sign up using Firebase Authentication.
Search Screen
Required User Feature: User can search for anime and manga titles and view search results with relevant details.
Anime Details Screen
Required User Feature: User can view detailed information about an anime, including description, cover image, and ratings.
Manga Details Screen
Required User Feature: User can view detailed information about a manga, including description, cover image, and ratings.
Rate Anime Screen
Required User Feature: User can rate an anime title they’ve watched.
Rate Manga Screen
Required User Feature: User can rate a manga title they’ve read.
Profile Screen
Required User Feature: User can view and manage their anime and manga collections, along with their ratings and progress.
3. Navigation
Tab Navigation (Tab to Screen)
Home Feed (Search Screen)
Profile (Profile Screen)
Flow Navigation (Screen to Screen)
Login Screen
→ Leads to Search Screen (After successful login)

Search Screen
→ Leads to Anime Details Screen (When selecting an anime title)
→ Leads to Manga Details Screen (When selecting a manga title)

Anime Details Screen
→ Leads to Rate Anime Screen (User rates the anime)

Manga Details Screen
→ Leads to Rate Manga Screen (User rates the manga)

Profile Screen
→ Leads to Search Screen (User can return to search from their profile)

Wireframes
Insert hand-sketched wireframes here to illustrate the layout and structure of the app screens.

[BONUS] Digital Wireframes & Mockups
Include digital wireframes or mockups (e.g., using tools like Figma or Adobe XD) to provide a clearer visualization of the app's UI.

[BONUS] Interactive Prototype
Link to an interactive prototype or provide an embedded version (e.g., using tools like Figma or InVision).

Schema
Models
User
Property	Type	Description
username	String	Unique identifier for the user
password	String	User’s password for authentication
email	String	User’s email address
profilePic	String	URL to the user’s profile picture (optional)
Anime/Manga
Property	Type	Description
title	String	Name of the anime or manga
description	String	A brief description of the anime or manga
imageURL	String	URL to the cover image of the anime or manga
genre	String	Genre(s) of the anime or manga (e.g., action, comedy)
rating	Float	User's rating for the anime or manga (1–10 scale)
progress	Integer	User's progress (e.g., number of episodes watched)
Networking
List of Network Requests by Screen
Login Screen

POST /auth/login — Authenticate user credentials.
POST /auth/register — Register a new user.
Search Screen

GET /anime/search — Search for anime titles.
GET /manga/search — Search for manga titles.
Anime Details Screen

GET /anime/{id} — Fetch detailed information about a selected anime.
Manga Details Screen

GET /manga/{id} — Fetch detailed information about a selected manga.
Rate Anime Screen

POST /anime/rate — Submit a user rating for an anime.
Rate Manga Screen

POST /manga/rate — Submit a user rating for a manga.
Profile Screen

GET /user/profile — Fetch user’s profile and collection.
POST /user/updateProfile — Update user profile details.
