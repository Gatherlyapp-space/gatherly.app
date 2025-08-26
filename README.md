# Gatherly — BusinessPlan.md

> **Kurzfassung:** Gatherly ist die schlanke Event-Plattform, die **private & öffentliche Events** endlich in **einer App** bündelt: Einladungen, Teilnehmer, Chat/Kommentare, **gemeinsame Fotoalben**, Suche (Events/Freunde/Gruppen/Veranstalter), **„Nearby“-Impulse** (à la „Beer-with-me“), **Business-Promo & Ticket-Links** – alles an einem Ort, ohne Tool-Chaos.

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
- [Produkt & Architektur](#produkt--architektur)
- [Datenmodell (vereinfacht)](#datenmodell-vereinfacht)
- [Sicherheit, Datenschutz, Moderation](#sicherheit-datenschutz-moderation)
- [Monetarisierung](#monetarisierung)
- [Go-to-Market](#go-to-market)
- [KPIs & Metriken](#kpis--metriken)
- [Roadmap (0–6 Monate)](#roadmap-0–6-monate)
- [Wettbewerb & Differenzierung](#wettbewerb--differenzierung)
- [Risiken & Blindspots](#risiken--blindspots)
- [Team](#team)
- [Funding & Einsatzplanung](#funding--einsatzplanung)
- [Anhänge / Assets](#anhänge--assets)
- [Lizenz & Kontakt](#lizenz--kontakt)

---

## Executive Summary
**Gatherly** löst das Alltagsproblem, Events über **viele Apps & Kanäle** (WhatsApp-Gruppen, Facebook-Events, Eventbrite, E-Mails, Cloud-Ordner) zu zersplittern.  
Wir bündeln Planung, Einladung, Abstimmung, **Foto-Sharing** und **Business-Promotion** in **einer** App – **privat gratis**, **kommerziell** über **Self-Serve-Promo & Ticket-Links** monetarisiert.

- **Privat:** Geburtstage, Grillen, Vereins-/Schul-Events, Nachbarschaft, Gemeinde.  
- **Öffentlich/Business:** Veranstalter, Städte, Firmen, Vereine – mit Promo-Tools, Sales-Links und Besucherstatistiken.  
- **USP:** **Ein App-Hub** für *alle* Events inkl. **„Nearby“-Impulse** (z. B. „Ich bin im Biergarten – wer kommt?“) + **QR-Foto-Uploads ohne Konto** (Hochzeitsmodus & Co.).

---

## Vision & Mission
**Vision:**  
Menschen **einfach** und **spontan** zusammenbringen – ohne Plattform-Hürden, ohne Info-Chaos. Gatherly wird der **Standard-Kalender** für gemeinsame Erlebnisse: privat, lokal, öffentlich & professionell – **alles in einer App**.

**Mission:**  
Wir konsolidieren verstreute Interaktionen – Einladungen, Zusagen, To-Dos, **Fotos** – und geben **Privatpersonen, Communities & Veranstaltern** ein **einheitliches Werkzeug**:  
- **Privat:** Ein Klick, und deine Leute wissen Bescheid, stimmen sich ab und teilen Fotos – **ohne** Toolsalat.  
- **Öffentlich/Business:** Reichweite, **Promo**, Ticket-Links & **Analytics** – operativ aus *einem* Dashboard.  
- **„Nearby“-Impulsfähigkeit:** spontane, lokale Treffen auslösen (z. B. „Beer-with-me“-Style).  
- **QR-Foto-Upload ohne Konto:** Gäste laden per QR Fotos für ein Event hoch – **ohne** Konto/Cloud-Hürden.

---

## Problem & Warum jetzt
- **Zerstreute Tools:** WhatsApp, Facebook, Eventbrite, Telegram, Cloud-Links – Informationen gehen unter, Bilder sind verteilt, Zusagen unklar.  
- **Privat vs. öffentlich:** Es gibt gute Tools für **öffentliche** Events **oder** gute Chats für **private** Treffen – kaum etwas vereint beides.  
- **Fotosharing-Pain:** Gäste wollen **ohne Konto** Fotos teilen (z. B. Hochzeit) – bestehende Lösungen zwingen zu Accounts/Clouds.  
- **Spontanität fehlt:** Ad-hoc-„Ich bin hier – kommt vorbei“-Momente sind in klassischen Event-Systemen umständlich.

**Zeitfenster:** Social- & Messaging-Overload → starker Bedarf für **„one hub“** und **„nearby contexts“**.

---

## Lösung & Produktversprechen
- **Ein Hub** für **private & öffentliche** Events inkl. **Foto-Album** & **Kommentare**.  
- **„Nearby“-Impulse:** simple, opt-in Status-Posts („Bin im Biergarten, bock?“), die direkt zu Micro-Events werden.  
- **QR-Foto-Upload ohne Konto:** Gäste laden per QR in das Event-Album hoch.  
- **Business-Suite:** Promo, Ticket-Links, QR-Codes, Besucherzahlen, Umsatz – **self-serve**.

---

## Zielgruppen
- **Privatpersonen**: Freunde, Familien, Nachbarschaft.  
- **Communities & Institutionen**: Vereine, Schulen, Gemeinden, Hochschulgruppen.  
- **Commercial/Business**: Veranstalter, Städte, Locations, Firmen-Events, Gastro, Kultur.

> **MVP-Fokus:** _TBD_ (z. B. „Privat + lokale Communities“ oder „Vereine/Schulen first“)

---

## Kernfunktionen (Feature Set)
### Auth & Profile
- E-Mail/Passwort, Social Logins (Google/Apple/Facebook), „Passwort vergessen“, Onboarding, Profil (Name, Bild, User-Typ **Privat/Commercial**), Edit.

### Homepage
- Willkommens-Text, **Event-Feed (privat/öffentlich)**, **Quick-Filter** (Datum, Entfernung, Kategorie), **Create-Event**, **Dark/Light-Mode**, **Search-Bar** (Name, Ort, Zeitraum, Kategorie, Freunde, Gruppen, Veranstalter).

### Events
- **Events-Übersicht:** Liste/Grid, Kategorien, Suche, Sortierung, Favoriten.  
- **Event-Detail:** Titelbild, Titel, Datum, Ort (Map), Beschreibung, Host-Info, Teilnehmer-Counter, **CTA** (Beitreten/Tickets), **Fotos**, Kommentare/optional Chat, **Share**.  
- **Create Event:** Titelbild, Datum/Uhrzeit, Ort + Map-Picker, Kategorie, Beschreibung, **Private/Public**, **Invite** (Kontakt/Name/Nummer), Uploads.  
- **My Events:** Eigene Events verwalten (Status public/private, Bearbeiten, Löschen, Teilnehmer, Link teilen).  
- **„Nearby“-Impulse:** spontane, sichtbare Mini-Posts im Umfeld (opt-in), die zu Events eskalieren können.

### Photos
- Event-Zuordnung, Kamera/Galerie, **Upload-Button**, **Progress**, **Success/Error**, Galerie.  
- **QR-Upload ohne Konto** (Guest Mode) für Hochzeiten, Vereinsfeste, Schul-Events.

### Business Dashboard
- **Event-Übersicht** (Status, Edit, Toggle public/private, Create).  
- **Promote**: Event wählen, Werbetext, Bild, Zielregion, **Push-Notification**, Start.  
- **Ticketing & Sales**: Sales-Links, QR-Codes, Teilen, **Statistiken** (Klicks, Conversions, Umsatz), **Disable**.

### Settings
- Dark/Light, Sprache, Benachrichtigungen, Datenschutz/Impressum, Logout.

---

## Einzigartige Use-Cases
1. **One-Hub für privat & öffentlich**: Ein Feed, getrennt filterbar – kein App-Hopping.  
2. **„Nearby“-Impulse** (Beer-with-me-Style): spontane, lokale „Ich bin hier“-Posts → Micro-Events.  
3. **QR-Foto-Upload ohne Konto**: Gäste geben Bilder direkt ins Event-Album – keine Cloud-Hürden.  
4. **„Bring-Mit“-Listen** im Event: wer bringt was, automatisch konsolidiert.  
5. **Hyperlokale Sichtbarkeit**: nur Freunde / Freunde-von-Freunden / Umkreis-X km.  
6. **Event-Duplikation**: Stammtische/Proben in 1 Klick kopieren.  
7. **Self-serve Promo & Tickets** im Business Dashboard.  
8. **Teilnehmer-Live-Status** (opt-in): „Ist schon vor Ort“.  
9. **Community-Feeds** (Schule/Verein/Gemeinde): zentrale, abonnierbare Event-Übersicht.  
10. **Gemeinsames Foto-Archiv** für jedes Event – privat zugänglich, public differenziert.

---

## High-Level User Journey
1) **Onboarding/Sign-Up** → Social/E-Mail, Profil anlegen.  
2) **Homepage** → Nearby/Upcoming sehen, filtern, suchen.  
3) **Event entdecken** → Karte/Detail, beitreten/ignorieren, Favorit.  
4) **Event planen** → Create, Freunde einladen, Bring-Mit, Kommentare.  
5) **Während des Events** → Live-Kommentare, Foto-Uploads, ggf. Live-Status.  
6) **Nach dem Event** → Gemeinsames Foto-Archiv, Rückblick, Duplizieren.  
7) **Business** → Promo starten, Sales-Links teilen, Analytics checken.

---

## Produkt & Architektur
- **Frontend:** Flutter/FlutterFlow (Mobile + Web)  
- **Backend/DB:** Supabase (Postgres, Auth, Row-Level-Security, Storage)  
- **Storage:** Supabase Storage (Fotos), CDN  
- **Server-Logik:** Supabase Edge Functions (Webhooks für Promo/Analytics)  
- **CI/CD:** GitHub + FlutterFlow Deploy  
- **Domains:** `gatherlyapp.space` (Web), später Custom Domains für Business

---

## Datenmodell (vereinfacht)
**users**  
- id (uuid, PK) — = Auth UID  
- email (text), user_type (enum: private|business), name, avatar_url, created_at

**events**  
- id (uuid, PK), user_id (FK→users)  
- title, description, category, location, lat, lng  
- start_at, end_at, is_public (bool), max_participants  
- created_at

**photos**  
- id (uuid, PK), event_id (FK→events), user_id (nullable für Guest-Uploads)  
- url, uploaded_at

**groups** *(Phase 2)*  
- id, name, description, owner_id

---

## Sicherheit, Datenschutz, Moderation
- **DSGVO-konform:** Opt-ins (Standort, Notifications), DPA mit Supabase, Datenminimierung.  
- **RLS:** strikte Zugriffspolicies.  
- **UGC Moderation:** Melden/Entfernen von Bildern/Beiträgen, Sperrlogik.  
- **Rechte an Fotos:** Einwilligung im Upload-Flow, private Events default „nicht öffentlich“.

---

## Monetarisierung
- **Privat**: kostenlos.  
- **Business/Commercial**:
  - **Promo/Ads** pro Event (Budget/CPC/CPM, Geo-Targeting)  
  - **Ticket-Sales** via Sales-Link (Rev-Share)  
  - **Affiliate-Integrationen** (Eventplattformen, z. B. Weiterleitung/Tracking)  
  - **Pro/Premium** (Phase 2): Branding, Custom Domains, Team-Seats, API.

---

## Go-to-Market
1. **MVP (Pilotregion)**: Lokale Vereine, Schulen, Gemeinden, Coworkings, Unis.  
2. **Community-Seeding**: Ambassadors (Vereins-/Klassensprecher), QR-Flyer.  
3. **Business-Outreach**: Städte/Veranstalter, Self-Serve Promo.  
4. **Partner**: Locations, Caterer, lokale Medien.  
5. **Content**: „Nearby Meetup Nights“, Fotowettbewerbe (Event-Galerien).

---

## KPIs & Metriken
- **Acquisition:** Registrierungen, Social-Login-Quote.  
- **Activation:** Event erstellt, erstes Event beigetreten, erstes Foto hochgeladen.  
- **Engagement:** Kommentare/Event, Uploads/Event, Bring-Mit-Nutzung.  
- **Virality:** Shares/Invites, QR-Uploads (Guest).  
- **Retention:** Wiederkehrende Nutzer, duplizierte Events.  
- **Monetization:** Promo-Ausgaben, Ticket-Umsatz, ARPU (Business).

---

## Roadmap (0–6 Monate)

**Monat 0–1 — Fundament (MVP Kern)**  
- Auth (E-Mail + Social), Profile/Settings  
- Events: Create, List (Nearby/Public + My Events), Detail, Join/Favorite  
- Fotos: Upload, Galerie, **QR-Guest-Upload (Basis)**  
- Kommentare, „Bring-Mit“ (simple checklist)  
- RLS/Policies, Logging, Basis-Analytics  
- Erste Community-Piloten (Verein/Schule)

**Monat 2–3 — UX & Feature-Vertiefung**  
- Suche/Filter (Name/Ort/Zeitraum/Kategorie/Freunde/Gruppen/Veranstalter)  
- „Nearby“-Impulse (opt-in Statusposts → Micro-Event)  
- Photo-Moderation, einfache Meldelogik  
- Event-Duplikation, ICS-Export  
- Web-Landing + Onboarding-Flows

**Monat 4–5 — Business Suite v1**  
- Business Dashboard (Event-Übersicht, Status, Create)  
- **Promote** (Geo, Text, Bild, Push), Sales-Links, QR-Codes  
- Besucher/Click-Stats, Einnahmen-Übersicht  
- Early Adopter Programm (10–20 Veranstalter)

**Monat 6 — Skalierungsphase**  
- Performance/Costs, Caching/Bild-Pipeline  
- Growth-Loops (Referral), Community-Features v1  
- Evaluierung: **Funding** für Team-Erweiterung (App-Dev, Growth)

---

## Wettbewerb & Differenzierung
**WhatsApp/Telegram**  
- _Stark:_ Reichweite, Einfachheit.  
- _Schwach:_ **keine strukturierte Event-Übersicht**, Infos/Fotos gehen im Chat unter.  
- _Gatherly-Vorteil:_ Einladungen, Zusagen, **Foto-Album & Kommentare** direkt **am Event**.

**Facebook Events**  
- _Stark:_ Reichweite (öffentlich).  
- _Schwach:_ Nicht jeder nutzt FB, **Privatsphäre** & UX, verstreute Gruppen/Seiten.  
- _Gatherly-Vorteil:_ **Privat & öffentlich** in einer App, **DSGVO-freundlicher**, fokussierte UX.

**Meetup**  
- _Stark:_ Community-Meetups, Nischen.  
- _Schwach:_ weniger für Privat/Ad-hoc, Hürde für Micro-Events.  
- _Gatherly-Vorteil:_ **„Nearby“-Impulse**, Micro-Events, **Foto-Flows**, **QR-Guest-Upload**.

**Eventbrite**  
- _Stark:_ Tickets/Payments.  
- _Schwach:_ Fokus **Business öffentlich**, **kein** Privat-Hub, kein Foto/Chat.  
- _Gatherly-Vorteil:_ **Privat + Business** integriert, **Promo & Sales** light, Community-Feed.

**„QR-Foto“-Tools (Hochzeit)**  
- _Stark:_ QR-Upload ohne Konto.  
- _Schwach:_ isolierte Funktion, kein Event-Ökosystem.  
- _Gatherly-Vorteil:_ **QR-Upload** als Teil einer **vollständigen Event-App** (Planen, Chat, Fotos, Business).

---

## Risiken & Blindspots
- **Ad-hoc-Spontanität**: „Nearby“-Feature muss verantwortungsvoll (Opt-in, Privatsphäre) und **nützlich** sein.  
- **UGC & Moderation**: Bild-Moderation, Abuse-Prevention (Reports, Rate Limits).  
- **Datenschutz**: DSGVO-konforme Einwilligungen (Fotos, Standort), DPA.  
- **Adoption**: Netzwerkeffekte vs. „alle sind schon in WhatsApp“.  
- **Business-Wert**: Promo & Sales müssen **wirklich** ROI bringen (Analytics-Qualität!).  

---

## Team
- **Jesse Barron** — Gründer, Produkt (Idee & Drive)  
- **Johannes Aragon** — Co-Founder, Produkt/Partnerships  
- **Sebastian Anders** — Tech & Design

> Rollen & Verantwortlichkeiten werden im nächsten Sprint formalisiert (Product, Eng, Growth, Ops).

---

## Funding & Einsatzplanung
**Status:** Bootstrapped – MVP mit FlutterFlow + Supabase.  
**Offen für Investment** (Seed/Pre-Seed), um zu beschleunigen:
- Einstellung 1–2 App-Entwickler (Flutter)  
- Growth/Community-Pilotprogramme  
- Marketing (lokal, Vereine/Schulen, Städte)

**Mittelverwendung (Beispiel):**  
- 50% Produkt/Engineering  
- 30% Go-to-Market/Partnerships  
- 20% Infrastruktur/Legal

---

## Anhänge / Assets
- **UI-Mocks (MVP-Stil):** Login, Sign-Up, Home, Profile, Edit Profile, Events (List/Detail), Create Event, My Events, Photos, Settings, Business Dashboard.  
- **Tech-Stack:** Flutter/FlutterFlow, Supabase (Auth, DB, Storage, RLS), Edge Functions, CDN.  
- **Domain:** `gatherlyapp.space`  
- **Repo:** `gatherly.app` (GitHub)

---

## Lizenz & Kontakt
- **Lizenz:** _TBD_ (z. B. Proprietary intern oder MIT für Teile).  
- **Kontakt:**  
  - Produkt: **Jesse Barron**  
  - E-Mail (Beispiel): `jesse@gatherly.com`  
  - Discord (Projektserver): _TBD_  
  - Website: _in Arbeit_
