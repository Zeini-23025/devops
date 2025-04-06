🏆 **Nom de l'équipe** : 見つかりません

# Gestion des Revenus - Application Web

📌 **Objectif**

Cette application permet aux entreprises de gérer efficacement leurs revenus à travers une interface web moderne, intuitive et sécurisée.

📚 **Description du Projet**

L'application permet la création, la consultation, la modification et la suppression des enregistrements liés aux revenus. Elle intègre également des fonctions de calcul de taxes et de bonus, ainsi que des statistiques sur les revenus.

🚀 **Fonctionnalités**

- **Gestion des revenus** : Ajout, modification, suppression et consultation des entrées.
- **Recherche et filtrage** : Par catégorie, période, montant, etc.
- **Calculs automatiques** : Taxes, bonus, total net.
- **Interface utilisateur moderne** : Réactive et intuitive avec React.js.
- **API REST sécurisée** : Développée avec Django REST Framework.
- **Conteneurisation** : Docker & Docker Compose.

🐳 **Conteneurisation avec Docker**

L’application est conteneurisée via deux images distinctes : une pour le backend (Django) et une pour le frontend (React). Docker Compose permet de les orchestrer ensemble.

⚙️ **CI/CD avec GitHub Actions**

Un pipeline GitHub Actions est utilisé pour automatiser le build et le push des images Docker vers Docker Hub.

📂 **Livrables**

- ✅ Code source backend et frontend (dans le même dépôt).
- ✅ Dockerfile pour le frontend et le backend.
- ✅ Workflow GitHub Actions CI/CD.
- ✅ Images Docker publiées sur Docker Hub.

🔹 **Dépôt GitHub**

- 🔗 [Revenus App (Backend + Frontend)](https://github.com/Zeini-23025/GRI)

🐳 **Dépôts Docker Hub**

- 🐳 [Backend](https://hub.docker.com/repository/docker/zeini/gri-backend)
- 🐳 [Frontend](https://hub.docker.com/repository/docker/zeini/gri-frontend)

🚀 **Accéder à l'application**

- 🔹 **Backend** : 🌍 [api.revenus-app.com](#)
- 🔹 **Frontend** : 🌍 [www.revenus-app.com](#)

---

## ⚙️ Installation du projet

### 1. Cloner le dépôt

```bash
git clone https://github.com/Zeini-23025/GRI.git
cd GRI
```

---

### 2. Exécuter avec Docker Compose (recommandé)

```bash
docker-compose up --build
```

Cela démarre les deux services :

- 🛠 Backend accessible sur [http://localhost:8000](http://localhost:8000)
- 💻 Frontend accessible sur [http://localhost:3000](http://localhost:3000)

---

### 3. Exécuter manuellement chaque partie

#### 🐳 Backend

```bash
docker pull zeini/gri-backend
docker run -p 8000:8000 zeini/gri-backend
```

#### 🐳 Frontend

```bash
docker pull zeini/gri-frontend
docker run -p 3000:3000 zeini/gri-frontend
```

---

### 4. Exécution locale sans Docker (optionnel)

#### ✅ Backend (Django)

Sous Linux/macOS :

```bash
cd backend
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Sous Windows :

```bash
cd backend
python -m venv env
env\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Accessible via [http://localhost:8000](http://localhost:8000)

#### ✅ Frontend (React)

```bash
cd frontend
npm install
npm start
```

Accessible via [http://localhost:3000](http://localhost:3000)

---

## 📁 Structure du projet

```
revenus-app/
├── .github/              # Workflows CI/CD
├── backend/              # Django API
│   ├── Dockerfile
│   └── ...
├── frontend/             # React App
│   ├── Dockerfile
│   └── ...
├── docker-compose.yml
└── README.md
```

---

## 🧑‍💻 Équipe

Projet réalisé par l’équipe **見つかりません** dans le cadre du module *Projet Intégrateur*.

---


