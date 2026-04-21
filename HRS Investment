"use client";

import React, { useState } from "react";
import {
  Coffee,
  Music,
  Sparkles,
  ShoppingBag,
  Handshake,
  Phone,
  Mail,
  MessageCircle,
  ChevronRight,
  TrendingUp,
  ShieldCheck,
  Zap,
  Package,
} from "lucide-react";
import { Toaster, toast } from "sonner";

const HumsafarLandingPage = () => {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
    phone: "",
    interest_type: "Investor",
    message: "",
  });
  const [loading, setLoading] = useState(false);

  const handleSubmit = async (e) => {
    e.preventDefault();
    setLoading(true);
    try {
      const response = await fetch("/api/leads", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(formData),
      });

      if (!response.ok) throw new Error("Submission failed");

      toast.success("Thank you for your interest! We'll be in touch soon.");
      setFormData({
        name: "",
        email: "",
        phone: "",
        interest_type: "Investor",
        message: "",
      });
    } catch (error) {
      toast.error("Something went wrong. Please try again.");
    } finally {
      setLoading(false);
    }
  };

  const verticals = [
    {
      title: "Cafe & Night Club",
      icon: <Coffee className="w-8 h-8 text-[#ffd700]" />,
      items: [
        {
          name: "Luxury Cafe",
          desc: "Premium hangout with modern vibes",
          icon: <Coffee className="w-5 h-5" />,
        },
        {
          name: "DJ Night",
          desc: "Music, lights, and party experience",
          icon: <Music className="w-5 h-5" />,
        },
        {
          name: "Private Events",
          desc: "Birthday, party, special nights",
          icon: <Sparkles className="w-5 h-5" />,
        },
      ],
    },
    {
      title: "Personal Care",
      icon: <Sparkles className="w-8 h-8 text-[#ffd700]" />,
      items: [
        {
          name: "Hair Oil",
          desc: "Natural essence for healthy hair",
          icon: <Zap className="w-5 h-5" />,
        },
        {
          name: "Face Wash",
          desc: "Gentle cleaning for glowing skin",
          icon: <Sparkles className="w-5 h-5" />,
        },
        {
          name: "Cream",
          desc: "Luxury hydration for daily care",
          icon: <ShieldCheck className="w-5 h-5" />,
        },
      ],
    },
    {
      title: "FMCG (Cafe Vibe)",
      icon: <ShoppingBag className="w-8 h-8 text-[#ffd700]" />,
      items: [
        {
          name: "Energy Drinks",
          desc: "Instant boost with premium taste",
          icon: <Zap className="w-5 h-5" />,
        },
        {
          name: "Snacks",
          desc: "Crunchy, tasty, and uniquely Humsafar",
          icon: <ShoppingBag className="w-5 h-5" />,
        },
        {
          name: "Combo Packs",
          desc: "Curated lifestyle essentials",
          icon: <TrendingUp className="w-5 h-5" />,
        },
      ],
    },
  ];

  return (
    <div className="min-h-screen bg-[#0a0a0a] text-white font-poppins selection:bg-[#ffd700] selection:text-black">
      <Toaster position="top-center" expand={true} richColors />

      {/* Navigation */}
      <nav className="fixed top-0 w-full z-50 bg-[#0a0a0a]/80 backdrop-blur-md border-b border-white/10">
        <div className="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
          <div className="text-2xl font-bold tracking-widest text-[#ffd700]">
            HUMSAFAR
          </div>
          <div className="hidden md:flex gap-8 text-sm uppercase tracking-widest font-medium">
            <a href="#about" className="hover:text-[#ffd700] transition-colors">
              About
            </a>
            <a
              href="#verticals"
              className="hover:text-[#ffd700] transition-colors"
            >
              Verticals
            </a>
            <a
              href="#investment"
              className="hover:text-[#ffd700] transition-colors"
            >
              Investment
            </a>
            <a
              href="#contact"
              className="hover:text-[#ffd700] transition-colors"
            >
              Contact
            </a>
          </div>
          <button
            onClick={() =>
              document
                .getElementById("investment")
                .scrollIntoView({ behavior: "smooth" })
            }
            className="bg-[#ffd700] text-black px-6 py-2 text-sm font-bold uppercase tracking-wider hover:bg-[#ffea00] transition-all transform hover:scale-105"
          >
            Invest Now
          </button>
        </div>
      </nav>

      {/* Hero Section */}
      <header className="relative h-screen flex items-center justify-center overflow-hidden">
        <div className="absolute inset-0 z-0">
          <div className="absolute inset-0 bg-gradient-to-b from-black/60 via-black/40 to-[#0a0a0a]" />
          <div className="absolute inset-0 bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-[#ffd70010] via-transparent to-transparent" />
        </div>

        <div className="relative z-10 text-center px-6 max-w-4xl mx-auto">
          <h1 className="text-6xl md:text-8xl font-bold tracking-[0.2em] text-[#ffd700] mb-6 drop-shadow-[0_0_15px_rgba(255,215,0,0.3)]">
            HUMSAFAR
          </h1>
          <p className="text-xl md:text-2xl text-white/70 tracking-[0.3em] uppercase mb-12">
            Cafe | Night Club | Lifestyle | FMCG
          </p>
          <div className="flex flex-col md:flex-row gap-4 justify-center">
            <button
              onClick={() =>
                document
                  .getElementById("verticals")
                  .scrollIntoView({ behavior: "smooth" })
              }
              className="px-10 py-4 border border-[#ffd700] text-[#ffd700] font-bold uppercase tracking-widest hover:bg-[#ffd700] hover:text-black transition-all duration-300"
            >
              Explore Brand
            </button>
            <button
              onClick={() =>
                document
                  .getElementById("investment")
                  .scrollIntoView({ behavior: "smooth" })
              }
              className="px-10 py-4 bg-[#ffd700] text-black font-bold uppercase tracking-widest hover:bg-[#ffea00] transition-all duration-300 shadow-[0_0_20px_rgba(255,215,0,0.3)]"
            >
              Become Investor
            </button>
          </div>
        </div>

        <div className="absolute bottom-10 left-1/2 -translate-x-1/2 bounce-animation">
          <div className="w-1 h-12 rounded-full bg-gradient-to-b from-[#ffd700] to-transparent" />
        </div>
      </header>

      {/* Brand Verticals */}
      <section id="verticals" className="py-24 px-6 bg-[#0f0f0f]">
        <div className="max-w-7xl mx-auto">
          <div className="text-center mb-16">
            <h2 className="text-4xl md:text-5xl font-bold mb-4 tracking-tight">
              Our Ecosystem
            </h2>
            <div className="w-20 h-1 bg-[#ffd700] mx-auto mb-6" />
            <p className="text-white/50 max-w-2xl mx-auto">
              A diversified lifestyle brand touching every aspect of modern
              luxury and daily essentials.
            </p>
          </div>

          {/* Cafe & Night Club with Images */}
          <div className="mb-20">
            <div className="flex items-center gap-4 mb-8">
              <Coffee className="w-8 h-8 text-[#ffd700]" />
              <h3 className="text-3xl font-bold text-[#ffd700]">
                Cafe & Night Club
              </h3>
            </div>

            {/* Cafe Hero Image */}
            <div className="mb-12 rounded-3xl overflow-hidden border border-[#ffd700]/20 hover:border-[#ffd700]/50 transition-all duration-300">
              <img
                src="https://raw.createusercontent.com/b805a87c-a9de-407d-8363-82e73d1eaa4b/"
                alt="Luxury Cafe Interior"
                className="w-full h-[500px] object-cover"
              />
              <div className="bg-[#1a1a1a] p-6">
                <h4 className="text-2xl font-bold text-[#ffd700] mb-2">
                  Luxury Cafe Experience
                </h4>
                <p className="text-white/70">
                  Premium hangout with modern vibes and golden aesthetics
                </p>
              </div>
            </div>

            {/* Night Club Hero Image */}
            <div className="mb-12 rounded-3xl overflow-hidden border border-[#ffd700]/20 hover:border-[#ffd700]/50 transition-all duration-300">
              <img
                src="https://raw.createusercontent.com/01dc486e-5fcf-43b4-8df3-8e4a39d82ee3/"
                alt="Night Club Experience"
                className="w-full h-[500px] object-cover"
              />
              <div className="bg-[#1a1a1a] p-6">
                <h4 className="text-2xl font-bold text-[#ffd700] mb-2">
                  DJ Nights & Events
                </h4>
                <p className="text-white/70">
                  Music, lights, and unforgettable party experiences
                </p>
              </div>
            </div>

            {/* Features Grid */}
            <div className="grid md:grid-cols-3 gap-6">
              <div className="p-6 rounded-2xl bg-[#1a1a1a] border border-white/5 hover:border-[#ffd700]/30 transition-all">
                <Coffee className="w-6 h-6 text-[#ffd700] mb-3" />
                <h4 className="font-bold text-white/90 mb-2">
                  Premium Coffee Bar
                </h4>
                <p className="text-sm text-white/50">
                  Artisan coffee and specialty beverages
                </p>
              </div>
              <div className="p-6 rounded-2xl bg-[#1a1a1a] border border-white/5 hover:border-[#ffd700]/30 transition-all">
                <Music className="w-6 h-6 text-[#ffd700] mb-3" />
                <h4 className="font-bold text-white/90 mb-2">
                  Live DJ Sessions
                </h4>
                <p className="text-sm text-white/50">
                  World-class DJs and sound systems
                </p>
              </div>
              <div className="p-6 rounded-2xl bg-[#1a1a1a] border border-white/5 hover:border-[#ffd700]/30 transition-all">
                <Sparkles className="w-6 h-6 text-[#ffd700] mb-3" />
                <h4 className="font-bold text-white/90 mb-2">Private Events</h4>
                <p className="text-sm text-white/50">
                  Birthdays, parties, and special nights
                </p>
              </div>
            </div>
          </div>

          {/* Personal Care with Product Images */}
          <div className="mb-20">
            <div className="flex items-center gap-4 mb-8">
              <Sparkles className="w-8 h-8 text-[#ffd700]" />
              <h3 className="text-3xl font-bold text-[#ffd700]">
                RUSA Personal Care
              </h3>
            </div>

            <div className="grid md:grid-cols-3 gap-8">
              {/* Hair Oil */}
              <div className="group rounded-3xl overflow-hidden bg-[#1a1a1a] border border-white/5 hover:border-[#ffd700]/40 transition-all duration-500 hover:scale-105 transform">
                <div className="h-80 overflow-hidden">
                  <img
                    src="https://raw.createusercontent.com/eb2e5f36-74ca-4ec5-8c56-9ce0a9d5e545/"
                    alt="RUSA Hair Oil"
                    className="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
                  />
                </div>
                <div className="p-6">
                  <Zap className="w-6 h-6 text-[#ffd700] mb-3" />
                  <h4 className="text-xl font-bold text-white/90 mb-2">
                    Premium Hair Oil
                  </h4>
                  <p className="text-sm text-white/50">
                    Natural essence for healthy, lustrous hair
                  </p>
                </div>
              </div>

              {/* Face Wash */}
              <div className="group rounded-3xl overflow-hidden bg-[#1a1a1a] border border-white/5 hover:border-[#ffd700]/40 transition-all duration-500 hover:scale-105 transform">
                <div className="h-80 overflow-hidden">
                  <img
                    src="https://raw.createusercontent.com/ea42de12-c409-4a2d-a9ab-9f6e40f4672d/"
                    alt="RUSA Face Wash"
                    className="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
                  />
                </div>
                <div className="p-6">
                  <Sparkles className="w-6 h-6 text-[#ffd700] mb-3" />
                  <h4 className="text-xl font-bold text-white/90 mb-2">
                    Luxury Face Wash
                  </h4>
                  <p className="text-sm text-white/50">
                    Gentle cleaning for glowing skin
                  </p>
                </div>
              </div>

              {/* Face Cream */}
              <div className="group rounded-3xl overflow-hidden bg-[#1a1a1a] border border-white/5 hover:border-[#ffd700]/40 transition-all duration-500 hover:scale-105 transform">
                <div className="h-80 overflow-hidden">
                  <img
                    src="https://raw.createusercontent.com/fb8c4b81-7b4f-410b-a282-2157429ab92e/"
                    alt="RUSA Face Cream"
                    className="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
                  />
                </div>
                <div className="p-6">
                  <ShieldCheck className="w-6 h-6 text-[#ffd700] mb-3" />
                  <h4 className="text-xl font-bold text-white/90 mb-2">
                    Hydrating Cream
                  </h4>
                  <p className="text-sm text-white/50">
                    Luxury hydration for daily care
                  </p>
                </div>
              </div>
            </div>
          </div>

          {/* FMCG with Product Images */}
          <div>
            <div className="flex items-center gap-4 mb-8">
              <ShoppingBag className="w-8 h-8 text-[#ffd700]" />
              <h3 className="text-3xl font-bold text-[#ffd700]">
                FMCG (Cafe Vibe)
              </h3>
            </div>

            <div className="grid md:grid-cols-3 gap-8">
              {/* Energy Drinks */}
              <div className="group rounded-3xl overflow-hidden bg-[#1a1a1a] border border-white/5 hover:border-[#ffd700]/40 transition-all duration-500 hover:scale-105 transform">
                <div className="h-80 overflow-hidden">
                  <img
                    src="https://raw.createusercontent.com/fa1c5b46-109a-4c3d-a1d0-b4cacf742c89/"
                    alt="Energy Drinks"
                    className="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
                  />
                </div>
                <div className="p-6">
                  <Zap className="w-6 h-6 text-[#ffd700] mb-3" />
                  <h4 className="text-xl font-bold text-white/90 mb-2">
                    Energy Drinks
                  </h4>
                  <p className="text-sm text-white/50">
                    Instant boost with premium taste
                  </p>
                </div>
              </div>

              {/* Snacks */}
              <div className="p-8 rounded-3xl bg-[#1a1a1a] border border-white/5 hover:border-[#ffd700]/30 transition-all duration-500 hover:scale-105 transform flex flex-col justify-center items-center">
                <ShoppingBag className="w-12 h-12 text-[#ffd700] mb-4" />
                <h4 className="text-xl font-bold text-white/90 mb-2 text-center">
                  Premium Snacks
                </h4>
                <p className="text-sm text-white/50 text-center">
                  Crunchy, tasty, and uniquely Humsafar
                </p>
              </div>

              {/* Combo Packs */}
              <div className="p-8 rounded-3xl bg-[#1a1a1a] border border-white/5 hover:border-[#ffd700]/30 transition-all duration-500 hover:scale-105 transform flex flex-col justify-center items-center">
                <TrendingUp className="w-12 h-12 text-[#ffd700] mb-4" />
                <h4 className="text-xl font-bold text-white/90 mb-2 text-center">
                  Combo Packs
                </h4>
                <p className="text-sm text-white/50 text-center">
                  Curated lifestyle essentials
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Investment Opportunity */}
      <section id="investment" className="py-24 px-6 relative overflow-hidden">
        <div className="absolute top-0 left-0 w-full h-full bg-[#ffd700]/5 -z-10" />
        <div className="max-w-7xl mx-auto flex flex-col lg:flex-row gap-16 items-center">
          <div className="lg:w-1/2">
            <h2 className="text-4xl md:text-6xl font-bold mb-8 leading-tight">
              Invest in the <span className="text-[#ffd700]">Future</span> of
              Lifestyle
            </h2>
            <div className="space-y-8 mb-10">
              <div className="flex gap-6">
                <div className="flex-shrink-0 w-12 h-12 bg-[#ffd700] text-black rounded-full flex items-center justify-center font-bold text-xl">
                  ₹
                </div>
                <div>
                  <h4 className="text-xl font-bold mb-2">
                    50 Lakh Opportunity
                  </h4>
                  <p className="text-white/60">
                    Strategic capital injection to scale our cafe network and
                    expand FMCG distribution nationwide.
                  </p>
                </div>
              </div>
              <div className="flex gap-6">
                <div className="flex-shrink-0 w-12 h-12 bg-white/10 rounded-full flex items-center justify-center">
                  <TrendingUp className="text-[#ffd700]" />
                </div>
                <div>
                  <h4 className="text-xl font-bold mb-2">
                    High Growth Potential
                  </h4>
                  <p className="text-white/60">
                    Targeting 3x revenue growth within 24 months through
                    omnichannel brand presence.
                  </p>
                </div>
              </div>
              <div className="flex gap-6">
                <div className="flex-shrink-0 w-12 h-12 bg-white/10 rounded-full flex items-center justify-center">
                  <Handshake className="text-[#ffd700]" />
                </div>
                <div>
                  <h4 className="text-xl font-bold mb-2">
                    Exclusive Partnership
                  </h4>
                  <p className="text-white/60">
                    Early investors gain equity stake and priority in future
                    funding rounds.
                  </p>
                </div>
              </div>
            </div>
          </div>

          <div className="lg:w-1/2 w-full">
            <div className="bg-[#1a1a1a] p-8 md:p-10 rounded-3xl border border-white/10 shadow-2xl relative">
              <div className="absolute -top-4 -right-4 bg-[#ffd700] text-black text-xs font-bold py-2 px-4 rounded-full uppercase tracking-tighter">
                Limited Slot
              </div>
              <h3 className="text-2xl font-bold mb-6 text-center">
                Investor Inquiry
              </h3>
              <form onSubmit={handleSubmit} className="space-y-4">
                <div className="grid md:grid-cols-2 gap-4">
                  <input
                    type="text"
                    placeholder="Full Name"
                    required
                    value={formData.name}
                    onChange={(e) =>
                      setFormData({ ...formData, name: e.target.value })
                    }
                    className="w-full bg-black/40 border border-white/10 rounded-xl px-5 py-4 focus:border-[#ffd700] outline-none transition-all"
                  />
                  <input
                    type="email"
                    placeholder="Email Address"
                    required
                    value={formData.email}
                    onChange={(e) =>
                      setFormData({ ...formData, email: e.target.value })
                    }
                    className="w-full bg-black/40 border border-white/10 rounded-xl px-5 py-4 focus:border-[#ffd700] outline-none transition-all"
                  />
                </div>
                <input
                  type="tel"
                  placeholder="Phone Number"
                  value={formData.phone}
                  onChange={(e) =>
                    setFormData({ ...formData, phone: e.target.value })
                  }
                  className="w-full bg-black/40 border border-white/10 rounded-xl px-5 py-4 focus:border-[#ffd700] outline-none transition-all"
                />
                <select
                  value={formData.interest_type}
                  onChange={(e) =>
                    setFormData({ ...formData, interest_type: e.target.value })
                  }
                  className="w-full bg-black/40 border border-white/10 rounded-xl px-5 py-4 focus:border-[#ffd700] outline-none transition-all appearance-none"
                >
                  <option value="Investor">Interested in Investing</option>
                  <option value="Partner">Business Partnership</option>
                  <option value="Other">Other Inquiry</option>
                </select>
                <textarea
                  placeholder="Tell us about your interest"
                  rows="4"
                  value={formData.message}
                  onChange={(e) =>
                    setFormData({ ...formData, message: e.target.value })
                  }
                  className="w-full bg-black/40 border border-white/10 rounded-xl px-5 py-4 focus:border-[#ffd700] outline-none transition-all resize-none"
                />
                <button
                  type="submit"
                  disabled={loading}
                  className="w-full bg-[#ffd700] text-black font-bold py-5 rounded-xl uppercase tracking-widest hover:bg-[#ffea00] transition-all disabled:opacity-50 flex items-center justify-center gap-3"
                >
                  {loading ? (
                    "Submitting..."
                  ) : (
                    <>
                      Submit Inquiry <ChevronRight className="w-5 h-5" />
                    </>
                  )}
                </button>
              </form>
            </div>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section
        id="contact"
        className="py-24 px-6 bg-black border-t border-white/5"
      >
        <div className="max-w-7xl mx-auto">
          <div className="grid md:grid-cols-2 gap-16">
            <div>
              <h2 className="text-4xl font-bold mb-8">
                Get In <span className="text-[#ffd700]">Touch</span>
              </h2>
              <p className="text-white/60 mb-12 max-w-md">
                Reach out to us directly for immediate inquiries regarding the
                brand or investment opportunities.
              </p>

              <div className="space-y-8">
                <div className="flex gap-5 items-center">
                  <div className="w-12 h-12 bg-[#1a1a1a] rounded-full flex items-center justify-center border border-white/5">
                    <Phone className="text-[#ffd700] w-5 h-5" />
                  </div>
                  <div>
                    <p className="text-xs uppercase tracking-widest text-white/40 mb-1">
                      Call Us
                    </p>
                    <p className="text-lg font-bold">+91 8509728920</p>
                  </div>
                </div>
                <div className="flex gap-5 items-center">
                  <div className="w-12 h-12 bg-[#1a1a1a] rounded-full flex items-center justify-center border border-white/5">
                    <Mail className="text-[#ffd700] w-5 h-5" />
                  </div>
                  <div>
                    <p className="text-xs uppercase tracking-widest text-white/40 mb-1">
                      Email Us
                    </p>
                    <p className="text-lg font-bold">
                      mubarakshaikh86176@gmail.com
                    </p>
                  </div>
                </div>
                <div className="flex gap-5 items-center">
                  <div className="w-12 h-12 bg-[#1a1a1a] rounded-full flex items-center justify-center border border-white/5">
                    <MessageCircle className="text-[#ffd700] w-5 h-5" />
                  </div>
                  <div>
                    <p className="text-xs uppercase tracking-widest text-white/40 mb-1">
                      WhatsApp
                    </p>
                    <a
                      href="https://wa.me/918509728920"
                      target="_blank"
                      rel="noopener noreferrer"
                      className="text-lg font-bold hover:text-[#ffd700] transition-colors"
                    >
                      Chat with Mubarak Shaikh
                    </a>
                  </div>
                </div>
              </div>
            </div>

            <div className="relative group">
              <div className="absolute inset-0 bg-[#ffd700]/5 blur-3xl -z-10 group-hover:bg-[#ffd700]/10 transition-all" />
              <div className="h-full flex items-center justify-center">
                <div className="text-center">
                  <div className="text-8xl mb-8 opacity-20 font-bold tracking-tighter text-[#ffd700]">
                    HUMSAFAR
                  </div>
                  <p className="text-[#ffd700] font-bold tracking-[0.5em] uppercase">
                    Established 2026
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="py-12 px-6 border-t border-white/5 text-center">
        <div className="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-8">
          <div className="text-xl font-bold tracking-widest text-[#ffd700]">
            HUMSAFAR
          </div>
          <div className="text-white/40 text-sm">
            © 2026 Humsafar Lifestyle Brand. All rights reserved.
          </div>
          <div className="flex gap-6 text-white/60 text-sm font-medium">
            <a href="#" className="hover:text-white">
              Privacy Policy
            </a>
            <a href="#" className="hover:text-white">
              Terms of Service
            </a>
          </div>
        </div>
      </footer>

      <style jsx global>{`
        @keyframes bounce {
          0%, 100% {
            transform: translate(-50%, 0);
          }
          50% {
            transform: translate(-50%, -20px);
          }
        }
        .bounce-animation {
          animation: bounce 2s infinite ease-in-out;
        }
      `}</style>
    </div>
  );
};

export default HumsafarLandingPage;
