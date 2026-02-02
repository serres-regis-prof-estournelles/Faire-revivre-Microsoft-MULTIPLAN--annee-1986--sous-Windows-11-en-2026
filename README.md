##🕰️ Pourquoi Multiplan ? (Le voyage d'un quinqua)
#
Ce projet est né d'une émotion : celle de retrouver, en 2026, le tableur Multiplan avec lequel j'ai découvert l'informatique il y a 40 ans. 
#
Témoin matériel de l'histoire, Multiplan (sorti initialement en 1982) nous rappelle une époque où tout se gérait au clavier, sans souris, sans copier/coller...
#
🛠️ Installation Rapide (Le Guide "Infaillible")
#
Pour les nostalgiques pressés, voici la marche à suivre :


---

## 🧱 Architecture du Projet

Le schéma ci-dessous illustre l'interaction entre les différentes couches logicielles :

```mermaid
flowchart TD
    A[Système Hôte<br>Windows 11] --> B{Couche d'Émulation<br>DOSBox Staging}
    B --> C[Système Invité<br>Environnement MS-DOS]
    C --> D[Application Cible<br>Multiplan 3]
    
    E[Dossier de Travail Hôte<br>C:\\DOSGAMES\\] -- Monté comme lecteur C: --> C
    D -- Lit/Écrit --> F[Fichiers .MOD utilisateur]
    F -- Stockés dans --> E


👤 Auteur : SERRES Régis Enseignant - Lycée Estournelles de Constant, La Flèche (72) GitHub : @serres-regis-prof-estournelles
