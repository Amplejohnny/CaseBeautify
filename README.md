# CaseBeautify

CaseBeautify is a **Next.js** application designed for users to **customize, preview, and order personalized phone cases**. Built with a modular and scalable architecture, CaseBeautify ensures a seamless experience for users who want to create and visualize their designs in real-time.

---

## Features

- **Custom Case Design**: Upload and configure custom designs.
- **Real-Time Preview**: View a live preview of the customized case.
- **Secure Authentication**: Powered by **KindeAuth** for user authentication.
- **Order Management**: Integrated order placement and tracking.
- **Stripe Payments**: Secure transactions using **Stripe API**.
- **Responsive UI**: Tailored for a smooth experience across devices.

---

## Technologies Used

### Core Technologies:

- **Next.js** (Page Router)
- **TypeScript**
- **Tailwind CSS** (UI Styling)
- **Prisma** (ORM for Database Management)
- **MongoDB** (Database)
- **Stripe** (Payment Processing)
- **UploadThing** (File Uploads)
- **Zod** (Validation)

### Authentication & APIs:

- **KindeAuth** for user authentication.
- **Stripe Webhooks** for handling transactions.
- **UploadThing API** for handling media uploads.

---

## Prerequisites

Ensure you have the following installed before proceeding:

- **Node.js** (v16 or higher)
- **MongoDB** (or a MongoDB Atlas connection string)
- **NPM** or **Yarn**

---

## Installation

### 1. Clone the Repository:

```bash
git clone https://github.com/Amplejohnny/CaseBeautify.git
cd CaseBeautify
```

### 2. Install Dependencies:

```bash
npm install
```

### 3. Set Up Environment Variables:

#### Create a `.env` file in the root directory:

```env
DATABASE_URL=your_mongodb_connection_string
KINDE_CLIENT_ID=your_kinde_id
KINDE_CLIENT_SECRET=your_kinde_client
UPLOADTHING_TOKEN=your_uploadthing_token
KINDE_ISSUER_URL=your_kinde_issuer_url
KINDE_SITE_URL=your_kinde_site
KINDE_POST_LOGOUT_REDIRECT_URL=your_kinde_post_logout_redirect_url
KINDE_POST_LOGIN_REDIRECT_URL=your_kinde_post_login_redirect_url
NEXT_PUBLIC_SERVER_URL=your_next_public_server
STRIPE_SECRET_KEY=your_stripe_secret
STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret
ADMIN_EMAIL=your_resend_admin_email
RESEND_API_KEY=your_resend_api
```

### 4. Run Database Migrations:

```bash
npx prisma migrate dev
```

### 5. Run the Development Server:

```bash
npm run dev
```

### 6. Open the App:

Visit [http://localhost:3000](http://localhost:3000) in your browser.

---

## Directory Structure

```
amplejohnny-casebeautify/
├── README.md
├── components.json
├── next-config.d.ts
├── next.config.mjs
├── package.json
├── postcss.config.mjs
├── tailwind.config.ts
├── tsconfig.json
├── .eslintrc.json
├── .hintrc
├── prisma/
│   └── schema.prisma
├── public/
│   ├── testimonials/
│   └── users/
└── src/
    ├── app/
    │   ├── globals.css
    │   ├── layout.tsx
    │   ├── page.tsx
    │   ├── api/
    │   │   ├── auth/
    │   │   │   └── [kindeAuth]/route.js
    │   │   ├── auth-callback/
    │   │   │   ├── actions.ts
    │   │   │   └── page.tsx
    │   │   ├── uploadthing/
    │   │   │   ├── core.ts
    │   │   │   └── route.ts
    │   │   └── webhooks/route.ts
    │   ├── configure/
    │   │   ├── design/
    │   │   ├── preview/
    │   │   ├── upload/
    │   ├── dashboard/
    │   ├── thank-you/
    ├── components/
    │   ├── emails/
    │   ├── ui/
    ├── config/
    ├── db/
    ├── lib/
    └── validators/
```

---

## Contributing

Contributions are welcome! Follow these steps:

1. **Fork** the repository.
2. **Create a new branch**: `git checkout -b feature/YourFeatureName`
3. **Commit your changes**: `git commit -m 'Add some feature'`
4. **Push to the branch**: `git push origin feature/YourFeatureName`
5. **Open a pull request**

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

## Contact

For any questions or feedback, feel free to reach out:

- **amplejohnny** - [workatdeveloper@gmail.com](mailto\:workatdeveloper@gmail.com)
- **GitHub**: [Amplejohnny](https://github.com/Amplejohnny)
