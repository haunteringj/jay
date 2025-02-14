# Lotus: Proof of Concept

## 🚀 Overview of Lotus

Lotus is a **community-powered mobile application** designed to help parents **locate, rate, and review parent rooms** in public spaces. By providing **real-time insights, structured quality ratings, and crowdsourced reviews**, Lotus eliminates the **frustration of finding clean, accessible spaces for parents and caregivers.**

### **What Problem Does Lotus Solve?**

Many parents struggle to find **clean, accessible parent rooms** while navigating public spaces. Existing solutions—Google searches, outdated blogs, and fragmented social media discussions—**lack real-time accuracy and structured ratings.** Lotus bridges this gap by offering a **centralized, reliable platform** tailored specifically for parents.

### **How Does Lotus Solve This Problem?**

- A **real-time, community-driven directory** of parent rooms
- **Standardized quality ratings** for cleanliness, accessibility, and amenities
- **Live user contributions**, ensuring up-to-date, trustworthy information
- **Gamified engagement**, rewarding users for reviewing and verifying locations

This document outlines:

- The **basic idea** behind Lotus
- The **wireframe** to visualize the application
- The **technology stack**
- The **sequence diagram** demonstrating core functionality
- **User journeys** illustrating key app interactions

---

## 🎨 **Wireframe**

The following wireframe provides a **visual representation of the Lotus app’s user interface.**

![Wireframe](./assets/low-fidelity_wireframe.png)

This wireframe illustrates:
✅ **Homepage & Search** – Users can quickly find nearby parent rooms
✅ **Room Details Page** – Reviews, ratings, and amenities listed clearly
✅ **Review Submission Flow** – Simple interface for adding contributions
✅ **Profile & Rewards** – Users track engagement and earned points

---

## 🏗️ **Technology Stack**

The **Lotus app** is built using a **modern, scalable, and mobile-friendly stack**:

### **📱 Frontend (Mobile App)**

- **React Native** (Cross-platform mobile development)
- **Expo** (Streamlined development & testing)

### **🔗 Backend & API**

- **Node.js & Express.js** (REST API for data exchange)
- **Firebase Auth & JWT** (User authentication & session management)

### **🗄️ Database & Storage**

- **PostgreSQL** (Structured data storage for parent room locations, reviews, user points)
- **Firebase (Firestore)** (Real-time updates & user activity tracking)

### **🌍 External Services**

- **Google Maps API** (Location data & navigation)
- **Cloudinary** (Image storage for user-submitted parent room photos)

---

## 🔄 **Sequence Diagram: How Lotus Works**

The following **sequence diagram** outlines how the system processes a **parent room search request**:

![Sequence Diagram](./assets/lotus_sequence_diagram.png)

**Steps:**
1️⃣ User opens the Lotus app and enters a search query  
2️⃣ The **frontend (React Native)** sends a request to the **backend API (Node.js/Express)**  
3️⃣ The **backend API queries the database (PostgreSQL/Firebase)** for matching parent rooms  
4️⃣ The database returns **relevant parent room details**  
5️⃣ The backend **fetches geolocation data** from **Google Maps API**  
6️⃣ The API sends the **combined response** to the mobile app  
7️⃣ The **user sees nearby parent rooms, complete with reviews, ratings, and amenities**

---

## 👣 **User Journeys**

The following user flows illustrate **how Lotus enhances the parent experience**:

### **1️⃣ Finding a Parent Room (Search Flow)**

**Scenario:** A parent needs a clean, accessible parent room nearby.

**Steps:**
1️⃣ The user **opens the Lotus app**  
2️⃣ The user enters **"parent room near me"**  
3️⃣ The app **retrieves real-time location data & nearby results**  
4️⃣ The user **filters results based on amenities (e.g., feeding area, changing table)**  
5️⃣ The app **displays room ratings, reviews, and directions**  
6️⃣ The user **navigates to the selected parent room**

---

### **2️⃣ Leaving a Review (Engagement Flow)**

**Scenario:** A parent visits a parent room and wants to help others by leaving a review.

**Steps:**
1️⃣ The user **checks in** at a parent room location  
2️⃣ The app **prompts them to leave a review**  
3️⃣ The user **adds a star rating, comments, and uploads photos**  
4️⃣ The review **is saved in the database** and **updates the average rating**  
5️⃣ The user **earns engagement points** for contributing to the community

---

### **3️⃣ Earning Points & Rewards (Gamification Flow)**

**Scenario:** The app encourages parents to contribute by offering a **reward system**.

**Steps:**
1️⃣ The user **earns points** for reviewing parent rooms or verifying information  
2️⃣ The app **tracks their contributions & milestones**  
3️⃣ The user **unlocks badges, in-app rewards, or discounts from brand partners**  
4️⃣ The system **updates the user’s profile & engagement score**

---

## 🛠️ **Next Steps in Development**

📌 **Develop a functional MVP with basic search & review capabilities**  
📌 **Launch a closed beta test with parents in urban areas**  
📌 **Implement gamification & brand partnerships for monetization**

Lotus is positioned to **advance beyond its proof of concept** as the **MVP moves into development and real-world testing.**

---
