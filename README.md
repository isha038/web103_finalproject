# Community Hub

CodePath WEB103 Final Project

Designed and developed by: Isha Shrestha

🔗 Link to deployed app: [URL here]

## About

### Description and Purpose
Community Hub is an app where users can join different community groups based on shared interests. Users can view posts/events from those communities, create new posts, and interact with other users in the community.

### Inspiration
The idea was inspired by the need to bring people with shared interests together in a centralized online space.

## Tech Stack

**Frontend:** React, React Router, Axios  
**Backend:** Express, PostgreSQL  
**Deployment:** Railway

## Features

### **Backend Features**

1. **Database Relationships (PostgreSQL):**
   - **One-to-Many Relationship:** 
     - **Communities and Posts:** Each community can have multiple posts. This structure allows for various discussions within each community.
   - **Many-to-Many Relationship with Join Table:**
     - **Users and Communities:** Users can join multiple communities, and each community can have multiple members. This relationship is established with a join table (e.g., `UserCommunity`) to manage these connections.

2. **RESTful API Implementation:**
   - **Endpoints:** Set up a well-designed RESTful API with the following routes:
     - **GET Requests:** Retrieve data, such as fetching all communities or posts within a community.
     - **POST Requests:** Add new entries, like creating a new community or post.
     - **PATCH Requests:** Update existing entries, such as editing community or post details.
     - **DELETE Requests:** Remove entries, like deleting a community or post.
   - **Naming Conventions:** Use proper RESTful naming conventions (e.g., `/communities`, `/communities/:id/posts`, `/users/:id/communities`).

3. **Database Reset Feature:**
   - Implement a route (`/reset`) to reset the database to its default state. This can drop and re-seed the database, useful for testing or restarting the data.

---

### **Frontend Features**

1. **Redirection:**
   - **User Redirection:** Implement a redirect after successful actions, such as after joining a community or creating a new post, to bring users to a relevant page (e.g., redirecting to the community feed).

2. **Single-Page Interaction:**
   - **Inline Post Creation:** Allow users to create a post directly within a community page, without needing to navigate to a new page. Use React state to dynamically update the post list upon submission, ensuring a smooth, single-page experience.

3. **Dynamic Frontend Routes with React Router:**
   - **Routes:** Implement dynamic routes for viewing community details, posts, and user profiles.
     - Example routes: `/communities/:id`, `/communities/:id/posts`, `/users/:id/profile`

4. **Hierarchically Designed React Components:**
   - **Component Breakdown:**
     - **Page Components:** `CommunityPage`, `PostPage`, `UserProfilePage`
     - **Container Components:** Manage data fetching and state for each page (e.g., `CommunityContainer`, `PostContainer`).
     - **Presenter Components:** Render individual UI elements (e.g., `CommunityCard`, `PostForm`, `UserProfile`).
   - **Structure:** Organize components by type (e.g., `pages`, `containers`, and `components` directories) to keep the codebase organized.

### Custom Features

1. **Filtering by Category**
    Communities can be filtered by category, making it easy to find groups based on interests.

2. **Error Handling**
    Graceful error handling is implemented for post or community creation.

## Installation Instructions
1. Clone the repository: `git clone [repo URL]`
2. Install dependencies: `npm install`
3. Set up environment variables in `.env`
4. Start the app: `npm start`



