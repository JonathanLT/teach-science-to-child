# Modules Électroniques pour Enfants

**Projet pédagogique** : Découverte de l'électronique par assemblage de modules standardisés type "tuiles".

---

## 🎯 Objectif

Permettre aux enfants de comprendre les mécaniques électroniques fondamentales en reliant des modules physiques pour créer des circuits fonctionnels (exemple : allumer une LED).

---

## 📐 Spécifications Techniques

### Format Standard des Modules

- **Dimensions** : 40 × 40 mm (carré), épaisseur 8–12 mm
- **4 interfaces électriques** : une par bord (Nord, Est, Sud, Ouest)
- **Chaque interface** : 2 contacts polarisés (`+` rouge, `−` noir)
- **Détrompage** : aimants polarisés
- **Tension max** : 3 V (2 piles LR44), aucun branchement secteur

### Brochage Standard par Bord

Chaque bord (N, E, S, O) comporte 2 plots de contact :

- **Plot +** (rouge) : positionné à 12 mm du bord gauche
- **Plot −** (noir) : positionné à 28 mm du bord gauche
- Distance entre plots : 16 mm
- Diamètre contact : 4 mm (3-pins, aimanté)

---

## 🧩 Modules de Base

### 1. Module `Wire-I` (Ligne droite)

- **Fonction** : Relie deux bords opposés
- **Variantes** : N↔S ou E↔O (selon orientation à 0° ou 90°)
- **Usage** : Rallonge de circuit en ligne droite

### 2. Module `Wire-L` (Perpendiculaire)

- **Fonction** : Relie deux bords adjacents (angle 90°)
- **Variantes** : N↔E, E↔S, S↔O, O↔N (par rotation de 90°)
- **Usage** : Faire tourner le chemin électrique

### 3. Module `Wire-X` (Perpendiculaire)

- **Fonction** : Découpage de la tension
- **Variantes** : N↔E↔S↔O
- **Usage** : Permet de faire des nœuds

### 4. Module `Pile`

- **Fonction** : Source d'énergie 3 V (2 × AA)
- **Sorties** : 2 bords opposés (N et S), + sur N, − sur S
- **Sécurité** : Interrupteur général intégré, protection court-circuit

### 5. Module `LED`

- **Fonction** : Diode électroluminescente avec résistance intégrée
- **Résistance** : 220–330 Ω (calcul pour 3 V, LED rouge/verte)
- **Orientation** : Entrée/sortie sur bords opposés (N→S)
- **Couleurs** : Rouge, verte, jaune, bleue selon variante

### 6. Module `Bouton Poussoir`

- **Fonction** : Contact momentané (NO - Normalement Ouvert)
- **Usage** : Allumer la LED uniquement pendant l'appui
- **Connexion** : En série dans le circuit

### 7. Module `Interrupteur`

- **Fonction** : Contact maintenu ON/OFF
- **Usage** : État mémorisé (allumé/éteint)
- **Type** : Toggle switch ou slide switch

### 8. Module `Potentiomètre`

- **Fonction** : Variation de résistance (luminosité LED)
- **Valeur** : 10 kΩ linéaire
- **Usage** : Niveau "découverte variation" (ajustement manuel)

---

## 🎓 Parcours Pédagogique

### Activité 1 : Circuit Fermé (15 min)

**Objectif** : Comprendre qu'il faut un chemin continu.

**Montage** :

```text
Pile (+) → Wire-I → LED → Wire-I → Pile (−)
```

**Résultat attendu** : La LED s'allume.

---

### Activité 2 : Bouton Momentané (20 min)

**Objectif** : Contact temporaire.

**Montage** :

```text
Pile (+) → Bouton → LED → Pile (−)
```

**Résultat attendu** : La LED s'allume uniquement quand on appuie.

---

### Activité 3 : Interrupteur (20 min)

**Objectif** : État mémorisé ON/OFF.

**Montage** :

```text
Pile (+) → Interrupteur → LED → Pile (−)
```

**Résultat attendu** : La LED reste allumée après basculement.

---

### Activité 4 : LEDs en Série (30 min)

**Objectif** : Observer la division de tension.

**Montage** :

```text
Pile (+) → LED1 → LED2 → Pile (−)
```

**Résultat attendu** : Les 2 LEDs sont moins lumineuses.

---

### Activité 5 : LEDs en Parallèle (30 min)

**Objectif** : Comparer avec le montage série.

**Montage** :

```text
Pile (+) → Wire-X (split) → LED1 → Wire-X (join)
           ↓                          ↑
           → LED2 ───────────────────→
```

**Résultat attendu** : Les 2 LEDs ont la même luminosité.

---

### Activité 6 : Potentiomètre (30 min)

**Objectif** : Variation de luminosité.

**Montage** :

```text
Pile (+) → Potentiomètre → LED → Pile (−)
```

**Résultat attendu** : Tourner le bouton modifie la luminosité.

---

### Activité 7 : Défi Erreur (25 min)

**Objectif** : Diagnostic de panne.

**Situation** : Un fil est inversé volontairement par l'animateur.

**Mission** : Retrouver l'erreur et corriger.

---

### Activité 8 : Feu de Signal (35 min)

**Objectif** : Combiner bouton + interrupteur.

**Montage** :

```text
Pile (+) → Interrupteur → Bouton → LED → Pile (−)
```

**Résultat attendu** : L'interrupteur active le circuit, le bouton contrôle la LED.

