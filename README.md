# PAC-MAN 1980 Arcade HD

![PAC-MAN Arcade](https://jeu-retro.grok.me/pacman-borne.png?v=3)

Jeu Pac-Man créé 100% avec Grok : de la retouche photo à la génération d'images jusqu'à la création du jeu complet (clone du classique arcade 1980).

## Jouer

- [Jouer en ligne](https://jeu-retro.grok.me/pacman.html)
- Accueil : [https://jeu-retro.grok.me/](https://jeu-retro.grok.me/)

## Transférer le code HTML5 à un bot

Le code source HTML5 complet est libre de droit (MIT).

Pour le récupérer et le transférer à ton bot / agent :
1. Ouvre https://jeu-retro.grok.me/pacman.html
2. Clic droit → Afficher le code source (ou Ctrl+U)
3. Copie tout le HTML/JS/CSS
4. Colle-le dans ton bot ou sauvegarde en .html

Le jeu est 100 % client-side (canvas + JS). Aucune dépendance externe obligatoire.

## Ajouter de la musique (Google Flow Music)

1. Va sur https://www.flowmusic.app/
2. Génère une piste chiptune / 8-bit / arcade style (ex: "Pac-Man style 8-bit chiptune, energetic, looping, no vocals")
3. Télécharge en MP3 ou WAV
4. Dans le code HTML5 : ajoute une balise `<audio>` et joue-la au démarrage / sur événements (manger un point, power pellet, mort, etc.)

Exemple minimal :
```html
<audio id="bgm" loop>
  <source src="pacman-theme.mp3" type="audio/mpeg">
</audio>
<script>
  document.getElementById('bgm').play();
</script>
```

## Processus

- Retouche et génération d'images avec Grok
- Code généré et itéré avec Grok
- Code libre de droit

## Licence

MIT License - voir LICENSE

Créé par Stéphane avec Grok.