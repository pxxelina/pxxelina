// Filename: App.jsx
import React from "react";

const tools = [
  { name: "JavaScript", color: "yellow-400", logo: "https://img.shields.io/badge/JavaScript-%23f7df1e?style=for-the-badge&logo=javascript&logoColor=black" },
  { name: "Python", color: "blue-900", logo: "https://img.shields.io/badge/Python-%2314354c?style=for-the-badge&logo=python&logoColor=white" },
  { name: "HTML5", color: "red-600", logo: "https://img.shields.io/badge/HTML5-%23e34f26?style=for-the-badge&logo=html5&logoColor=white" },
  { name: "CSS3", color: "blue-700", logo: "https://img.shields.io/badge/CSS3-%231572b6?style=for-the-badge&logo=css3&logoColor=white" },
  { name: "C++", color: "blue-800", logo: "https://img.shields.io/badge/C++-%2300599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" },
];

const projects = [
  {
    title: "Virtual Piano 🎹",
    desc: "Play beautiful melodies with this responsive web piano.",
    link: "https://your-piano-demo-link.vercel.app",
  },
  {
    title: "Virtual Cat 🐱",
    desc: "An interactive cat companion that reacts to your clicks and keyboard.",
    link: "https://your-virtual-cat-link.vercel.app",
  },
  {
    title: "My Bot 🤖 (in progress)",
    desc: "Building a smart bot to make digital life easier and fun.",
    link: "#", // Add when ready
  },
];

export default function App() {
  return (
    <div className="min-h-screen bg-pink-50 text-gray-900 font-sans selection:bg-pink-300 selection:text-white">
      {/* Header */}
      <header className="bg-pink-200 shadow-md py-8 mb-12 text-center">
        <h1 className="text-5xl font-extrabold tracking-wide mb-2">Lina Yassire</h1>
        <p className="text-xl text-pink-700 font-semibold">pxxelina — Digital Dreamer & Code Alchemist</p>
      </header>

      {/* About */}
      <section className="max-w-4xl mx-auto px-6 mb-16">
        <h2 className="text-3xl font-semibold mb-4 border-b-2 border-pink-300 inline-block pb-1">
          About Me
        </h2>
        <p className="text-lg leading-relaxed max-w-3xl mx-auto">
          Hi! I’m Lina, a coder who loves crafting magical digital experiences with a soft, cozy aesthetic.  
          I’m passionate about combining logic and creativity to build tools and art that feel like little gifts for the world.  
          Follow me on Instagram <a href="https://instagram.com/lina_yassire" className="text-pink-600 font-bold hover:underline">@lina_yassire</a> or reach me at <a href="mailto:linayassire00@gmail.com" className="text-pink-600 font-bold hover:underline">linayassire00@gmail.com</a>.
        </p>
      </section>

      {/* Toolbox */}
      <section className="max-w-4xl mx-auto px-6 mb-16">
        <h2 className="text-3xl font-semibold mb-6 border-b-2 border-pink-300 inline-block pb-1">
          Toolbox 🧰
        </h2>
        <div className="flex flex-wrap justify-center gap-6">
          {tools.map(({ name, logo }) => (
            <img key={name} src={logo} alt={name} className="h-12 rounded-lg shadow-md hover:scale-110 transition-transform" />
          ))}
        </div>
      </section>

      {/* Projects */}
      <section className="max-w-4xl mx-auto px-6 mb-20">
        <h2 className="text-3xl font-semibold mb-6 border-b-2 border-pink-300 inline-block pb-1">
          Projects ✨
        </h2>
        <div className="grid md:grid-cols-3 gap-8">
          {projects.map(({ title, desc, link }) => (
            <a
              href={link}
              key={title}
              target="_blank"
              rel="noopener noreferrer"
              className="bg-white p-6 rounded-xl shadow-md hover:shadow-pink-400 transition-shadow flex flex-col justify-between"
            >
              <h3 className="text-xl font-bold mb-2">{title}</h3>
              <p className="text-pink-700 mb-4">{desc}</p>
              <button className="self-start bg-pink-300 hover:bg-pink-400 text-white font-semibold py-2 px-4 rounded-lg transition">
                View Project
              </button>
            </a>
          ))}
        </div>
      </section>

      {/* Achievements & Stats */}
      <section className="max-w-4xl mx-auto px-6 mb-20">
        <h2 className="text-3xl font-semibold mb-6 border-b-2 border-pink-300 inline-block pb-1">
          Achievements & Stats 🏆
        </h2>
        <div className="flex flex-col items-center gap-8">
          <img
            src="https://github-profile-trophy.vercel.app/?username=pxxelina&theme=dracula&no-frame=true&title=Stars,Followers,Commits,Repositories"
            alt="GitHub trophies"
            className="max-w-md rounded-lg shadow-lg"
          />
          <img
            src="https://github-readme-stats.vercel.app/api?username=pxxelina&show_icons=true&theme=tokyonight&hide_border=true&count_private=true"
            alt="GitHub stats"
            className="max-w-md rounded-lg shadow-lg"
          />
          <img
            src="https://github-readme-stats.vercel.app/api/top-langs/?username=pxxelina&layout=compact&theme=tokyonight&hide_border=true"
            alt="Top languages"
            className="max-w-md rounded-lg shadow-lg"
          />
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-pink-200 py-6 text-center text-pink-800 font-semibold">
        Made with 💖 by Lina Yassire — <a href="https://github.com/pxxelina" className="underline hover:text-pink-600">pxxelina</a>
      </footer>
    </div>
  );
}











