# 📒 Mon carnet de bord

**Nom :KANE 

**Prénom :Abdoulaye Elimane Boubacar

**Adresse de mon site :** https://elimanekanee06.pythonanywhere.com

> Modifiez ce fichier directement sur GitHub (icône crayon ✏️) pour répondre aux questions de chaque exercice.
> Écrivez avec vos propres mots : une réponse courte et juste vaut mieux qu'un long copier-coller ! 🙂

---

## 🟢 Exercice 1 — Mon premier déploiement

1. Où se trouve physiquement le code qui fabrique votre page : sur votre ordinateur, sur GitHub ou sur PythonAnywhere ?

   > _Ma réponse :_ Il se trouve sur Pythonanywhere

2. Pourquoi votre voisin(e) peut-il voir votre site, alors que vous n'avez rien installé sur son ordinateur ?

   > _Ma réponse :_ Car le serveur PythonAnywhere possède une adresse accessible sur le Web.

---

## 🟢 Exercice 2 — Les URL et les routes

1. Dans l'URL `https://www.google.com/maps`, quel est le nom de domaine ? Quel est le chemin ?

   > _Ma réponse : Nom de domaine : [www.google.com] ; Chemin : /maps

2. Que veut dire le message *Not Found* ? Qui l'a envoyé : votre navigateur ou le serveur ?

   > _Ma réponse :_ Signification : La page ou le chemin demandé n'existe pas à cette adresse. Émetteur : C'est le serveur qui l'a envoyé.

