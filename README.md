# 🚀 Ibrahim Ankidine — Portfolio Flask

Portfolio professionnel avec panneau d'administration, construit avec **Python Flask**.

---

## 📁 Structure du projet

```
portfolio_flask/
│
├── app.py                  ← Application Flask principale
├── init_db.py              ← Script d'initialisation DB
├── requirements.txt        ← Dépendances Python
├── Procfile                ← Pour déploiement Render/Heroku
│
├── templates/
│   ├── public/
│   │   ├── base.html       ← Layout public
│   │   └── index.html      ← Page principale (portfolio)
│   └── admin/
│       ├── base.html       ← Layout admin
│       ├── login.html      ← Connexion admin
│       ├── dashboard.html  ← Tableau de bord
│       ├── profile.html    ← Gestion du profil
│       ├── projects.html   ← Liste des projets
│       ├── project_form.html
│       ├── experiences.html
│       ├── experience_form.html
│       ├── skills.html
│       ├── skill_form.html
│       ├── education.html
│       ├── education_form.html
│       ├── messages.html   ← Messages de contact
│       └── stats.html      ← Statistiques de visites
│
├── static/
│   ├── css/
│   │   ├── public.css      ← Styles portfolio public
│   │   └── admin.css       ← Styles panneau admin
│   ├── js/
│   │   ├── public.js       ← Animations & interactions
│   │   └── admin.js        ← Logique admin
│   ├── images/
│   │   └── profile.png     ← Photo de profil
│   └── uploads/            ← Fichiers uploadés (photos, CV)
│
└── instance/
    └── portfolio.db        ← Base de données SQLite (générée)
```

---

## ⚙️ Installation locale

### 1. Prérequis
- Python 3.8+
- pip

### 2. Cloner / extraire le projet
```bash
cd portfolio_flask
```

### 3. Créer un environnement virtuel
```bash
python -m venv venv
# Windows :
venv\Scripts\activate
# Mac/Linux :
source venv/bin/activate
```

### 4. Installer les dépendances
```bash
pip install -r requirements.txt
```

### 5. Initialiser la base de données
```bash
python init_db.py
```

### 6. Lancer l'application
```bash
python app.py
```

➡️ Ouvrez : **http://localhost:5000**

---

## 🔐 Accès Admin

- URL : **http://localhost:5000/admin**
- Utilisateur : `admin`
- Mot de passe : `admin123`

> ⚠️ **Changez le mot de passe après la première connexion !**

---

## 🌐 Déploiement sur Render (gratuit)

### 1. Créer un compte sur [render.com](https://render.com)

### 2. Pousser le projet sur GitHub
```bash
git init
git add .
git commit -m "Portfolio Flask initial"
git remote add origin https://github.com/VOTRE_USERNAME/portfolio
git push -u origin main
```

### 3. Créer un nouveau Web Service sur Render
- **Build Command** : `pip install -r requirements.txt && python init_db.py`
- **Start Command** : `gunicorn app:app`
- **Environment** : Python 3

### 4. Variables d'environnement à configurer sur Render
```
SECRET_KEY = une-clé-secrète-longue-et-aléatoire
```

---

## 🎛️ Fonctionnalités Admin

| Section | Fonctionnalités |
|---------|----------------|
| **Dashboard** | KPIs, messages récents, pages visitées, actions rapides |
| **Profil** | Nom, titre, bio, photo, CV, réseaux sociaux, stats hero |
| **Projets** | CRUD complet (créer, lire, modifier, supprimer) |
| **Expériences** | CRUD avec points clés dynamiques |
| **Compétences** | CRUD par catégorie avec icônes FontAwesome |
| **Formation** | CRUD diplômes et établissements |
| **Messages** | Voir, marquer comme lu, répondre, supprimer |
| **Statistiques** | Graphique des visites, répartition par page |

---

## 🎨 Fonctionnalités Publiques

- ✅ Design UI/UX 2026 premium (Cormorant Garamond + Syne)
- ✅ Mode Clair / Sombre avec toggle animé
- ✅ Curseur personnalisé avec effet de lag
- ✅ Animations scroll reveal + stagger
- ✅ Typing effect rotatif
- ✅ Compteurs animés
- ✅ Tilt 3D sur les cartes projets
- ✅ Boutons magnétiques
- ✅ Téléchargement CV (3 points d'accès)
- ✅ Formulaire de contact (messages en base de données)
- ✅ Page loader
- ✅ Navigation sticky avec active link
- ✅ Responsive mobile complet

---

## 🛠️ Personnalisation

Toutes les données sont éditables depuis l'interface admin :
- Pas besoin de toucher au code
- Changement de photo en un clic
- Ajout/modification de projets en temps réel

---

*Développé par Ibrahim Ankidine · 2025*
