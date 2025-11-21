import React from "react";

// Nikhil Shinde - Single-file React + Tailwind portfolio component
// Drop this component into a Next.js page (e.g., pages/index.js) or any React app

export default function NikhilPortfolio() {
  return (
    <main className="min-h-screen bg-gradient-to-b from-slate-50 via-white to-slate-100 text-slate-900 antialiased">
      <section className="max-w-6xl mx-auto p-6 md:p-12">
        {/* Header / Hero */}
        <header className="flex flex-col md:flex-row items-center gap-8 md:gap-12">
          <div className="relative w-48 h-48 md:w-60 md:h-60 rounded-2xl overflow-hidden shadow-2xl ring-1 ring-slate-200">
            <img
              src="/profile-placeholder.jpg"
              alt="Nikhil Shinde"
              className="w-full h-full object-cover transform hover:scale-105 transition duration-500"
            />
            <div className="absolute -bottom-4 left-4 bg-white/90 px-3 py-1 rounded-xl shadow backdrop-blur">
              <p className="text-xs text-slate-700">PCCoE, Pune · B.Tech Computer Eng.</p>
            </div>
          </div>

          <div className="flex-1">
            <h1 className="text-4xl md:text-5xl font-playfair font-bold leading-tight">Nikhil Subhash Shinde</h1>
            <p className="mt-2 text-slate-600 max-w-2xl">
              Passionate developer focused on modern web technologies, AI, and building delightful user experiences.
              Currently studying Computer Engineering at Pimpri Chinchwad College of Engineering (PCCoE), Pune.
            </p>

            <div className="mt-6 flex flex-wrap gap-3 items-center">
              <a
                href="https://nikhilshindeportfolio.vercel.app/"
                target="_blank"
                rel="noreferrer"
                className="inline-flex items-center gap-2 px-4 py-2 bg-emerald-500 text-white rounded-full shadow hover:shadow-lg transition"
              >
                View Live Portfolio
                <svg className="w-4 h-4" viewBox="0 0 24 24" fill="none">
                  <path d="M5 12h14M12 5l7 7-7 7" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round" />
                </svg>
              </a>

              <div className="flex items-center gap-3 text-slate-500">
                <a href="https://www.linkedin.com/in/nikhil-shinde-1b1b3b1b2/" target="_blank" rel="noreferrer" aria-label="LinkedIn" className="hover:text-slate-800">
                  <i className="fab fa-linkedin fa-lg"></i>
                </a>
                <a href="https://github.com/nikhilshinde01" target="_blank" rel="noreferrer" aria-label="GitHub" className="hover:text-slate-800">
                  <i className="fab fa-github fa-lg"></i>
                </a>
                <a href="https://twitter.com/nikhilshinde" target="_blank" rel="noreferrer" aria-label="Twitter" className="hover:text-slate-800">
                  <i className="fab fa-twitter fa-lg"></i>
                </a>
              </div>
            </div>

            <div className="mt-6 grid grid-cols-2 sm:grid-cols-4 gap-3 text-sm text-slate-700">
              <div className="bg-white p-3 rounded-lg shadow-sm">
                <p className="text-xs text-slate-400">HTML</p>
                <p className="font-semibold">20%</p>
              </div>
              <div className="bg-white p-3 rounded-lg shadow-sm">
                <p className="text-xs text-slate-400">CSS</p>
                <p className="font-semibold">20%</p>
              </div>
              <div className="bg-white p-3 rounded-lg shadow-sm">
                <p className="text-xs text-slate-400">JavaScript</p>
                <p className="font-semibold">60%</p>
              </div>
              <div className="bg-white p-3 rounded-lg shadow-sm">
                <p className="text-xs text-slate-400">C / Problem Solving</p>
                <p className="font-semibold">Core</p>
              </div>
            </div>
          </div>
        </header>

        {/* Divider */}
        <div className="my-10 h-px bg-gradient-to-r from-transparent via-slate-200 to-transparent" />

        {/* About + Skills */}
        <section className="grid md:grid-cols-3 gap-8">
          <article className="md:col-span-2 bg-white p-6 rounded-2xl shadow-lg">
            <h2 className="text-2xl font-semibold mb-4">About Me</h2>
            <p className="text-slate-700 leading-relaxed">
              I'm <strong>Nikhil Subhash Shinde</strong>, 18 years old, pursuing a B.Tech in Computer Engineering at PCCoE (Phule Pune University).
              I chose Computer Engineering for its scope and the creative problem solving it enables. I enjoy building web applications, learning
              about artificial intelligence, and solving algorithmic challenges.
            </p>

            <div className="mt-6 grid sm:grid-cols-2 gap-4">
              <div>
                <h3 className="text-sm text-slate-500">Education</h3>
                <p className="font-medium">PCCoE, Pune — B.Tech, Computer Engineering</p>
              </div>

              <div>
                <h3 className="text-sm text-slate-500">Contact</h3>
                <p className="font-medium">nikhilshinde@example.com</p>
              </div>
            </div>
          </article>

          <aside className="bg-white p-6 rounded-2xl shadow-lg">
            <h3 className="text-xl font-semibold mb-4">Skills</h3>

            <div className="space-y-4">
              <SkillBar label="JavaScript" percent={60} />
              <SkillBar label="HTML" percent={20} />
              <SkillBar label="CSS" percent={20} />
              <SkillBar label="C Programming" percent={50} />
              <SkillBar label="Web Development" percent={60} />
            </div>

            <h4 className="mt-6 text-sm text-slate-500">Tools</h4>
            <div className="mt-3 flex flex-wrap gap-2">
              {['React', 'Next.js', 'Vercel', 'Git', 'VS Code', 'npm'].map((t) => (
                <span key={t} className="text-xs px-3 py-1 bg-slate-100 rounded-full">{t}</span>
              ))}
            </div>
          </aside>
        </section>

        {/* Projects */}
        <section className="mt-12">
          <h2 className="text-2xl font-semibold mb-6">Selected Projects</h2>
          <div className="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
            <ProjectCard
              title="Animated Portfolio"
              desc="High-animation portfolio with Tailwind and modern UI — live on Vercel."
              href="https://nikhilshindeportfolio.vercel.app/"
            />
            <ProjectCard title="Project Two" desc="Short description for another project." href="#" />
            <ProjectCard title="Project Three" desc="Short description for another project." href="#" />
          </div>
        </section>

        {/* Contact */}
        <section className="mt-12 bg-gradient-to-r from-emerald-50 to-cyan-50 p-8 rounded-2xl shadow-inner">
          <div className="flex flex-col md:flex-row md:items-center md:justify-between gap-4">
            <div>
              <h3 className="text-xl font-semibold">Let's build something awesome</h3>
              <p className="text-slate-700">Open to internships, collaborations, and freelance projects.</p>
            </div>
            <div className="flex items-center gap-3">
              <a href="mailto:nikhilshinde@example.com" className="px-4 py-2 bg-slate-900 text-white rounded-md shadow">Email Me</a>
              <a href="https://github.com/nikhilshinde01" target="_blank" rel="noreferrer" className="px-4 py-2 border border-slate-900 rounded-md">View Code</a>
            </div>
          </div>
        </section>

        <footer className="mt-8 text-center text-sm text-slate-500">© {new Date().getFullYear()} Nikhil Subhash Shinde. All rights reserved.</footer>
      </section>
    </main>
  );
}


function SkillBar({ label, percent = 50 }) {
  return (
    <div>
      <div className="flex justify-between text-sm text-slate-600 mb-1">
        <span>{label}</span>
        <span>{percent}%</span>
      </div>
      <div className="w-full bg-slate-100 rounded-full h-3 overflow-hidden">
        <div
          className="h-3 rounded-full shadow-inner"
          style={{ width: `${percent}%`, background: 'linear-gradient(90deg,#06b6d4,#10b981)' }}
        />
      </div>
    </div>
  );
}

function ProjectCard({ title, desc, href = '#' }) {
  return (
    <article className="bg-white rounded-2xl p-5 shadow hover:shadow-2xl transition">
      <div className="flex items-center justify-between mb-4">
        <h4 className="font-semibold">{title}</h4>
        <span className="text-xs text-slate-400">Web App</span>
      </div>
      <p className="text-slate-600 mb-4">{desc}</p>
      <a href={href} target="_blank" rel="noreferrer" className="inline-block text-sm font-medium">
        View Project →
      </a>
    </article>
  );
}

