# sole-bunny-store /sole-bunny-store
├── public/
│   └── vite.svg (ou vide)
├── src/
│   ├── App.jsx ✅
│   ├── Home.jsx ✅
│   └── main.jsx ✅
├── index.html
├── package.json ✅
├── vite.config.js ✅
import React from "react";
import { Button } from "@/components/ui/button";

export default function Home() {
  return (
    <div className="min-h-screen bg-white text-gray-800 font-sans">
      {/* Header */}
      <header className="p-4 flex justify-between items-center border-b">
        <h1 className="text-xl font-bold">Sole Bunny Co.</h1>
        <nav>
          <ul className="flex gap-4">
            <li><a href="#shop" className="hover:text-blue-600">Shop</a></li>
            <li><a href="#about" className="hover:text-blue-600">About</a></li>
            <li><a href="#contact" className="hover:text-blue-600">Contact</a></li>
          </ul>
        </nav>
      </header>

      {/* Hero Section */}
      <section className="flex flex-col md:flex-row items-center justify-between p-8 md:p-16 bg-gradient-to-r from-pink-100 to-yellow-100">
        <div className="max-w-xl">
          <h2 className="text-4xl font-extrabold mb-4">Hop into style</h2>
          <p className="text-lg mb-6">Limited Easter Nike socks drop – pastel vibes, all-day comfort.</p>
          <Button className="bg-blue-600 text-white px-6 py-2 rounded-xl hover:bg-blue-700">Shop Now</Button>
        </div>
        <img
          src="https://example.com/easter-nike-socks.png"
          alt="Easter Nike Socks"
          className="w-64 h-auto mt-8 md:mt-0"
        />
      </section>

      {/* Product Section */}
      <section id="shop" className="p-8 md:p-16">
        <h3 className="text-2xl font-bold mb-4">Easter Nike Cotton Socks</h3>
        <p className="mb-4">These limited-edition Nike cotton socks bring the perfect mix of comfort, performance, and playful vibes. Featuring pastel colorways and soft breathable fabric, they're made to match your best spring fits.</p>
        <ul className="list-disc list-inside mb-4">
          <li>🐰 Premium cotton blend</li>
          <li>👟 Ideal for streetwear or sport</li>
          <li>🌸 Easter-only design – don’t miss the drop!</li>
        </ul>
        <p className="text-xl font-semibold mb-2">$12.99</p>
        <Button className="bg-green-600 text-white px-6 py-2 rounded-xl hover:bg-green-700">Add to Cart</Button>
      </section>

      {/* Footer */}
      <footer className="p-4 border-t text-sm text-center text-gray-500">
        © 2025 Sole Bunny Co. All rights reserved.
      </footer>
    </div>
  );
}
import React from 'react';
import Home from './Home';

function App() {
  return <Home />;
}

export default App;
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';
import './index.css';

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" href="/favicon.ico" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Sole Bunny Co.</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
});
{
  "name": "sole-bunny-store",
  "version": "1.0.0",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },
  "devDependencies": {
    "@vitejs/plugin-react": "^4.0.0",
    "vite": "^4.0.0"
  }
}
