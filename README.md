# Q-Bank – SAT Question Generator

Q-Bank is a smart SAT question generator web app that helps users improve their test skills through personalized practice. Users can choose the subject, question type, and difficulty to receive targeted SAT questions, track their performance, and get recommendations for improvement.

## 🔧 Tech Stack

- **Frontend**: React, TypeScript, React Router, Tailwind CSS
- **Backend/Auth**: Firebase Authentication
- **Development Tooling**: Vite

## 🚀 Features

- Email/password sign-up and login
- Google social login support
- Responsive and clean landing page
- Choose SAT subject, type, and difficulty to receive questions
- Track incorrect answers
- Automatically generate similar questions based on user’s mistakes
- Post-practice feedback with:
  - Accuracy rate
  - Weak areas analysis
  - Recommended focus strategies

## 📁 Project Structure

/src  
├── components/               # Reusable UI components  
├── context/                 # React contexts for auth and question state  
│   ├── authContext.tsx  
│   └── QuestionBankContext.tsx  
├── data/                    # Firebase configuration  
├── hooks/                   # Custom React hooks  
├── lib/                     # Utility functions (if any)  
├── pages/                   # Page-level components  
│   ├── AnalyzeLoadingPage.tsx  
│   ├── AnalyzePage.tsx  
│   ├── DifficultiesSelection.tsx  
│   ├── LandingPage.tsx  
│   ├── Login.tsx / SignUp.tsx  
│   ├── MyPage.tsx  
│   ├── Practice.tsx  
│   ├── SkillsSelection.tsx  
│   ├── Summary.tsx  
│   ├── TestJson.tsx  
│   └── NotFound.tsx  
├── App.tsx                  # Main app with routing  
├── index.css / App.css      # Global styles  
├── main.tsx                 # App entry point  
└── vite-env.d.ts            # Type definitions for Vite

## 🔐 Firebase Setup

To enable user authentication:

1. Go to https://console.firebase.google.com and create a new project.
2. Enable **Email/Password** and **Google** sign-in methods in **Authentication** settings.
3. Copy your project’s Firebase config.
4. Add it to `src/data/firebase.ts` like below:

```ts
// firebase.ts
import { initializeApp } from "firebase/app";
import { getAuth, GoogleAuthProvider } from "firebase/auth";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  appId: "YOUR_APP_ID",
  // ...other config if needed
};

const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);
export const provider = new GoogleAuthProvider();
```

## 📦 Getting Started

```bash
# Install dependencies
npm install

# Start development server
npm run dev
```

## ✅ TODO

- [ ] Add password reset functionality
- [ ] Implement question history dashboard
- [ ] Improve personalized feedback logic
- [ ] Add real SAT-style timer and progress tracker

## ✨ Contribution

1. Fork this repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License.
```
