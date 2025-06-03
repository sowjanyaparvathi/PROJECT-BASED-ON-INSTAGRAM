# PROJECT-BASED-ON-INSTAGRAM
# 📸 Instagram Clone SQL Project

This project simulates the backend schema of an Instagram-like application using SQL. It creates a relational database structure for managing users, photos, likes, comments, followers, and tags.

## 🗂️ Database Schema

The project creates a database named `instagram_clone_db2` and the following tables:

- **users** – stores user profiles.
- **photos** – stores images uploaded by users.
- **comments** – allows users to comment on photos.
- **likes** – stores information about photo likes by users.
- **follows** – stores follower-followee relationships.
- **tags** – contains tags users can apply to photos.
- **photo_tags** – a mapping table between photos and tags.

## 📥 Sample Data

The script also includes:

- Sample data for all tables including `users`, `photos`, `follows`, etc.
- Pre-populated relationships to simulate a realistic social graph.

## 🛠️ Usage

1. Open your SQL client (like MySQL Workbench, DBeaver, etc.)
2. Execute the script: `INSTAGRAM SQL PROJECT.sql`
3. Explore the schema with your own queries or extend the schema.

## ✅ Requirements

- MySQL or any compatible SQL engine
- Basic SQL knowledge

## 💡 Features Demonstrated

- Relational database design
- One-to-many and many-to-many relationships
- Use of timestamps and default constraints
- Composite primary keys
- Basic normalization principles

## 📎 Sample Queries You Can Try

```sql
-- Get all photos by a specific user
SELECT * FROM photos WHERE user_id = 1;

-- Find users who liked a specific photo
SELECT u.username
FROM likes l
JOIN users u ON l.user_id = u.id
WHERE l.photo_id = 1;

-- Get number of followers for each user
SELECT followee_id, COUNT(follower_id) AS follower_count
FROM follows
GROUP BY followee_id;
