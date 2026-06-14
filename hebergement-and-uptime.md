---
description: >-
  Pour que ton application fonctionne 24h/24 même quand ton ordinateur est
  éteint, nous allons l'héberger gratuitement dans le Cloud !
---

# 🌐 Hébergement & Uptime

{% hint style="info" %}
#### Le combo gagnant

Nous utilisons **Render** pour faire tourner le code, combiné à **UptimeRobot** pour envoyer un signal toutes les 5 minutes et empêcher l'application de s'endormir.
{% endhint %}

{% tabs %}
{% tab title="1. Render" %}
{% stepper %}
{% step %}
### Crée un compte sur [Render.com](https://render.com) et connecte ton compte GitHub.
{% endstep %}

{% step %}
### Clique sur New + → Web Service.
{% endstep %}

{% step %}
### Sélectionne ton dépôt `DiscordR34App`.
{% endstep %}

{% step %}
### Reste sur l'offre Free (Gratuite).
{% endstep %}
{% endstepper %}

<table><thead><tr><th width="287.39996337890625">Nom de la Variable</th><th>Valeur / Provenance</th></tr></thead><tbody><tr><td><code>DISCORD_CLIENT_ID</code></td><td>Ton ID d'application récupéré sur Discord.</td></tr><tr><td><code>DISCORD_BOT_TOKEN</code></td><td>Le jeton (Token) secret de ton bot Discord.</td></tr><tr><td><code>RULE34_API_KEY</code></td><td>Ta clé API personnelle rule34.xxx.</td></tr><tr><td><code>RULE34_USER_ID</code></td><td>Ton ID de compte utilisateur rule34.xxx.</td></tr></tbody></table>
{% endtab %}

{% tab title="2. UptimeRobot" %}


{% stepper %}
{% step %}
### Crée un compte gratuit sur [UptimeRobot.com](https://uptimerobot.com).
{% endstep %}

{% step %}
### Sur ton tableau de bord, clique sur + Add New Monitor.
{% endstep %}

{% step %}
### Configure le moniteur avec ces paramètres exacts :

1. **3.1. Monitor Type** : `HTTP(s)`
2. **Friendly Name** : `Discord R34 App`
3. **URL (or IP)** : _Colle l'URL que Render t'a donnée pour ton Web Service (ex:_ [_https://ton-app.onrender.com_](https://www.google.com/search?q=https://ton-app.onrender.com)_)_.
4. **Monitoring Interval** : `Every 5 minutes` (Toutes les 5 minutes).
{% endstep %}

{% step %}
### Clique sur Create Monitor.
{% endstep %}
{% endstepper %}


{% endtab %}
{% endtabs %}

***

<p align="center"><a href="guide-des-commandes.md" class="button secondary">NEXT PAGE</a></p>
