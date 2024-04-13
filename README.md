<div align="center">
  <br />
    </a>
  <br />

  <div>
    <img src="https://img.shields.io/badge/-React_Native-black?style=for-the-badge&logoColor=white&logo=react&color=61DAFB" alt="react.js" />
    <img src="https://img.shields.io/badge/-Appwrite-black?style=for-the-badge&logoColor=white&logo=appwrite&color=FD366E" alt="appwrite" />
    <img src="https://img.shields.io/badge/NativeWind-black?style=for-the-badge&logoColor=white&logo=tailwindcss&color=06B6D4" alt="nativewind" />
  </div>

  <h3 align="center">Caleb Tech Hub</h3>

</div>

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. ⚙️ [Tech Stack](#tech-stack)
3. 🔋 [Features](#features)
4. 🤸 [Quick Start](#quick-start)
5. 🕸️ [Snippets](#snippets)
6. 🔗 [Links](#links)
7. 🚀 [More](#more)

## <a name="introduction">🤖 Introduction</a>

Built with React Native for seamless user experiences, Animatable for captivating animations, and integrated with the dependable backend systems of Appwrite,
this app showcases impressive design and functionality, enabling seamless sharing of AI videos within the community.

## <a name="tech-stack">⚙️ Tech Stack</a>

- React Native
- Expo
- Nativewind
- Animatable
- Appwrite

## <a name="features">🔋 Features</a>

👉 **Onboarding Screen**: Engaging graphics and clear instructions welcome users to the app.

👉 **Robust Authentication & Authorization System**: Secure email login safeguards user accounts.

👉 **Dynamic Home Screen with Animated Flat List**: Smoothly animated flat list showcases the latest videos for seamless browsing.

👉 **Pull-to-Refresh Functionality**: Users can refresh content with a simple pull gesture for up-to-date information.

👉 **Full-Text Search Capability**: Efficiently search through videos with real-time suggestions and instant results.

👉 **Tab Navigation**: Navigate between sections like Home, Search, and Profile with ease using tab navigation.

👉 **Post Creation Screen for Uploading Media**: Upload video and image posts directly from the app with integrated media selection.

👉 **Profile Screen with Detailed Insights**: View account details and activity, including uploaded videos and follower count, for a personalized experience.

👉 **Responsiveness**: Smooth performance and adaptability across various devices and screen sizes for a consistent user experience.

👉 **Animations**: Dynamic animations using the Animatable library to enhance user interaction and engagement throughout the app's UI.

and many more, including code architecture and reusability

## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up the project locally on your machine.

**Prerequisites**

Make sure you have the following installed on your machine:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)

**Installation**

Install the project dependencies using npm:

```bash
npm install
```

**Running the Project**

```bash
npm start
```

**Expo Go**

Download the [Expo Go](https://expo.dev/go) app onto your device, then use it to scan the QR code from Terminal and run.

## <a name="snippets">🕸️ Snippets</a>

<details>
<summary><code>tailwind.config.js</code></summary>

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./app/**/*.{js,jsx,ts,tsx}", "./components/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {
      colors: {
        primary: "#161622",
        secondary: {
          DEFAULT: "#FF9C01",
          100: "#FF9001",
          200: "#FF8E01",
        },
        black: {
          DEFAULT: "#000",
          100: "#1E1E2D",
          200: "#232533",
        },
        gray: {
          100: "#CDCDE0",
        },
      },
      fontFamily: {
        pthin: ["Poppins-Thin", "sans-serif"],
        pextralight: ["Poppins-ExtraLight", "sans-serif"],
        plight: ["Poppins-Light", "sans-serif"],
        pregular: ["Poppins-Regular", "sans-serif"],
        pmedium: ["Poppins-Medium", "sans-serif"],
        psemibold: ["Poppins-SemiBold", "sans-serif"],
        pbold: ["Poppins-Bold", "sans-serif"],
        pextrabold: ["Poppins-ExtraBold", "sans-serif"],
        pblack: ["Poppins-Black", "sans-serif"],
      },
    },
  },
  plugins: [],
};
```

</details>

<details>
<summary><code>Font Loaded</code></summary>

```javascript
const [fontsLoaded, error] = useFonts({
  "Poppins-Black": require("../assets/fonts/Poppins-Black.ttf"),
  "Poppins-Bold": require("../assets/fonts/Poppins-Bold.ttf"),
  "Poppins-ExtraBold": require("../assets/fonts/Poppins-ExtraBold.ttf"),
  "Poppins-ExtraLight": require("../assets/fonts/Poppins-ExtraLight.ttf"),
  "Poppins-Light": require("../assets/fonts/Poppins-Light.ttf"),
  "Poppins-Medium": require("../assets/fonts/Poppins-Medium.ttf"),
  "Poppins-Regular": require("../assets/fonts/Poppins-Regular.ttf"),
  "Poppins-SemiBold": require("../assets/fonts/Poppins-SemiBold.ttf"),
  "Poppins-Thin": require("../assets/fonts/Poppins-Thin.ttf"),
});

useEffect(() => {
  if (error) throw error;

  if (fontsLoaded) {
    SplashScreen.hideAsync();
  }
}, [fontsLoaded, error]);

if (!fontsLoaded && !error) {
  return null;
}
```

</details>

<details>
<summary><code>Dummy Videos for Appwrite</code></summary>

```javascript
const videos = [
  {
    title: "Get inspired to code",
    thumbnail:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660eff632e9b0[…]ht=2000&gravity=top&quality=100&project=660d0e00da0472f3ad52",
    video:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660f004955f51e7e3212/view?project=660d0e00da0472f3ad52",
    prompt:
      "Create a motivating AI driven video aimed at inspiring coding enthusiasts with simple language",
  },
  {
    title: "How AI Shapes Coding Future",
    thumbnail:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660f0294e36d8[…]ht=2000&gravity=top&quality=100&project=660d0e00da0472f3ad52",
    video:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660f032718759c0250ae/view?project=660d0e00da0472f3ad52",
    prompt: "Picture the future of coding with AI. Show AR VR",
  },
  {
    title: "Dalmatian's journey through Italy",
    thumbnail:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660f08374f22d[…]ht=2000&gravity=top&quality=100&project=660d0e00da0472f3ad52",
    video:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660f093a03c20c7b2d12/view?project=660d0e00da0472f3ad52",
    prompt:
      "Create a heartwarming video following the travels of dalmatian dog exploring beautiful Italy",
  },
  {
    title: "Meet small AI friends",
    thumbnail:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660f0aef26136[…]ht=2000&gravity=top&quality=100&project=660d0e00da0472f3ad52",
    video:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660f0b7855304dd4f802/view?project=660d0e00da0472f3ad52",
    prompt:
      "Make a video about a small blue AI robot blinking its eyes and looking at the screen",
  },
  {
    title: "Find inspiration in Every Line",
    thumbnail:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660fd24347331[…]ht=2000&gravity=top&quality=100&project=660d0e00da0472f3ad52",
    video:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660fd2cec9eb0298c9ac/view?project=660d0e00da0472f3ad52",
    prompt:
      "A buy working on his laptop that sparks excitement for coding, emphasizing the endless possibilities and personal growth it offers",
  },
  {
    title: "Japan's Blossoming temple",
    thumbnail:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660fd5105ae00[…]ht=2000&gravity=top&quality=100&project=660d0e00da0472f3ad52",
    video:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660fd543cc4792ba0611/view?project=660d0e00da0472f3ad52",
    prompt: "Create a captivating video journey through Japan's Sakura Temple",
  },
  {
    title: "A Glimpse into Tomorrow's VR World",
    thumbnail:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660fd68ced2ad[…]ht=2000&gravity=top&quality=100&project=660d0e00da0472f3ad52",
    video:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660fd6b103374105e099/view?project=660d0e00da0472f3ad52",
    prompt: "An imaginative video envisioning the future of Virtual Reality",
  },
  {
    title: "A World where Ideas Grow Big",
    thumbnail:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660fd7cb71f83[…]ht=2000&gravity=top&quality=100&project=660d0e00da0472f3ad52",
    video:
      "https://cloud.appwrite.io/v1/storage/buckets/660d0e59e293896f1eaf/files/660fd84ce8c5ff020f71/view?project=660d0e00da0472f3ad52",
    prompt:
      "Make a fun video about hackers and all the cool stuff they do with computers",
  },
];
```

</details>

## <a name="links">🔗 Links</a>

Assets and constants used in the project can be found [here](https://drive.google.com/drive/folders/1pckq7VAoqZlmsEfYaSsDltmQSESKm8h7?usp=sharing)
