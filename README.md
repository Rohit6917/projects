import React from "react";
import { BrowserRouter as Router, Route, Routes } from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Projects from "./pages/Projects";
import Resume from "./pages/Resume";
import Contact from "./pages/Contact";
import Navbar from "./components/Navbar";
import Footer from "./components/Footer";
import "./styles/global.css";

function App() {
  return (
    <Router>
      <Navbar />
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/projects" element={<Projects />} />
        <Route path="/resume" element={<Resume />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
      <Footer />
    </Router>
  );
}

export default App;

// Navbar Component
import { Link } from "react-router-dom";

const Navbar = () => (
  <nav className="bg-gray-900 text-white p-4 flex justify-between items-center">
    <h1 className="text-xl font-bold">Rohit Kumar Raj</h1>
    <div>
      <Link to="/" className="mx-2">Home</Link>
      <Link to="/about" className="mx-2">About</Link>
      <Link to="/projects" className="mx-2">Projects</Link>
      <Link to="/resume" className="mx-2">Resume</Link>
      <Link to="/contact" className="mx-2">Contact</Link>
    </div>
  </nav>
);

export default Navbar;

// Footer Component
const Footer = () => (
  <footer className="bg-gray-800 text-white text-center p-3 mt-4">
    <p>&copy; 2025 Rohit Kumar Raj. All Rights Reserved.</p>
  </footer>
);

export default Footer;
