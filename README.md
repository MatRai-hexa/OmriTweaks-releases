# OmriTweaks

**Optimisation de Windows 10 et 11, en un clic, adaptée à votre PC.**

OmriTweaks est une application gratuite qui rassemble, dans une interface simple, les réglages
(« tweaks ») qui rendent Windows plus rapide, plus léger et plus réactif. Elle détecte votre
matériel, n'affiche que ce qui convient à votre PC et explique précisément chaque réglage, avec ses
risques, avant de l'appliquer.

> **Version bêta** : l'application est en cours de développement (versions 0.x). La version 1.0
> sera la première version stable.

---

## Sommaire

- [Téléchargement](#téléchargement)
- [Installation et premier lancement](#installation-et-premier-lancement)
- [Fonctionnalités](#fonctionnalités)
- [Les tweaks disponibles](#les-tweaks-disponibles)
- [Sécurité : comment OmriTweaks vous protège](#sécurité--comment-omritweaks-vous-protège)
- [Mises à jour](#mises-à-jour)
- [Configuration requise](#configuration-requise)
- [Questions fréquentes](#questions-fréquentes)

---

## Téléchargement

Téléchargez **`OmriTweaks.exe`** depuis la dernière version :

**➡ [Télécharger la dernière version](https://github.com/MatRai-hexa/OmriTweaks-releases/releases/latest)**

Un seul fichier, aucune installation : Python et toutes les bibliothèques sont intégrés.

## Installation et premier lancement

1. Placez `OmriTweaks.exe` où vous voulez (le Bureau, par exemple) et double-cliquez dessus.
2. Windows demande l'autorisation de l'exécuter **en tant qu'administrateur** : c'est nécessaire pour
   modifier les réglages du système. Acceptez.
3. Au premier lancement, Windows SmartScreen peut afficher « Windows a protégé votre ordinateur »,
   car l'application n'est pas signée : cliquez sur **Informations complémentaires**, puis
   **Exécuter quand même**.
4. Une fenêtre de présentation résume vos composants, les points à surveiller sur votre PC et des
   conseils adaptés.

**Conseil** : avant votre première série de réglages, cliquez sur **Point de restauration** (en haut
à droite) pour pouvoir revenir en arrière à tout moment.

## Fonctionnalités

### Adaptée à votre matériel
- Détection du processeur (Intel, AMD, processeurs hybrides cœurs P + E), des cartes graphiques
  (NVIDIA, AMD, Intel), de la mémoire, du disque (SSD NVMe, SSD, disque dur), du type de PC (portable
  ou bureau) et de la version de Windows.
- Seuls les tweaks compatibles sont affichés ; ceux des autres fabricants sont masqués.
- **Profil du PC** (modeste, intermédiaire ou performant) : sur un PC modeste, un **mode léger**
  s'active automatiquement (animations coupées, mesures espacées) pour laisser toute la puissance à
  vos applications.
- Section **« Recommandé pour ce PC »** : les tweaks les plus utiles pour votre configuration, en un
  clic.

### Accueil : votre PC en temps réel
Tuiles en direct avec courbe des 90 dernières secondes (survolez une courbe pour lire une valeur) :
processeur (charge, fréquence), mémoire, carte graphique (charge, fréquence, consommation, mémoire
vidéo), températures du processeur et de la carte graphique, ventilateurs, disque, réseau et
batterie.

> La température du processeur et la vitesse des ventilateurs ne sont pas toujours exposées par
> Windows. Pour des mesures précises, lancez [LibreHardwareMonitor](https://github.com/LibreHardwareMonitor/LibreHardwareMonitor) :
> OmriTweaks lit automatiquement ses capteurs.

### Onglets par composant
Processeur · Carte graphique · Mémoire · Stockage · Réseau · Windows & services, avec recherche,
filtres (type, état, risque, redémarrage) et tri. Le bouton **« Tout appliquer »** applique les
tweaks affichés ; sur la carte graphique, **« Mode performance max »** la passe entièrement en mode
performance.

### Onglet Écran
Luminosité, contraste, gamma, température de couleur et intensité du rouge, du vert et du bleu, en
direct, pour tous les écrans ou un seul ; préréglages **Lecture**, **Nuit**, **Jeu vif** et
**Cinéma** ; rétroéclairage réel de l'écran des portables ; mire de contrôle.

### Onglet Ventilateurs (inspiré de FanControl)
- Stratégie de refroidissement de Windows (active ou passive).
- Profil thermique du BIOS sur les PC Dell compatibles (Optimisé, Frais, Silencieux, Ultra
  performance).
- Courbes température → vitesse : glissez les points, réglez la source de température,
  l'hystérésis et le temps de réponse. Elles pilotent les ventilateurs des cartes graphiques NVIDIA
  de PC de bureau.

> Sur la plupart des portables, les ventilateurs sont gérés par le matériel et Windows ne permet
> pas de les commander : l'onglet l'indique clairement.

### Suivi
L'onglet **Tweaks activés** montre l'état réel de chaque réglage sur votre PC (activé, non activé,
non applicable), avec un bouton pour l'annuler ou l'appliquer.

### Personnalisation
- 8 thèmes (Sombre, Graphite, Minuit, OLED, Nord, Forêt, Clair, Crème) + mode Automatique qui suit
  Windows, 7 couleurs d'accent ou une couleur sur mesure.
- **Couleurs entièrement modifiables** : fond, cartes, texte, boutons, bordures, journal…, avec
  alerte si le texte devient difficile à lire.
- Police, taille du texte, densité, arrondi, style des cartes, onglets compacts, vitesse des
  animations, opacité de la fenêtre.

### En arrière-plan
La croix vous demande si vous voulez **quitter** ou **réduire OmriTweaks près de l'horloge**. En
arrière-plan, il ne consomme pas de processeur, garde vos réglages d'écran et de ventilateurs actifs,
et reste accessible d'un clic (clic droit : préréglages d'écran, libérer la RAM, quitter). Option
**Lancer avec Windows**.

## Les tweaks disponibles

| Catégorie | Tweaks |
|---|---|
| **Processeur** | Plan d'alimentation maximal · Fréquence minimale à 100 % · Priorité au programme actif · Désactiver le Power Throttling · Désactiver le parcage des cœurs · Turbo Boost / Precision Boost agressif · Prioriser les cœurs P (Intel hybride) |
| **Carte graphique** | Planification GPU matérielle · NVIDIA / AMD : performances maximales · Télémétrie NVIDIA · Priorité GPU aux jeux · PCI Express à pleine puissance · Désactiver le MPO · Optimisations en mode fenêtré · Taux de rafraîchissement variable · Optimisation plein écran · Mode Jeu · Game DVR |
| **Mémoire** | Libérer la RAM · Compression mémoire · Garder le noyau en RAM · SysMain |
| **Stockage** | Fichiers temporaires · Cache Windows Update · Corbeille · Cache des miniatures · Prefetch · Journaux d'événements · Hibernation · Date de dernier accès · Optimisation du disque (TRIM / défragmentation) |
| **Réseau** | Bridage réseau · Optimisation TCP · DNS Cloudflare / Google · Vider le cache DNS · Réinitialiser le réseau |
| **Windows & services** | Effets visuels allégés · Menus instantanés · Applications en arrière-plan · Applications au démarrage · Télémétrie · Services Xbox · Services inutiles |

## Sécurité : comment OmriTweaks vous protège

- **Confirmation avant chaque action** : ce que fait précisément le tweak (clés de registre,
  commandes), son **niveau de risque** (aucun, faible, modéré, élevé) et ses conséquences, s'il est
  réversible et s'il demande un redémarrage.
- **Point de restauration** proposé avant les tweaks à risque et avant « Tout appliquer ».
- **Bouton « Annuler »** sur chaque tweak réversible ; les valeurs d'origine de votre PC sont
  sauvegardées pour être remises à l'identique.
- **Avertissements adaptés** : PC portable (chaleur, autonomie), PC d'entreprise (DNS, télémétrie,
  stratégies informatiques), peu de mémoire, disque dur…

> OmriTweaks modifie des réglages de Windows. Lisez la fenêtre de confirmation avant d'appliquer un
> tweak, en particulier sur un PC professionnel géré par un service informatique.

## Mises à jour

OmriTweaks vérifie automatiquement les nouvelles versions publiées ici (au démarrage puis toutes
les 10 minutes). Quand une version est disponible, une fenêtre **« Mise à jour disponible »**
affiche les nouveautés : **Mettre à jour maintenant** télécharge la nouvelle version, ferme
l'application, la remplace et la relance toute seule.

Réglages dans **Paramètres > Mises à jour** (recherche automatique, bouton « Rechercher
maintenant »).

## Configuration requise

- Windows 10 ou Windows 11, 64 bits (certains tweaks, comme la planification GPU matérielle ou les
  optimisations en mode fenêtré, n'apparaissent que sur les versions de Windows qui les prennent en
  charge)
- Droits administrateur
- Environ 35 Mo d'espace disque et 60 Mo de mémoire

## Questions fréquentes

**L'antivirus ou SmartScreen bloque le fichier.**
L'application n'est pas signée numériquement : Windows se méfie des programmes peu répandus. Si
vous l'avez téléchargée depuis cette page, vous pouvez l'autoriser.

**Comment revenir en arrière ?**
Bouton **Annuler** sur le tweak concerné, onglet **Tweaks activés**, ou point de restauration
Windows (Panneau de configuration > Récupération > Ouvrir la Restauration du système).

**Où sont enregistrés mes réglages ?**
Dans `%APPDATA%\OmriTweaks` (paramètres de l'application et valeurs d'origine sauvegardées).

**Comment désinstaller ?**
Quittez OmriTweaks (clic droit sur son icône près de l'horloge > Quitter), désactivez « Lancer avec
Windows » s'il était activé, puis supprimez `OmriTweaks.exe` et le dossier `%APPDATA%\OmriTweaks`.