3. Que se passe-t-il si deux fonctions portent le même nom dans `flask_app.py` ? (Indice : essayez, puis lisez l'Error log.)

   > _Ma réponse :_ L'application plante au démarrage

---

## 🔵 Exercice 3 — Le langage HTML

1. Quelle est la différence entre ce que le serveur **envoie** et ce que le navigateur **affiche** ?

   > _Ma réponse :_ Le serveur envoie : Du texte brut contenant du code source HTML et le navigateur affiche : Une page Web visuellement mise en forme

2. À quoi servent les balises `<h1>`, `<p>`, `<ul>` et `<li>` ?

   > _Ma réponse :_ <h1> : Définit un titre principal de niveau 1,<p> : Définit un paragraphe de texte structuré,<ul> : Crée une liste non ordonnée,<li> : Définit un élément de liste

3. Pourquoi l'image s'affiche-t-elle alors qu'elle n'est pas sur votre serveur ?

   > _Ma réponse :_ L'image s'affiche car l'attribut src de la balise <img> contient une URL absolue

---

## 🔵 Exercice 4 — Les templates

1. Pourquoi est-ce une bonne idée de séparer le code Python et le HTML ? (Pensez à une équipe avec un développeur et un graphiste.)

   > _Ma réponse :_ Le développeur s'occupe de la logique métier, des bases de données et des routes en Python, tandis que le graphiste/intégrateur web s'occupe de la mise en page et du style dans les fichiers HTML/CSS sans risquer de casser le code de l'application.

2. Les `{{ prenom }}` sont-ils remplacés par le serveur ou par le navigateur ? Comment l'avez-vous vérifié ?

   > _Ma réponse :_ C'est le serveur qui remplace. Pour verifier j'ai fait ctrl + U et je ne vois nulle part {{prenom}}

---

## 🔵 Exercice 5 — Le CSS et les liens

1. Quelle est la différence de rôle entre le HTML et le CSS ?

   > _Ma réponse :_ Le HTML: Il gère la structure et le contenu de la page et le CSS : Il gère la présentation et la mise en forme visuelle

2. Pour afficher votre page `/presentation`, combien de fichiers le navigateur doit-il télécharger ? (Vous pourrez le vérifier à l'exercice suivant !)

   > _Ma réponse :_ Le navigateur doit télécharger 2 fichiers :Le fichier HTML principal et le fichier CSS externe

3. Pourquoi faut-il parfois faire **Ctrl + F5** pour voir les changements de CSS ?

   > _Ma réponse :_ Pour accélérer l'affichage des sites

---

## 🟣 Exercice 6 — Espionner le navigateur

1. Que signifie HTTP ? Qui envoie la **requête** et qui envoie la **réponse** ?

   > _Ma réponse :_ HTTP signifie HyperText Transfer Protocol. C'est le client (mon navigateur) qui envoie la requête HTTP au serveur et c'est le serveur (PythonAnywhere) qui traite la demande et envoie la réponse HTTP.

2. Combien de requêtes votre page `/presentation` a-t-elle déclenchées ? Lesquelles ?

   > _Ma réponse :_ Elle a declechée 2 requêtes presentation (le document HTML) et style.css (la feuille de style).

3. Que signifie le code `200` ? Et le code `404` de la favicon ?

   > _Ma réponse :_ Code 200 (OK) : Succès. Le serveur a correctement trouvé et renvoyé la ressource demandée et le code 404 pour la favicon signifie que le navigateur a cherché automatiquement l'icône de l'onglet mais comme elle n'existe pas encore  ce dernier a renvoyé une erreur "Introuvable".

4. Pourquoi les modifications faites dans l'onglet Éléments ne sont-elles pas visibles par les autres visiteurs ?

   > _Ma réponse :_ Parce que l'onglet Éléments ne modifie que le code HTML/CSS temporaire chargé dans la mémoire vive de mon navigateur. Je ne modifie pas les fichiers réels situés physiquement sur le serveur PythonAnywhere. Les autres visiteurs interrogent toujours le serveur distant et reçoivent le code d'origine intact

---

## 🟣 Exercice 7 — Envoyer des informations dans l'URL

1. Dans l'URL `https://www.youtube.com/results?search_query=chat`, quel est le nom du paramètre ? Quelle est sa valeur ?

   > _Ma réponse :_ Nom du paramètre : search_query ,Valeur du paramètre : chat

2. Pourquoi le serveur plante-t-il avec `a=bonjour` ? Que faudrait-il faire pour l'éviter ?

   > _Ma réponse :_ La chaîne de caractères "bonjour" ne représentant pas un nombre valide Python lève une erreur. Pour eviter il faut utiliser un bloc d'exception try...except ValueError

3. Pourquoi est-il dangereux d'afficher **tel quel** ce que l'utilisateur envoie ?

   > _Ma réponse :_ Si un utilisateur malveillant injecte du code HTML ou JavaScript ce code sera exécuté directement par le navigateur des autres visiteurs.

---

## 🟣 Exercice 8 — Les formulaires

1. Quelle est la différence visible entre GET et POST ?

   > _Ma réponse :_ En GET on voit les donnees dans l'URL et en POST on voit pas

2. Pour un formulaire de **recherche**, quelle méthode choisiriez-vous ? Et pour un formulaire de **connexion avec mot de passe** ? Pourquoi ?

   > _Ma réponse :_ Formulaire de recherche = Méthode GET Pourquoi : Une recherche ne modifie aucune donnée sur le serveur .Formulaire de connexion avec mot de passe =Méthode POST Pourquoi : Avec GET, le mot de passe apparaîtrait en clair dans l'URL ce qui l'exposerait. Le POST masque ces informations sensibles de la barre d'adresse et empêche qu'elles soient enregistrées dans l'historique de navigation.

3. Les données envoyées en POST sont-elles vraiment « secrètes » ? (Pensez à ce que vous avez vu dans l'onglet Réseau.)

   > _Ma réponse :_ Non

---

## 🔴 Exercice 9 — Les codes de statut

1. Quelle est la différence entre une erreur `4xx` et une erreur `5xx` ? Qui est « fautif » dans chaque cas ?

   > _Ma réponse :_ Erreurs 4xx: Indiquent que le problème vient de la requête envoyée par le navigateur et Erreurs 5xx: Indiquent que le problème vient du serveur.

2. Comment fonctionne une redirection ? Qui fait la deuxième requête : le serveur ou le navigateur ?

   > _Ma réponse :_ Lorsqu'on accédez à une route qui redirige le serveur répond avec un code d'état HTTP de redirection accompagné d'un en-tête. C'est le navigateur qui lit cet en-tête et effectue automatiquement la deuxième requête HTTP vers la nouvelle adresse.

3. Donnez un exemple de situation où un vrai site utilise une redirection.

   > _Ma réponse :_ Lorsqu'un utilisateur se connecte sur un site le formulaire envoie une requête POST avec ses identifiants. Si la connexion réussit le serveur renvoie une redirection 302 vers la page du tableau de bord.

---

## 🔴 Exercice 10 — Ce que le serveur sait de vous

1. Citez trois informations que le serveur connaît sur vous, sans que vous ayez rien rempli.

   > _Ma réponse :_ Mon adresse IP, mon navigateur et mes langues

2. À quoi peut servir l'en-tête `Accept-Language` pour un site comme Wikipédia ?

   > _Ma réponse :_ Cet en-tête permet à Wikipédia d'effectuer une négociation de contenu automatique pour rediriger ou afficher par défaut le site dans la langue préférée du visiteur

3. Dans l'Access log, retrouvez une requête qui a reçu un code `404`. Quelle page était demandée ?

   > _Ma réponse :_ 

4. Après cet exercice, que pensez-vous de la notion de « navigation anonyme » ?

   > _Ma réponse :_ La navigation privée ne rend pas du tout anonyme sur Internet. Ce qu'elle fait : Elle empêche simplement le navigateur de sauvegarder localement mon historique, mes cookies et mes données de formulaires sur mon ordinateur.

---

## 🔴 Exercice 11 — Le Web des machines : API et JSON

1. Quelle est la différence entre une page HTML et une réponse JSON ? À qui chacune est-elle destinée ?

   > _Ma réponse :_ Page HTML : C'est un document structuré contenant du texte, des balises et des styles. Elle est destinée à être interprétée et affichée visuellement pour un être humain dans son navigateur.
   >Réponse JSON : C'est un format de données brut et structuré. Elle est destinée à être lue et traitée par un programme informatique.

2. Dans la page `/horloge`, quel code s'exécute sur le **serveur** et quel code s'exécute dans le **navigateur** ?

   > _Ma réponse :_ Sur le serveur : Flask exécute la route @app.get("/horloge") charge le fichier horloge.html et l'envoie au navigateur. Plus loin, le serveur gère aussi l'API /api/heure en calculant la date/heure actuelle et en renvoyant le JSON.
   > s le navigateur: Le navigateur reçoit la page HTML/JS. Son moteur JavaScript exécute le script  pour récupérer les données JSON de l'API et mettre à jour le DOM HTML en temps réel sans recharger la page.

3. Citez une application de votre téléphone qui, selon vous, utilise une API. Quelles données échange-t-elle ?

   > _Ma réponse :_ Météo

---

## 🏁 Pour conclure

En quelques phrases, expliquez à un ami ce qui se passe entre le moment où il tape une adresse dans son navigateur et celui où la page s'affiche :

> _Ma réponse :_ Lorsque tu tapes une adresse web ton navigateur envoie une requête via Internet au serveur distant pour lui demander le contenu de la page puis il traduit le code HTML CSS et JavaScript reçu pour l'afficher visuellement sur ton écran.
