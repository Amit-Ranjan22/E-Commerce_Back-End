# 🧮 E-Commerce_Back-End

## ✍️ User Story

---

```
AS a manager at an internet retail company
I WANT:  a back end for my e-commerce
         website that uses the latest technologies
SO THAT: my company can compete with
         other e-commerce companies.
```

---

## 🤝 Acceptance Criteria

---

```
GIVEN a functional Express.js API
WHEN: I add my database name, MySQL
      username, and MySQL password
      to an environment variable file
THEN: I am able to connect to a
      database using Sequelize.
WHEN: I enter schema and seed commands
THEN: a development database is created
      and is seeded with test data.
WHEN: I enter the command to invoke the
      application
THEN: my server is started and the
      Sequelize models are synced to the MySQL database.
WHEN: I open API GET routes in Insomnia
      Core for categories, products, or tags
THEN: the data for each of these routes
      is displayed in a formatted JSON.
WHEN: I test API POST, PUT, and DELETE
      routes in Insomnia Core
THEN: I am able to successfully create,
      update, and delete data in my database.

```

---

## 🖼️ Mock-Up

---

The following animation shows the application's GET routes to return all categories, all products, and all tags being tested in Insomnia Core:

![In Insomnia Core, the user tests “GET tags,” “GET Categories,” and “GET All Products.”.](./Assets/13-orm-homework-demo-01.gif)

The following animation shows the application's GET routes to return a single category, a single product, and a single tag being tested in Insomnia Core:

![In Insomnia Core, the user tests “GET tag by id,” “GET Category by ID,” and “GET One Product.”](./Assets/13-orm-homework-demo-02.gif)

The following animation shows the application's POST, PUT, and DELETE routes for categories being tested in Insomnia Core:

![In Insomnia Core, the user tests “DELETE Category by ID,” “CREATE Category,” and “UPDATE Category.”](./Assets/13-orm-homework-demo-03.gif)

---

## 🏃‍♂️ Getting Started

---

You need to use the [MySQL2](https://www.npmjs.com/package/mysql2) and [Sequelize](https://www.npmjs.com/package/sequelize) packages to connect your Express.js API to a MySQL database and the [dotenv](https://www.npmjs.com/package/dotenv) package to use environment variables to store sensitive data.

Use the `schema.sql` file in the `db` folder to create your database with MySQL shell commands. Use environment variables to store sensitive data like your MySQL username, password, and database name.
