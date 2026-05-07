# Calcul de l'indice d'Autorité Relative d'une chaîne YouTube



Cet indice permet de mesurer l'influence réelle d'une chaîne au sein d'un échantillon, en neutralisant les écarts extrêmes grâce à une pondération basée sur les racines carrées.



### 1\. Formule du Score Brut



Le score brut repose sur le volume de vues (notoriété), le volume d'abonnés (fidélité) et le volume de vidéos (activité).



**Pondération :**

* **Vues :** 50%
* **Abonnés :** 35%
* **Vidéos :** 15%



**Formule :**
$$Score\_{brut} = (\\sqrt{Vues} \\times 0,5) + (\\sqrt{Abonnés} \\times 0,35) + (\\sqrt{Vidéos} \\times 0,15)$$

\---

### 2\. Normalisation (Échelle 1 à 100)



Le score brut est projeté sur une échelle de 1 à 100 en utilisant les valeurs de référence de l'échantillon (Min/Max).



**Formule de normalisation :**
$$Score\_{final} = \\left( \\frac{Score - Score\_{min}}{Score\_{max} - Score\_{min}} \\right) \\times 99 + 1$$

\---

### Exemple de calcul : *GCN en Français*



Données : 79,9M vues, 214k abonnés, 1618 vidéos.



1. **Calcul du Score Brut :**

   * $\\sqrt{79,906,084} \\times 0,5 = 4469,5$
   * $\\sqrt{214,000} \\times 0,35 = 161,9$
   * $\\sqrt{1618} \\times 0,15 = 6,0$
   * **Total Score Brut *GCN* = 4637**



1. **Calcul de la Normalisation :**

   * $Score\_{max} = 10,271$ (*Aurélien Fontenoy*)
   * $Score\_{min} = 345$ (*Cols Cyclisme*)
   * $Normalisation = \\left( \\frac{4637 - 345}{10,271 - 345} \\right) \\times 99 + 1 \\approx \\mathbf{44}$
   * **Indice d'Autorité *GCN* = 44**

\---

#### Valeurs de Référence

Ces valeurs sont mises à jour périodiquement pour refléter l'évolution de l'échantillon :

* **Score Max (100) :** *Aurélien Fontenoy* (392M vues, 1.08M abonnés, 779 vidéos).
* **Score Min (1) :** *Cols Cyclisme* (356k vues, 9k abonnés, 91 vidéos).

