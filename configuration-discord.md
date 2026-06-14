---
description: >-
  Avant de pouvoir lancer ton code, tu dois déclarer ton application auprès de
  Discord. C'est ici que tu vas activer le mode "User App" et récupérer tes clés
  d'accès secrètes !
---

# 🛠️ Configuration Discord

{% stepper %}
{% step %}
### Étape 1 : Créer un environnement !

Créez un fichier `.env` et copiez collez ceci :&#x20;

```
DISCORD_BOT_TOKEN=bot_token_here
DISCORD_CLIENT_ID=client_id_here

RULE34_API_KEY=api_key_here
RULE34_USER_ID=user_id_here
```
{% endstep %}

{% step %}
### Étape 1 : Créer le projet sur Discord

Rends-toi sur le [Discord Developer Portal](https://discord.com/developers/applications). Connecte-toi avec ton compte, clique sur le gros bouton bleu **New Application** en haut à droite, donne-lui un nom qui te plaît et valide.
{% endstep %}

{% step %}
### Étape 2 : Activer le mode "User App" (Crucial !)

Dans le menu de gauche, clique sur l'onglet Installation.

* Dans la section _Installation Contexts_, coche la case **User Install** et décoche _Guild Install_.
* Dans le champ _Install Link_, sélectionne **Discord Provided Link** dans le menu déroulant.

_Grâce à ça, l'application pourra être installée directement sur ton propre compte utilisateur pour t'accompagner sur tous les serveurs ! (Les autres utilisateur ne peuvent pas y ajouter ton application !)_
{% endstep %}

{% step %}
### **Étape 3 : Récupérer tes identifiants secret**

C'est le moment de récupérer tes variables d'environnement. Toujours dans le menu de gauche :

* **Le Client ID :** Va dans _General Information_, repère le champ **Application ID** et copie-le (ce sera ton `DISCORD_CLIENT_ID`).
* **Le Token :** Va dans l'onglet _Bot_, clique sur le bouton **Reset Token**, puis copie la longue ligne de texte qui s'affiche (ce sera ton `DISCORD_BOT_TOKEN`).&#x20;

{% hint style="danger" %}
### Garde tes clés secrètes !

Ne donne jamais, au grand jamais, ton `DISCORD_BOT_TOKEN` à quelqu'un et ne le push pas en clair sur un dépôt GitHub public. Si quelqu'un le récupère, il peut contrôler ton application à ta place !
{% endhint %}
{% endstep %}
{% endstepper %}

