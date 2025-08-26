# Gatherly — BusinessPlan.md

> **Gatherly ist die Event-Plattform, die private und öffentliche Events endlich in einer App bündelt:**  
Einladungen, Teilnehmer, Kommentare/To-Dos, **gemeinsame Fotoalben (inkl. QR-Gast-Upload ohne Konto)**, Suche (Events/Freunde/Gruppen/Veranstalter), **„Nearby“-Impulse** à la „Ich bin hier – wer kommt?“, **Business-Promo & Ticket-Links** – alles an einem Ort, ohne Tool-Chaos.

---

## Inhaltsverzeichnis
- [Executive Summary](#executive-summary)  
- [Vision & Mission](#vision--mission)  
- [Problem & Warum jetzt](#problem--warum-jetzt)  
- [Lösung & Produktversprechen](#lösung--produktversprechen)  
- [Zielgruppen](#zielgruppen)  
- [Kernfunktionen (Feature Set)](#kernfunktionen-feature-set)  
- [Einzigartige Use-Cases](#einzigartige-use-cases)  
- [High-Level User Journey](#high-level-user-journey)  
- [Design & UX als USP](#design--ux-als-usp)  
- [Produkt & Architektur](#produkt--architektur)  
- [Datenmodell (vereinfacht)](#datenmodell-vereinfacht)  
- [Sicherheit, Datenschutz, Moderation](#sicherheit-datenschutz-moderation)  
- [Monetarisierung](#monetarisierung)  
- [Go-to-Market](#go-to-market)  
- [KPIs & Metriken](#kpis--metriken)  
- [Roadmap (0–6 Monate)](#roadmap-0-6-monate)  
- [Wettbewerb & Differenzierung](#wettbewerb--differenzierung)  
- [Risiken & Blindspots](#risiken--blindspots)  
- [Team](#team)  
- [Funding & Einsatzplanung](#funding--einsatzplanung)  
- [Anhänge / Assets](#anhänge--assets)  
- [Lizenz & Kontakt](#lizenz--kontakt)

---

## Executive Summary
**Gatherly** löst das Alltagsproblem, Events über viele Kanäle (WhatsApp, Facebook, Eventbrite, Telegram, E-Mails, Cloud-Ordner) zu organisieren.  

Wir bündeln alles in **einer App**: Planung, Einladungen, Foto-Sharing, Event-Kommentare, spontane Treffen („Nearby“), und für Business-Kunden ein Dashboard mit **Promo, Ticket-Links und Analytics**.  

- **Privatnutzer:** Geburtstage, Grillen, Vereins- und Schul-Events.  
- **Communities:** Schulen, Gemeinden, Nachbarschaften.  
- **Business:** Städte, Veranstalter, Firmen.  
- **USP:** Kombination von *privaten* und *öffentlichen* Events in **einer Plattform**, inkl. **QR-Foto-Uploads ohne Konto** und **Nearby-Microevents**.

---

## Vision & Mission

**Vision:**  
Gatherly wird der **Standard-Kalender für gemeinsame Erlebnisse**: privat, lokal, öffentlich & professionell – **alles in einer App**.  

**Mission:**  
- **Privat:** Ein Klick → Einladung, Zusagen, Fotos und Kommentare direkt am Event.  
- **Öffentlich/Business:** Reichweite, Promotion, Ticket-Links & Analytics – aus einem Dashboard.  
- **Spontanität:** Nearby-Impulse à la *Beer With Me* machen Treffen einfach & schnell.  
- **Zugänglichkeit:** QR-Foto-Upload ohne Konto für Gäste (inspiriert von *weddies*).  
- **Low Friction Groups:** Per Link/QR/SMS beitreten (inspiriert von *GroupMe*).  

⚠️ **TBD:** Framing – wird Gatherly als **Event-App mit Social Layer** positioniert oder als **Social-App mit Event-Kern**?

---

## Problem & Warum jetzt
- **Fragmentierte Tools:** Chats, Social, Ticketing, Foto-Clouds – alles verstreut.  
- **Privat vs. öffentlich:** Keine App kombiniert beides sinnvoll.  
- **Fotosharing:** Gäste wollen Fotos hochladen **ohne Account**.  (Wedding-Mode etc.)
- **Spontanität fehlt:** klassische Event-Systeme sind schwerfällig, nicht für spontane Treffen.  

---

## Lösung & Produktversprechen
- **Ein Hub** für alle Events – privat und öffentlich.  
- **Trojan Horse-Feature (⚠️ TBD):** QR-Foto-Upload oder Nearby-Impulse als virales Einstiegs-Feature.  
- **Business-Suite:** Self-Serve Promotion, Ticketing, Besucher-Analytics.  

---

## Zielgruppen
- **Privatpersonen:** Freunde, Familien, Nachbarschaften.  
- **Communities & Institutionen:** Vereine, Schulen, Gemeinden, Unis.  
- **Commercial/Business:** Veranstalter, Städte, Locations, Firmen-Events.  

⚠️ **TBD:** MVP-Fokus – Privat/Communities zuerst oder sofort Hybrid?

---

## Kernfunktionen (Feature Set)

### Auth & Profile
- E-Mail/Passwort, Social Logins (Google, Apple, Facebook)  
- Passwort vergessen  
- Profil mit Name, Bild, User-Typ (Privat/Commercial)  
- Edit Profile  

### Homepage
- Willkommens-Text  
- Event-Feed (privat & öffentlich)  
- Quick-Filter (Datum, Entfernung, Kategorie)  
- Create Event Button  
- Dark/Light-Mode Toggle  
- Search Bar (Name, Ort, Zeitraum, Kategorie, Freunde, Gruppen, Veranstalter)  

### Events
- **Übersicht:** Liste/Grid, Kategorien, Suche, Favoriten  
- **Detail:** Titelbild, Titel, Datum, Ort (Map), Beschreibung, Host-Info, Teilnehmer-Counter, CTA (Beitreten/Tickets), Fotos, Kommentare, optional Chat, Share-Button  
- **Create Event:** Titelbild, Datum/Uhrzeit, Ort + Map-Picker, Kategorie, Beschreibung, Public/Private Toggle, Invite (Kontakt/Name/Nummer), Save Button  
- **My Events:** Übersicht, Status (public/private), Bearbeiten/Löschen, Teilnehmer, Link teilen  
- **Nearby-Impulse:** spontane Kurz-Posts („Ich bin hier“), sichtbar für Freunde oder Umkreis  

### Photos
- Event-Zuordnung  
- Kamera/Galerie Zugriff  
- Upload-Button  
- Upload-Progress-Bar  
- Success/Error Feedback  
- Galerie aller Fotos  
- QR-Gast-Upload ohne Konto  

### Business Dashboard
- Event-Übersicht (Status, Edit, Toggle public/private, Create Event)  
- Promote-Panel: Event wählen, Werbetext, Bild, Zielregion, Push-Notification, Start  
- Ticketing & Sales: Sales-Links, QR-Codes, Teilen, Statistiken (Klicks, Umsatz), Einnahmen  
- Event Disable Option  

---

## Einzigartige Use-Cases
1. One-Hub für privat & öffentlich  
2. Nearby-Impulse (Beer With Me)  
3. QR-Foto-Upload ohne Konto (weddies)  
4. Low-Friction Group Join (GroupMe)  
5. Bring-Mit-Listen  
6. Community-Feeds (Schulen/Vereine)  
7. Event-Duplikation  
8. Self-Serve Promo & Ticketing  
9. Teilnehmer-Live-Status (opt-in)  
10. Gemeinsame Foto-Archive pro Event  

---

## High-Level User Journey
### Private Events  
Sign Up → Create Event → Invite Friends → Kommentare/Bring-Mit → Fotos teilen → (optional: Bill Splitting ⚠️ TBD)  

### Public Events  
Login → Browse Events → Filter → Detail → Join → Notifications  

### Business Events  
Login → Dashboard → Create/Promote Event → Sales Links → Analytics → Revenue  

---

## Design & UX als USP
- **Design als Differenzierung:** Nutzer erwarten modernes, minimalistisches UI (Inspiration: mobbin.com, 60fps.design).  
- **UX-Strategie:** Low Friction, klare Flows, keine Überladung im MVP.  
- **Testing & Prototyping:** Früh testen, Feature-Creep vermeiden.  

⚠️ **TBD:** eigener Design Sprint Workshop?

---

## Produkt & Architektur
- **Frontend:** ⚠️ **TBD:**
- **Backend/DB:** ⚠️ **TBD:** 
- **Storage: ** ⚠️ **TBD:**
- **Server-Logik: ⚠️ **TBD:**
- **CI/CD:** GitHub or ⚠️ **TBD:**
- **Domain:** `gatherlyapp.space`  

---

## Datenmodell (vereinfacht)
**users**: id, email, user_type (private|business), name, avatar_url, created_at  
**events**: id, user_id, title, description, category, location, lat, lng, start_at, end_at, is_public, max_participants, created_at  
**photos**: id, event_id, user_id (nullable für Guest-Uploads), url, uploaded_at  
**groups** (Phase 2): id, name, description, owner_id  

---

## Sicherheit, Datenschutz, Moderation
- DSGVO-konform: Opt-ins (Standort, Notifications), DPA mit Supabase  
- Row-Level-Security Policies  
- Moderation: Melden/Entfernen von Inhalten, Sperren von Usern  
- Foto-Rechte: Einwilligung beim Upload  

---

## Monetarisierung
- **Privatnutzer:** kostenlos  
- **Business/Commercial:**  
  - Promo/Ads pro Event (Geo-Targeting, CPC/CPM)  
  - Ticket-Sales (Rev-Share)  
  - Affiliate-Integrationen  
  - Pro/Premium (⚠️ TBD – Custom Branding, Domains, Teams)  

⚠️ **Offen:** Preismodell (Flat Fee? CPC? Subscription?)  

---

## Go-to-Market
1. MVP Pilot (Vereine, Schulen, Gemeinden)  
2. Trojan Horse Feature (⚠️ TBD: QR-Upload oder Nearby)  
3. Business-Onboarding (Veranstalter, Städte)  

---

## KPIs & Metriken
- Acquisition: Registrierungen, Social-Login-Quote  
- Activation: Erstes Event, erste Teilnahme, erstes Foto  
- Engagement: Kommentare/Event, Uploads/Event  
- Virality: Shares, QR-Uploads (Guest)  
- Retention: Wiederkehrende Nutzer, Event-Duplikationen  
- Monetization: Promo-Ausgaben, Ticket-Umsatz  

---

## Roadmap (0–6 Monate)
- **Monat 0–1:** Auth, Profile, Events (Create/List/Detail), Fotos (inkl. QR-Upload), Nearby-Basis, erste Community-Tests  
- **Monat 2–3:** Suche/Filter, Event-Duplikation, Moderation, „Nearby“-Impulse erweitern  
- **Monat 4–5:** Business Dashboard v1 (Promo, Sales-Links, QR-Codes, Analytics)  
- **Monat 6:** Growth Loops, Community-Features, Funding-Entscheidung  

---

## Wettbewerb & Differenzierung
- **Beer With Me:** spontane Check-ins, keine Event-Suite  
- **weddies:** QR-Foto-Upload ohne Konto, kein Event-Kontext  
- **GroupMe:** Chat, Low-Friction Join, aber kein Event-Hub  
- **FB Events/Meetup/Eventbrite:** Reichweite & Ticketing, aber kein Privat+Business in einer App  

---

## Risiken & Blindspots
- Adoption: Wechselhürde von WhatsApp hoch  
- Datenschutz: Standort & Fotos sensibel  
- Business Value: Promo muss ROI liefern  

---

## Team
- **Jesse Barron** — 
- **Johannes Aragon** — 
- **Sebastian Anders** — 

---

## Funding & Einsatzplanung
- Offen für Seed/Pre-Seed Funding  

⚠️ **TBD:** Kapitalbedarf für 6–12 Monate (z. B. 250–500k €)  

---

## Anhänge / Assets
- UI-Mocks (MVP-Stil)  
- Präsentation (Sebastian Anders)  
- Gatherly Domains & GitHub Repo  

---

## Lizenz & Kontakt
- Lizenz: ⚠️ TBD (Proprietär oder MIT für Teile)  
- Kontakt:  
  - Discord: ⚠️ TBD  
  - Website: ⚠️ TBD
