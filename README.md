# Threads Feed Clone Tutorial

This repository showcases a clone of a Threads Feed, using technologies like TypeScript, React Native, and Expo.

![Threads Feed Clone Screenshot](/assets/images/thread-clone-screenshot.png)

## Features

- TypeScript + Expo + React Native Application with dynamic routing using Expo Router.
- Utilizes JSON Images from Lottie with the help of the "lottie-react-native": "^6.3.1" package.
- Generates dummy data with the "@faker-js/faker": "^8.2.0" library.

## Not Included

- Account login/security/account persistence.
- Data Storage.

## Prerequisites

Before cloning and running the application, make sure you have the necessary tools to simulate the application (such as a mobile simulator). Please review [Expo's documentation](https://docs.expo.dev/get-started/installation/) for further guidance.

## Getting Started

1. **Clone the repository:**

   ```bash
   git clone https://github.com/PSkinnerTech/threads-feed-clone
   ```

2. **Navigate to the project directory:**

   ```bash
   cd threads-feed-clone
   ```

3. **Install dependencies:**

   ```bash
   yarn
   ```

4. **Start the project:**

   ```bash
   npx expo start
   ```

5. **Simulation:**

   - For iOS simulation, press `i`.
   - For Android simulation, press `a`.

   Alternatively, you can scan the generated QR code with the Expo Go app on your smartphone. Note: Ensure your smartphone and computer are connected to the same Wi-Fi network.

6. Congratulations! You've successfully cloned and run the application.

## Generating Your Own Dummy Data for Threads

Follow these steps to create dummy data for your social media or Threads:

1. **Create a new directory named `types` at the root of your project.**

2. **Inside the `types` directory, create a file named `threads.ts` and set up your interfaces as follows:**

```typescript
export interface Thread {
  id: string;
  author: User;
  content: string;
  image?: string;
  replies?: Reply[];
  repliesCount: number;
  likesCount: number;
  mention?: boolean;
  mentionUser: User;
  createdAt: string;
}

export interface Reply {
  id: string;
  author: User;
  content: string;
  likes: number;
  createdAt: string;
}

export interface User {
  id: string;
  name: string;
  username: string;
  verified: boolean;
  photo: string;
  bio: string;
  link?: string;
  followers?: User[];
}
```

3. **Create a new directory named `utils` at the root of your project.**

4. **Inside the `utils` directory, create a file named `generate-dummy-data.ts`.**

5. **Install "@faker-js/faker" as a development dependency:**

   ```bash
   yarn add -D @faker-js/faker
   ```

   or

   ```bash
   npm i -D @faker-js/faker
   ```

6. **Set up your dummy data generation in `generate-dummy-data.ts` as provided in the initial instructions.**

7. With the above steps completed, you can design and structure your project to display the social media timeline as you see fit.

## Conclusion

This tutorial gives you a foundation for building your Threads Feed application. For further enhancements or functionalities, feel free to modify or extend the existing codebase. Happy Hacking!

## License

This project is licensed under the MIT License.