---

### Activité 9 : Code Morse (40 min)

**Objectif** : Communication par signaux lumineux.

**Montage** :

```text
Pile (+) → Bouton → LED → Pile (−)
```

**Exercice** : Envoyer SOS (• • • — — — • • •).

---

### Activité 10 : Projet Libre (45 min)

**Objectif** : Créativité et autonomie.

**Mission** : Créer une lampe interactive avec minimum 3 modules différents.

---

## 🛠️ Kit Matériel Recommandé

| Module              | Quantité |
|---------------------|----------|
| Pile (3 V)          | 3        |
| LED (rouge/verte)   | 5        |
| Bouton poussoir     | 2        |
| Interrupteur        | 2        |
| Potentiomètre       | 1        |
| Wire-I              | 10       |
| Wire-L              | 10       |
| Wire-X              | 10       |

### Connectique

- **3-pins aimenté** : Contacts magnétiques polarisés mâle/femelle

---

## 🏗️ Fabrication des Modules

### Boîtier (impression 3D ou découpe)

- **Matériau** : PLA (impression 3D)
- **Finition** : Coins arrondis, ponçage léger
- **Marquage** : Pictogramme + nom du module sur face avant

### Face Avant

- Pictogramme clair (pile, LED, bouton, etc.)
- Nom du module en lettres capitales
- Couleur de fond selon famille (bleu = alimentation, jaune = contrôle, rouge = sortie)

### Face Arrière

- Schéma électrique ultra-simple (2 symboles max)
- Légende + / − pour repérage polarité

### Robustesse

- Bornes vissées ou soudées (pas de fil nu accessible)
- Protection contre court-circuit (fusible 500 mA sur module Pile)
- Test de chute obligatoire (50 cm sur sol dur)

---

## 🔒 Sécurité

### Règles Obligatoires

1. **Tension max** : 3 V (2 piles LR44), jamais de secteur
2. **Supervision adulte** : Vérification avant mise sous tension
3. **Interdiction** : Court-circuit direct Pile + / −
4. **Composants** : Aucune pièce détachable < 3 cm (risque ingestion)

### Protection Intégrée

- Fusible réarmable 500 mA (PTC) sur module Pile
- Résistance toujours intégrée au module LED (jamais de LED nue)
- Contacts affleurants (pas de pointe métallique saillante)

---

## 💰 Budget Indicatif

**Pour un kit** :

- Version économique : 180–250 €
- Version standard : 250–350 €
- Version premium (aimants, boîtiers pro) : 350–500 €

**Détail par module** :

- Pile (avec support + interrupteur) : 5–8 € / pièce
- LED (avec résistance + boîtier) : 2–3 € / pièce
- Bouton/Interrupteur : 1,5–2,5 € / pièce
- Potentiomètre : 2–4 € / pièce
- Wire (passif) : 1–1,5 € / pièce

---

## 🎯 Évaluation Pédagogique

### Critères de Réussite

- **Niveau 1** : L'enfant sait créer un circuit fermé fonctionnel
- **Niveau 2** : L'enfant explique pourquoi la LED s'allume (ou non)
- **Niveau 3** : L'enfant diagnostique une erreur de montage
- **Niveau 4** : L'enfant conçoit un circuit original fonctionnel

### Questions Clés

- "Pourquoi la LED ne s'allume pas si on enlève un fil ?"
- "Que se passe-t-il si on inverse + et − ?"
- "Comment faire pour que 2 LEDs s'allument en même temps ?"

---

## 📚 Ressources Complémentaires

### Schémas de Circuits sur Grille 4×4

#### Circuit 1 : LED Simple

```text
[Pile] → [Wire-I] → [LED] → [Wire-L]
                               ↓
[Wire-I] ← [Wire-L] ← ← ← ← ←
   ↓
[Pile] (retour −)
```

#### Circuit 2 : Bouton + LED

```text
[Pile] → [Bouton] → [LED] → [Wire-I] → retour Pile
```

#### Circuit 3 : Interrupteur + Potentiomètre + LED

```text
[Pile] → [Interrupteur] → [Potentiomètre] → [LED] → retour Pile
```

---

## 🚀 Évolutions Futures

### Modules Avancés (niveau collège)

- **Buzzer** : Mise en action d'un son
- **Moteur DC** : Mise en action d'un mouvement
- **Logic gate** : Création des portes logiques (Notion d'algébre de Boole)
- **Transistor** : Amplification ou commutation (Simplification des portes logique)
- **Photorésistance** : Détection de lumière
- **Condensateur** : Stockage temporaire d'énergie (⚠️ peut être dangereux si mal déchargé ⚠️)

### Programmation

- **Module Arduino** : Introduction au code (LED clignotante)
- **Module Capteur** : Température, distance, son

---

## 📝 Licence

Ce projet est mis à disposition sous licence **Creative Commons BY-SA 4.0**.

Vous êtes libre de :

- Partager et adapter ce contenu
- L'utiliser à des fins commerciales

Sous conditions :

- Attribution (mention de l'auteur)
- Partage dans les mêmes conditions

---

## ✨ Contribution

Pour toute amélioration ou suggestion :

- Ouvrir une issue
- Proposer un schéma de circuit additionnel
- Partager un retour d'expérience atelier

---

**Version** : 1.0  
**Date** : 18 février 2026  
**Contact** : [Jonathan LOQUET](mailto:jonathanlt.idf@gmail.com)
