# App Description and Product Spec

**AniTracker**
A feature-rich iOS application designed to help anime and manga enthusiasts track their progress in a personalized and efficient way, while connecting with the global anime community. Built using SwiftUI and Firebase, this app offers seamless user experience, real-time syncing, and powerful community-building features. The app integrates with the MyAnimeList API, providing access to a vast database of anime and manga, ensuring up-to-date content and accurate tracking.

Key Features:
Secure User Authentication: Create and manage your personal account securely with Firebase Authentication. Your data is synced across devices, giving you access to your library and progress wherever you go.

Real-Time Syncing & Data Storage: Integrated with Firebase Firestore, the app ensures that your anime and manga collection and progress are updated in real-time, no matter the device you're using.

Efficient MVVM Architecture: The app leverages the Model-View-ViewModel (MVVM) design pattern for efficient state management, ensuring a smooth and responsive experience, even with large libraries or frequent updates.

Dynamic, User-Friendly Interface: Designed with SwiftUI, the app provides a sleek, intuitive interface, making it easy to track your watched anime, read manga, and explore new titles with ease.

API Integration with MyAnimeList: The app pulls data from the MyAnimeList API, a popular platform that offers an extensive catalog of anime and manga information. With access to MyAnimeList’s vast library, users can seamlessly add titles to their collections, track their progress, and discover new content based on their preferences. The API provides detailed information about anime series, characters, genres, episodes, reviews, and more, ensuring your tracking experience is comprehensive and up-to-date.

Connecting the Anime Community: This app not only helps users track their anime and manga progress, but it also serves as a platform for anime fans to connect. Share your collection with others, get recommendations, and discuss your favorite series with a community of passionate fans from around the world.

The MyAnimeList API is a robust and widely used API that enables users to interact with one of the largest and most comprehensive anime and manga databases. It provides detailed metadata for thousands of anime and manga titles, allowing users to track what they've watched or read, manage their progress, and discover new series based on personalized recommendations. By integrating the MyAnimeList API, your app ensures that users have access to an up-to-date, expansive database to enhance their tracking experience.

This app blends powerful tracking tools with social features, helping users stay organized while building connections with fellow anime fans globally.

--------------------------------------------
**Product Spec**
Here's a product specification for your anime and manga tracking app based on the template you've provided:

---

## **Product Spec for Anime & Manga Tracker App**

### 🎯 **A. Required and Optional Features**

#### **Required (Must-have) Features:**

1. **User Authentication:**
   - Users must be able to securely log in to their account using Firebase Authentication.
   - Users must be able to sign up for a new account.

2. **Anime/Manga Search:**
   - Users must be able to search for anime and manga titles by name using the MyAnimeList API.
   - Search results must display relevant titles with information like description and image.

3. **Anime/Manga Details View:**
   - Upon selecting a title from search results, users must see a detailed view of the anime or manga, including a description, cover image, genre, and more.

4. **Rate Anime and Manga:**
   - Users must be able to rate an anime or manga title.
   - Users must be able to submit ratings via a separate screen for anime and manga (to be accessed after viewing the anime/manga details).

5. **Profile Management:**
   - Users must have a profile screen that displays their anime and manga collections and ratings.

#### **Optional (Nice-to-have) Features:**

1. **Search History:**
   - Users could view their past search queries for convenience.

2. **Anime/Manga Recommendations:**
   - The app could suggest anime or manga based on user ratings or viewing history.

3. **Community Interaction:**
   - Users could share ratings or favorite titles with other users in-app.
   
4. **Review System:**
   - Users could leave written reviews on anime or manga titles, in addition to rating them.

---

### 🎯 **B. Screens in Your App**

Based on the features outlined above, here are the core screens your app will have to function:

1. **Login Screen:**
   - Allows users to log in or sign up using Firebase Authentication.

2. **Search Screen:**
   - A search bar for users to input anime or manga titles.
   - Display search results with relevant details (title, description, image).

3. **Anime Details Screen:**
   - Shows detailed information about a selected anime, including a description, image, and other metadata.
   - Includes a button to rate the anime.

4. **Manga Details Screen:**
   - Shows detailed information about a selected manga, similar to the Anime Details Screen.
   - Includes a button to rate the manga.

5. **Rate Anime Screen:**
   - A screen where users can submit a rating for an anime title they’ve viewed.

6. **Rate Manga Screen:**
   - A screen where users can submit a rating for a manga title they’ve read.

7. **Profile Screen:**
   - Displays a user’s profile with their list of tracked anime and manga, along with ratings.
   - Users can see and edit their profile details.

---

### 🎯 **C. Navigation Flow**

This section defines how users will navigate between the different screens in your app.

#### **Tab Navigation:**
- **Home:** Displays the **Search** screen.
- **Profile:** Displays the **Profile** screen where users can see their personal collection.
  
#### **Flow Navigation:**
- **Login Screen**  
   => **Search Screen** (After successful login)

- **Search Screen**  
   => **Anime Details Screen** (When a user selects an anime from search results)  
   => **Manga Details Screen** (When a user selects a manga from search results)

- **Anime Details Screen**  
   => **Rate Anime Screen** (User navigates to rate the anime)

- **Manga Details Screen**  
   => **Rate Manga Screen** (User navigates to rate the manga)

- **Profile Screen**  
   => **Search Screen** (User can return to the search screen from their profile)

---

### **Flow Diagram Example:**

1. **Login Screen**  
   - → **Search Screen** (after login)

2. **Search Screen**  
   - → **Anime Details Screen** (when selecting an anime title)  
   - → **Manga Details Screen** (when selecting a manga title)

3. **Anime Details Screen**  
   - → **Rate Anime Screen** (to submit a rating for the anime)

4. **Manga Details Screen**  
   - → **Rate Manga Screen** (to submit a rating for the manga)

5. **Profile Screen**  
   - → **Search Screen** (return to the search functionality)

---

### **Summary**

- **Required Features:** User authentication, search functionality, anime/manga details, rating system, and a profile screen.
- **Optional Features:** Search history, recommendations, community interaction, and review system.
- **Screens:** Login, Search, Anime Details, Manga Details, Rate Anime, Rate Manga, Profile.
- **Navigation Flow:** Uses both **Tab Navigation** (for switching between Home and Profile) and **Flow Navigation** (for transitioning between details and rating screens).

This product spec outlines the core structure, features, and navigation flow for your anime and manga tracking app, providing a clear blueprint for development and design.

