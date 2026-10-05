\# StyleFolio



StyleFolio is a full-stack virtual wardrobe application that helps users organize clothing, create outfits, plan what to wear, and get AI-powered styling suggestions.



This repository contains both the React frontend and the Express backend.



\## Features



\- User registration and login with JWT authentication

\- Google OAuth sign-in

\- Personal wardrobe and clothing management

\- Outfit creation and calendar planning

\- AI-powered styling advice

\- Wishlist management

\- User messaging

\- Profile management and password reset

\- Admin pages for managing users and clothing

\- Stripe payment integration



\## Tech Stack



| Area | Technologies |

| --- | --- |

| Frontend | React, Vite, Redux Toolkit, React Router, Axios |

| Backend | Node.js, Express, Mongoose |

| Database | MongoDB Atlas |

| Authentication | JWT, Passport, Google OAuth |

| Media | Cloudinary |

| Messaging | Firebase Realtime Database |

| AI | Groq |

| Payments | Stripe |



\## Repository Structure



\- `StyleFolio-main/` — React frontend

\- `StyleFoliobackend-main/` — Express API

\- `.gitignore` — shared Git ignore rules



Each application has its own `package.json` and dependencies.



\## Getting Started



\### Prerequisites



\- Node.js and npm

\- A MongoDB database

\- Credentials for the external services used by the application



\### Clone the Repository



```bash

git clone https://github.com/atakhan11/Stylefolioy.git

cd Stylefolioy

```



\### Start the Backend



```bash

cd StyleFoliobackend-main

npm install

```



Create a `.env` file in the backend directory. The application uses the following environment variables:



```env

PORT=5000

MONGO\_URI=

JWT\_SECRET=

SESSION\_SECRET=



FRONTEND\_URL=http://localhost:5173

GOOGLE\_CALLBACK\_URL=http://localhost:5000/api/users/auth/google/callback

GOOGLE\_CLIENT\_ID=

GOOGLE\_CLIENT\_SECRET=



CLOUDINARY\_CLOUD\_NAME=

CLOUDINARY\_API\_KEY=

CLOUDINARY\_API\_SECRET=



GROQ\_API\_KEY=

STRIPE\_SECRET\_KEY=



EMAIL\_USER=

EMAIL\_PASS=

RESEND\_API\_KEY=

```



Replace empty values with your own configuration. External service credentials are needed for their corresponding features.



Use a random `SESSION\_SECRET` of at least 32 characters. Keep secret values out of Git.



Start the development server:



```bash

npm run server

```



The backend runs at `http://localhost:5000` by default.



\### Start the Frontend



Open another terminal:



```bash

cd StyleFolio-main

npm install

```



Create a `.env` file in the frontend directory:



```env

VITE\_API\_BASE\_URL=http://localhost:5000

VITE\_STRIPE\_PUBLISHABLE\_KEY=

```



Start the frontend:



```bash

npm run dev

```



The frontend normally runs at `http://localhost:5173`. Use that port to match the default backend CORS configuration.



Firebase configuration is currently maintained in the frontend source and must match your Firebase project.



\## Available Commands



\### Frontend



| Command | Purpose |

| --- | --- |

| `npm run dev` | Start the development server |

| `npm run build` | Generate production files in `dist/` |

| `npm run preview` | Preview the production build locally |

| `npm run lint` | Run ESLint |



\### Backend



| Command | Purpose |

| --- | --- |

| `npm run server` | Start development mode with Nodemon |

| `npm start` | Start the Node.js server |



The backend does not currently have an automated test suite.



\## Deployment Configuration



The frontend and backend can be deployed separately from this repository.



\- Set the frontend's `VITE\_API\_BASE\_URL` to the backend HTTPS URL before building.

\- Set the backend's `FRONTEND\_URL` to the frontend URL without a trailing slash.

\- Set `GOOGLE\_CALLBACK\_URL` to the backend's full Google OAuth callback URL.

\- Register the same callback URL in Google Cloud Console.

\- Configure backend secrets through the hosting provider's environment settings.

\- Ensure MongoDB network access allows connections from the deployed backend.



Vite embeds frontend environment variables during the build. Changing them requires a new build. Never put private service keys in `VITE\_` variables.



\## Author



\*\*Atakhan Hajizada\*\*



\- \[GitHub](https://github.com/atakhan11)

\- \[LinkedIn](https://www.linkedin.com/in/atakhan-hacizade/)

