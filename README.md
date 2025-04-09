## Subscription Tracker API

**SubscriptionTracker-API** is a secure and scalable backend service for managing user subscriptions. It offers powerful features such as JWT-based authentication, email reminders for upcoming renewals, global error handling, and bot protection via Arcjet. Designed with modular architecture and robust logging, this API is perfect for building modern SaaS subscription tracking applications.

## ⚙️ Tech Stack

- Node.js
- Express.js
- MongoDB

## 🔋 Features

👉 **Advanced Rate Limiting and Bot Protection**: with Arcjet that helps you secure the whole app.

👉 **Database Modeling**: Models and relationships using MongoDB & Mongoose.

👉 **JWT Authentication**: User CRUD operations and subscription management.

👉 **Global Error Handling**: Input validation and middleware integration.

👉 **Logging Mechanisms**: For better debugging and monitoring.

👉 **Email Reminders**: Automating smart email reminders with workflows using Upstash.

and many more, including code architecture and reusability

## 🤸 Installation & Setup

Follow these steps to set up the project locally on your machine.

```bash
git clone https://github.com/ankushchhabra02/SubscriptionTracker-API.git
cd SubscriptionTracker-API
```

**Installation**

Install the project dependencies using npm:

```bash
npm install
```

**Set Up Environment Variables**

Create a new file named `.env.local` in the root of your project and add the following content:

```env
# PORT
PORT=5500
SERVER_URL="http://localhost:5500"

# ENVIRONMENT
NODE_ENV=development

# DATABASE
DB_URI=

# JWT AUTH
JWT_SECRET=
JWT_EXPIRES_IN="1d"

# ARCJET
ARCJET_KEY=
ARCJET_ENV="development"

# UPSTASH
QSTASH_URL=http://127.0.0.1:8080
QSTASH_TOKEN=

# NODEMAILER
EMAIL_PASSWORD=
```

**Running the Project**

```bash
npm run dev
```

Open [http://localhost:5500](http://localhost:5500) in your browser or any HTTP client to test the project.

## <a name="snippets">🕸️ Snippets</a>

<details>
<summary><code>Dummy JSON Data</code></summary>

```json
{
  "name": "Amazon Prime Membership",
  "price": 139.0,
  "currency": "USD",
  "frequency": "monthly",
  "category": "entertainment",
  "startDate": "2025-03-10T00:00:00.000Z",
  "paymentMethod": "Credit Card"
}
```

</details>

## 📡 API Endpoints

### 🧑 User Auth

- `POST /api/v1/auth/sign-up` – Register a new user
- `POST /api/v1/auth/sign-in` – Login and receive JWT
- `POST /api/v1/auth/sign-out` – Logout user (optional implementation)

### 👤 Users

- `GET /api/v1/users/` – Get all users
- `GET /api/v1/users/:id` – Get a single user by ID
- `POST /api/v1/users/` – Create new user (admin use)
- `PUT /api/v1/users/:id` – Update user details
- `DELETE /api/v1/users/:id` – Delete a user

### 📦 Subscriptions

- `POST /api/v1/subscriptions/` – Create new subscription
- `GET /api/v1/subscriptions/:id` – Get subscription by ID
- `PUT /api/v1/subscriptions/:id` – Update subscription
- `DELETE /api/v1/subscriptions/:id` – Delete subscription
- `PUT /api/v1/subscriptions/:id/cancel` – Cancel subscription
- `GET /api/v1/subscriptions/user/:id` – Get all subscriptions by a user
- `GET /api/v1/subscriptions/upcoming-renewals` – Get upcoming renewals (static demo)

### 🔔 Workflows

- `POST /api/v1/workflows/` – Trigger reminder workflow using Upstash

## 📄 License

This project is licensed under the MIT License.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to check the [issues page](https://github.com/ankushchhabra02/SubscriptionTracker-API/issues).
