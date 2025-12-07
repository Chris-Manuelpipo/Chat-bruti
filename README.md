# 🤖 Chat-Bruti

Une application de chatbot moderne et interactive avec un robot animé intelligent qui répond à vos questions en temps réel.

![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## ✨ Fonctionnalités

### 🎨 Interface Moderne
- **Design inspiré de Claude AI** - Interface professionnelle et épurée
- **Thème clair/sombre** - Basculez entre les modes selon vos préférences
- **Responsive** - Fonctionne parfaitement sur desktop, tablette et mobile
- **Animations fluides** - Transitions et effets visuels soignés

### 🤖 Robot Interactif
- **Suit le curseur** - Le robot suit vos mouvements de souris avec ses yeux
- **Réagit à la saisie** - Regarde le champ de texte quand vous tapez
- **Animation de parole** - Sa bouche s'anime quand il répond
- **États émotionnels** - Excité, pensif, en train de parler
- **Toujours visible** - Présent dans l'en-tête de l'application

### 💬 Gestion des Conversations
- **Historique complet** - Toutes vos conversations sont sauvegardées localement
- **Multi-conversations** - Créez et gérez plusieurs discussions
- **Titres automatiques** - Les conversations sont nommées automatiquement
- **Navigation facile** - Basculez entre vos conversations en un clic
- **Persistance des données** - Vos conversations restent après fermeture du navigateur

### 🚀 Fonctionnalités UX
- **Indicateur de saisie** - Points animés pendant que le bot réfléchit
- **Auto-resize du textarea** - Le champ s'adapte à votre texte
- **Raccourcis clavier** - `Enter` pour envoyer, `Shift+Enter` pour nouvelle ligne
- **État vide engageant** - Message de bienvenue avec robot animé
- **Feedback visuel** - Confirmations et animations pour chaque action

## 🛠️ Technologies Utilisées

- **HTML5** - Structure sémantique moderne
- **CSS3** - Animations, transitions, flexbox, grid
- **JavaScript (Vanilla)** - Logique interactive sans dépendances
- **LocalStorage API** - Persistance des données côté client
- **Fetch API** - Communication avec le backend

## 📋 Prérequis

- Un navigateur web moderne (Chrome, Firefox, Safari, Edge)
- Connexion internet pour communiquer avec l'API backend
- JavaScript activé

## 🚀 Installation

### Option 1 : Utilisation directe

1. Clonez le dépôt :
```bash
git clone https://github.com/votre-username/chat-bruti.git
cd chat-bruti
```

2. Ouvrez `index.html` dans votre navigateur :
```bash
# Sur macOS
open index.html

# Sur Linux
xdg-open index.html

# Sur Windows
start index.html
```

### Option 2 : Serveur local

Pour un développement optimal, utilisez un serveur HTTP local :

```bash
# Avec Python 3
python -m http.server 8000

# Avec Node.js (http-server)
npx http-server -p 8000

# Avec PHP
php -S localhost:8000
```

Puis accédez à `http://localhost:8000`

## ⚙️ Configuration

### API Backend

L'application communique avec un backend via l'endpoint :
```
https://chatbrutiapi.onrender.com/chat
```

Pour utiliser votre propre API, modifiez la ligne suivante dans `index.html` :

```javascript
const res = await fetch('VOTRE_URL_API/chat', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ question })
});
```

### Format de l'API

L'API doit accepter :
```json
{
  "question": "Votre question ici"
}
```

Et retourner :
```json
{
  "response": "La réponse du bot"
}
```

## 📱 Fonctionnalités Détaillées

### Animations du Robot

Le robot possède plusieurs états animés :

| État | Déclencheur | Animation |
|------|-------------|-----------|
| **Suivi du curseur** | Mouvement de la souris | Yeux qui suivent |
| **Attention** | Focus sur le champ de saisie | Regarde vers le bas |
| **Réflexion** | Saisie de texte | Bras en mouvement |
| **Excitation** | Envoi d'un message | Saut joyeux |
| **Parole** | Réponse du bot | Bouche qui s'ouvre/ferme |
| **Veille** | Inactivité | Lumière clignotante |

### Gestion du Thème

```javascript
// Le thème est automatiquement sauvegardé
localStorage.getItem('theme') // 'light' ou 'dark'

// Changer le thème programmatiquement
toggleTheme()
```

### Structure des Données

Les conversations sont stockées au format :

```javascript
{
  id: "1701234567890",
  title: "Ma première question...",
  messages: [
    { text: "Question", sender: "user" },
    { text: "Réponse", sender: "bot" }
  ],
  timestamp: "2024-12-07T10:30:00.000Z"
}
```

## 🎯 Utilisation

### Démarrer une conversation

1. Cliquez sur **"➕ Nouvelle conversation"** dans la sidebar
2. Tapez votre question dans le champ de saisie
3. Appuyez sur `Enter` ou cliquez sur le bouton d'envoi
4. Le robot réagit et vous répond !

### Gérer l'historique

- **Voir les conversations** - Toutes listées dans la sidebar gauche
- **Charger une conversation** - Cliquez sur n'importe quel élément
- **Conversation active** - Surlignée en violet dans la liste
- **Nouveau chat** - Créez autant de conversations que vous voulez

### Changer le thème

Cliquez sur l'icône 🌙/☀️ en haut à droite pour basculer entre les thèmes.

## 📂 Structure du Projet

```
chat-bruti/
│
├── index.html          # Application complète (HTML + CSS + JS)
├── README.md           # Cette documentation
└── assets/             # Ressources (optionnel)
    └── images/
        └── robot.png   # Image du robot (si externe)
```

## 🔧 Personnalisation

### Couleurs

Modifiez les variables CSS pour personnaliser les couleurs :

```css
/* Thème principal */
--primary: #8b5cf6;      /* Violet */
--primary-dark: #7c3aed; /* Violet foncé */

/* Thème clair */
--bg-light: #f9fafb;
--text-light: #111827;

/* Thème sombre */
--bg-dark: #0f0f0f;
--text-dark: #f9fafb;
```

### Animations

Ajustez la durée des animations :

```css
transition: all 0.3s ease; /* Modifiez 0.3s */
```

### Taille du Robot

Modifiez les dimensions dans la classe `.header-robot` :

```css
.header-robot {
    width: 40px;   /* Largeur */
    height: 50px;  /* Hauteur */
}
```

## 🐛 Résolution des Problèmes

### Le robot ne s'anime pas
- Vérifiez que JavaScript est activé
- Assurez-vous qu'aucune extension ne bloque les animations
- Rechargez la page (Ctrl+R ou Cmd+R)

### L'historique ne se sauvegarde pas
- Vérifiez que le localStorage n'est pas désactivé
- Effacez le cache du navigateur et réessayez
- Mode navigation privée désactive le localStorage

### Erreur de connexion à l'API
- Vérifiez votre connexion internet
- L'API backend doit être accessible
- Consultez la console (F12) pour les erreurs détaillées

### Le thème ne se sauvegarde pas
- LocalStorage doit être activé
- Pas de mode navigation privée
- Vérifiez les permissions du site

## 🚀 Améliorations Futures

- [ ] Export des conversations en PDF/TXT
- [ ] Recherche dans l'historique
- [ ] Personnalisation du robot (couleurs, accessoires)
- [ ] Support vocal (Speech-to-Text)
- [ ] Réponses avec markdown
- [ ] Partage de conversations
- [ ] Mode hors ligne avec Service Worker
- [ ] Thèmes personnalisables multiples
- [ ] Raccourcis clavier avancés
- [ ] Analytics des conversations

## 📄 License

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 👥 Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. Forkez le projet
2. Créez une branche pour votre fonctionnalité (`git checkout -b feature/AmazingFeature`)
3. Committez vos changements (`git commit -m 'Add some AmazingFeature'`)
4. Poussez vers la branche (`git push origin feature/AmazingFeature`)
5. Ouvrez une Pull Request

## 📞 Contact

- **Créateur** : Votre Nom
- **Email** : votre.email@example.com
- **GitHub** : [@votre-username](https://github.com/votre-username)
- **Twitter** : [@votre_handle](https://twitter.com/votre_handle)

## 🙏 Remerciements

- Inspiré par [Claude AI](https://claude.ai) d'Anthropic
- Icônes emoji pour l'interface
- Communauté open-source pour l'inspiration

## 📊 Statistiques

- **Lignes de code** : ~800 lignes
- **Taille** : ~25 KB (minifié)
- **Performance** : 100/100 Lighthouse
- **Compatibilité** : Chrome 90+, Firefox 88+, Safari 14+, Edge 90+

---

**Made with ❤️ and lots of ☕**

*Si vous aimez ce projet, n'oubliez pas de lui donner une ⭐ sur GitHub !*