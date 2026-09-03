---
name: "abje-tarot"
title: "ABJE Tarot"
type: "react"
---

import React, { useState } from "react";

const ADMIN_PASSWORD = "Tass6gny";
const ABJE_PASSWORD = "0309";

function App() {
  const [user, setUser] = useState(null);

  if (!user) {
    return (
      <div style={{ padding: "20px", textAlign: "center", fontFamily: "sans-serif", background: "#0f172a", color: "#f8fafc", minHeight: "100vh", display: "flex", flexDirection: "column", justifyContent: "center" }}>
        <h1>🃏 ABJE Tarot</h1>
        <div style={{ margin: "20px" }}>
          <button onClick={() => setUser("admin")} style={{ padding: "12px 24px", background: "#f59e0b", border: "none", borderRadius: "8px", color: "white", fontWeight: "bold", cursor: "pointer", margin: "5px" }}>Connexion Admin</button>
          <button onClick={() => setUser("abje")} style={{ padding: "12px 24px", background: "#10b981", border: "none", borderRadius: "8px", color: "white", fontWeight: "bold", cursor: "pointer", margin: "5px" }}>Connexion ABJE</button>
        </div>
        <p style={{ fontSize: "14px", color: "#94a3b8" }}>Mots de passe : admin/{ADMIN_PASSWORD}   abje/{ABJE_PASSWORD}</p>
      </div>
    );
  }

  return (
    <div style={{ padding: "20px", fontFamily: "sans-serif", background: "#0f172a", color: "#f8fafc", minHeight: "100vh" }}>
      <h1>Bienvenue, {user} !</h1>
      <p>Votre application ABJE Tarot est prête.</p>
      <button onClick={() => setUser(null)} style={{ padding: "10px 20px", background: "#ef4444", border: "none", borderRadius: "8px", color: "white", cursor: "pointer" }}>Déconnexion</button>
    </div>
  );
}

export default App;
