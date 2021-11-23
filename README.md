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

---

## 💡 Database Models

Database should contain the following four models, including the requirements listed for each model:

- `Category`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `category_name`

    - String.

    - Doesn't allow null values.

- `Product`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `product_name`

    - String.

    - Doesn't allow null values.

  - `price`

    - Decimal.

    - Doesn't allow null values.

    - Validates that the value is a decimal.

  - `stock`

    - Integer.

    - Doesn't allow null values.

    - Set a default value of `10`.

    - Validates that the value is numeric.

  - `category_id`

    - Integer.

    - References the `Category` model's `id`.

- `Tag`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `tag_name`

    - String.

- `ProductTag`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `product_id`

    - Integer.

    - References the `Product` model's `id`.

  - `tag_id`

    - Integer.

    - References the `Tag` model's `id`.

---

## 🔦 Associations

---

You need to execute association methods on your Sequelize models to create the following relationships between them:

- `Product` belongs to `Category`, and `Category` has many `Product` models, as a category can have multiple products but a product can only belong to one category.

- `Product` belongs to many `Tag` models, and `Tag` belongs to many `Product` models. Allow products to have multiple tags and tags to have many products by using the `ProductTag` through model.

---

## Fill Out the API Routes to Perform RESTful CRUD Operations

Fill out the unfinished routes in `product-routes.js`, `tag-routes.js`, and `category-routes.js` to perform create, read, update, and delete operations using Sequelize models.

---

## Sync Sequelize to the Database on Server Start

Create the code needed in `server.js` to sync the Sequelize models to the MySQL database on server start.

---

## 💾 Installation & Usage

---

To install this application, clone the repository to your local directory by visiting following link:

- https://github.com/Amit-Ranjan22/E-Commerce_Back-End.git

Once downloaded, you can install its dependencies by navigating to the E-Commerce_Back-End directory on your local machine and issuing the following command:

- npm install

This command will install the following dependencies:

- dotenv
- express
- mysql2
- sequelize

from your terminal, log into mysql by using

- mysql -u root -p

and enter your password for mysql.
Once you are logged in to your mysql, run the schema by using

- source db/schema.sql;

Once you run the schema, come out of mysql by using

- exit

Now, from your terminal run your seed file by using

- npm run seed

After seeding your database run your server.js file by using

- node server.js

And now, you can use Insomnia to use the different apis for get, post, put or delete request.

---
