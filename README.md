# 🧮 Renaissance de Microsoft Multiplan 3 sous Windows 11


**État du projet** :
#
✅ Opérationnel | **Plateforme** : Windows 10/11 | **Niveau** : Intermédiaire
#
## Un guide pas à pas pour faire revivre le logiciel historique **Microsoft Multiplan 3 de 1986** dans un environnement DOS émulé sur un système **Windows 11 en 2026.**
#
Ce projet démontre la préservation de logiciels par l'émulation... **40 ans**.
#
---

## 📋 Table des matières

- [Aperçu et Motivation](#-aperçu-et-motivation)
- [Architecture du Projet](#-architecture-du-projet)
- [Prérequis Matériels](#-prérequis-matériels)
- [🛠 Guide d'Installation & Configuration](#-guide-dinstallation--configuration)
- [🚀 Utilisation](#-utilisation)
- [📁 Structure des Fichiers](#-structure-des-fichiers)
- [❓ FAQ](#-faq)
- [🤝 Contribution](#-contribution)
- [📜 Licence](#-licence)
- [🙏 Remerciements](#-remerciements)

---

## 🎯 Aperçu et Motivation

**Microsoft Multiplan** a été un pionnier des tableurs avant l'avènement d'Excel. Ce projet a pour objectifs de :
*   **Préserver l'accès** à un outil historique de l'informatique personnelle.
*   Servir de **tutoriel pratique** sur l'émulation de systèmes DOS.
*   Illustrer le principe de **pont technologique** entre des logiciels anciens et des OS modernes.

**Résultat final** : Un lanceur en un clic qui exécute Multiplan 3 de manière stable sous Windows 11, avec un accès complet aux fichiers de travail.

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
