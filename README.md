# Coffee-Bar
This is my first repositories
Author- Parth Sarthi
import React from "react";

// Coffee Bar Profile - Single-file React component
// Tailwind CSS classes used. Paste this file into a React app (Vite / Create React App)
// Make sure Tailwind is configured. Replace image URLs and contact endpoints as needed.

export default function CoffeeBarProfile() {
  const menu = [
    { name: "Espresso", price: "₹80", desc: "Bold single-shot espresso." },
    { name: "Cappuccino", price: "₹140", desc: "Espresso, steamed milk, froth." },
    { name: "Flat White", price: "₹150", desc: "Smooth microfoam, velvety texture." },
    { name: "Cold Brew", price: "₹160", desc: "Slow-steeped for 16 hours." },
    { name: "Hazelnut Latte", price: "₹170", desc: "House syrup, steamed milk." },
  ];

  const team = [
    { name: "Asha Patel", role: "Head Barista", img: "https://images.unsplash.com/photo-1544005313-94ddf0286df2?w=800&q=60" },
    { name: "Rohit Singh", role: "Roast Master", img: "https://images.unsplash.com/photo-1547425260-76bcadfb4f2c?w=800&q=60" },
    { name: "Nina Roy", role: "Pastry Chef", img: "https://images.unsplash.com/photo-1523986371872-9d3ba2e2f642?w=800&q=60" },
  ];

  return (
    <div className="min-h-screen bg-amber-50 text-slate-800">
      <header className="bg-amber-600 text-amber-50">
        <div className="max-w-6xl mx-auto px-6 py-6 flex items-center justify-between">
          <div className="flex items-center gap-4">
            <div className="w-12 h-12 rounded-full bg-amber-100 flex items-center justify-center text-amber-700 font-bold">CB</div>
            <div>
              <h1 className="text-xl font-extrabold leading-none">Coffee Bar</h1>
              <p className="text-sm opacity-90">Brewed with love in your neighborhood</p>
            </div>
          </div>

          <nav className="hidden md:flex gap-6 items-center">
            <a href="#about" className="hover:underline">About</a>
            <a href="#menu" className="hover:underline">Menu</a>
            <a href="#team" className="hover:underline">Team</a>
            <a href="#contact" className="hover:underline">Contact</a>
            <a href="https://github.com/" target="_blank" rel="noreferrer" className="px-3 py-1 bg-amber-100 text-amber-800 rounded-md shadow-sm">View on GitHub</a>
          </nav>

          <button className="md:hidden p-2 rounded-md bg-amber-700/20">Menu</button>
        </div>
      </header>

      <main className="max-w-6xl mx-auto px-6 py-12">
        {/* Hero */}
        <section className="grid md:grid-cols-2 gap-8 items-center">
          <div>
            <h2 className="text-4xl md:text-5xl font-extrabold">Sip. Savor. Smile.</h2>
            <p className="mt-4 text-lg text-slate-700">Handcrafted coffee, seasonal pastries, and warm community vibes — right in the heart of town.</p>

            <div className="mt-6 flex gap-4">
              <a href="#menu" className="inline-block px-6 py-3 bg-amber-600 text-amber-50 rounded-lg shadow">See Menu</a>
              <a href="#contact" className="inline-block px-6 py-3 border border-amber-600 rounded-lg">Book a Table</a>
            </div>

            <div className="mt-8 grid grid-cols-3 gap-3">
              <div className="rounded-lg overflow-hidden shadow">
                <img alt="coffee" src="https://images.unsplash.com/photo-1511920170033-f8396924c348?w=800&q=60" className="w-full h-24 object-cover" />
              </div>
              <div className="rounded-lg overflow-hidden shadow">
                <img alt="latte" src="https://images.unsplash.com/photo-1509042239860-f550ce710b93?w=800&q=60" className="w-full h-24 object-cover" />
              </div>
              <div className="rounded-lg overflow-hidden shadow">
                <img alt="pastry" src="https://images.unsplash.com/photo-1544025162-d76694265947?w=800&q=60" className="w-full h-24 object-cover" />
              </div>
            </div>
          </div>

          <div className="rounded-2xl overflow-hidden shadow-lg">
            <img alt="shop" src="https://images.unsplash.com/photo-1521305916504-4a1121188589?w=1200&q=80" className="w-full h-80 object-cover" />
          </div>
        </section>

        {/* About */}
        <section id="about" className="mt-16 bg-white rounded-xl p-8 shadow">
          <h3 className="text-2xl font-bold">About Coffee Bar</h3>
          <p className="mt-3 text-slate-700">Founded in 2020, Coffee Bar sources ethically traded beans and roasts small batches on site. We care about great coffee and a friendly place to gather.</p>

          <div className="mt-6 grid md:grid-cols-3 gap-4">
            <div className="p-4 border rounded-lg">
              <h4 className="font-semibold">Open Hours</h4>
              <p className="mt-1 text-sm">Mon–Fri: 7am–7pm<br/>Sat–Sun: 8am–8pm</p>
            </div>
            <div className="p-4 border rounded-lg">
              <h4 className="font-semibold">Address</h4>
              <p className="mt-1 text-sm">123 Brew Lane, Coffee City</p>
            </div>
            <div className="p-4 border rounded-lg">
              <h4 className="font-semibold">What we do</h4>
              <p className="mt-1 text-sm">Specialty coffees, seasonal drinks, pastries, and cozy seating.</p>
            </div>
          </div>
        </section>

        {/* Menu */}
        <section id="menu" className="mt-12">
          <h3 className="text-2xl font-bold">Menu</h3>
          <p className="mt-2 text-slate-600">A curated selection — rotate seasonally.</p>

          <div className="mt-6 grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
            {menu.map((item) => (
              <article key={item.name} className="bg-white rounded-xl p-5 shadow hover:scale-[1.01] transition-transform">
                <div className="flex items-start justify-between">
                  <div>
                    <h4 className="font-semibold text-lg">{item.name}</h4>
                    <p className="text-sm mt-1 text-slate-600">{item.desc}</p>
                  </div>
                  <div className="text-amber-700 font-bold">{item.price}</div>
                </div>
                <div className="mt-4 flex gap-2">
                  <button className="px-3 py-1 border rounded-md text-sm">Add</button>
                  <button className="px-3 py-1 bg-amber-600 text-amber-50 rounded-md text-sm">Order</button>
                </div>
              </article>
            ))}
          </div>
        </section>

        {/* Team */}
        <section id="team" className="mt-12">
          <h3 className="text-2xl font-bold">Meet the Team</h3>
          <div className="mt-6 grid sm:grid-cols-2 md:grid-cols-3 gap-6">
            {team.map((p) => (
              <div key={p.name} className="bg-white rounded-xl p-4 text-center shadow">
                <img src={p.img} alt={p.name} className="w-28 h-28 rounded-full mx-auto object-cover" />
                <h4 className="mt-3 font-semibold">{p.name}</h4>
                <p className="text-sm text-slate-600">{p.role}</p>
              </div>
            ))}
          </div>
        </section>

        {/* Contact */}
        <section id="contact" className="mt-12 bg-white rounded-xl p-6 shadow">
          <h3 className="text-2xl font-bold">Contact & Map</h3>
          <div className="mt-4 grid md:grid-cols-2 gap-6">
            <form className="space-y-3">
              <div>
                <label className="block text-sm font-medium">Name</label>
                <input className="mt-1 w-full border rounded-md p-2" placeholder="Your name" />
              </div>
              <div>
                <label className="block text-sm font-medium">Email</label>
                <input className="mt-1 w-full border rounded-md p-2" placeholder="you@example.com" />
              </div>
              <div>
                <label className="block text-sm font-medium">Message</label>
                <textarea className="mt-1 w-full border rounded-md p-2" rows={4} placeholder="Tell us how we can help" />
              </div>
              <div className="flex gap-3">
                <button type="button" className="px-4 py-2 bg-amber-600 text-white rounded-md">Send</button>
                <button type="reset" className="px-4 py-2 border rounded-md">Reset</button>
              </div>
            </form>

            <div>
              {/* Replace the iframe src with your actual Google Maps embed for the address */}
              <iframe
                title="Coffee Bar location"
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3153.0190964413695!2d144.9631579155619!3d-37.814107979751504!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6ad65d43f2f3b7c1%3A0x2a0c3f2f0f3b7c1!2sFederation%20Square!5e0!3m2!1sen!2sin!4v1600000000000!5m2!1sen!2sin"
                className="w-full h-72 rounded-md border-0"
                allowFullScreen={false}
                loading="lazy"
              />

              <div className="mt-4 text-sm text-slate-600">
                <p><strong>Phone:</strong> +91 98765 43210</p>
                <p><strong>Email:</strong> hello@coffeebar.example</p>
              </div>
            </div>
          </div>
        </section>
      </main>

      <footer className="bg-amber-700 text-amber-50">
        <div className="max-w-6xl mx-auto px-6 py-6 flex flex-col md:flex-row items-center justify-between gap-4">
          <p className="text-sm">© {new Date().getFullYear()} Coffee Bar — All rights reserved</p>
          <div className="flex gap-3">
            <a href="#" aria-label="Instagram" className="hover:underline">Instagram</a>
            <a href="#" aria-label="Facebook" className="hover:underline">Facebook</a>
            <a href="#" aria-label="Twitter" className="hover:underline">Twitter</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
