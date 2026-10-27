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
2. Prompt recommandé : "8-bit chiptune Pac-Man arcade 1980 style, energetic looping background music, square waves, no vocals, 120 BPM, retro Namco"
3. Génère, écoute, télécharge en MP3
4. Héberge le MP3 (même domaine ou GitHub raw) ou place-le à côté du HTML
5. Dans le code source (View Source) : ajoute juste avant `</body>` :

```html
<audio id="bgm" loop autoplay>
  <source src="pacman-theme.mp3" type="audio/mpeg">
</audio>
<script>
  const bgm = document.getElementById('bgm');
  bgm.volume = 0.4;
  // Play on first user interaction (autoplay policy)
  document.addEventListener('keydown', () => { if (bgm.paused) bgm.play(); }, { once: true });
  document.addEventListener('click', () => { if (bgm.paused) bgm.play(); }, { once: true });
</script>
```

Pour les effets (waka, death, power pellet) : génère des sons courts sur Flow Music et joue-les via `new Audio('waka.mp3').play()` dans le code JS aux événements correspondants.

## Processus

- Retouche et génération d'images avec Grok
- Code généré et itéré avec Grok
- Code libre de droit

## Licence

MIT License - voir LICENSE

Créé par Stéphane avec Grok.