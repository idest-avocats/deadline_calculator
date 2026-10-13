# Calcul des délais – id est avocats

Outil en ligne d’aide au calcul des délais de procédure en droit suisse, développé par id est avocats Sàrl.

> **Aide au calcul uniquement.** Le résultat doit toujours être vérifié par l’utilisateur. Voir [AVERTISSEMENT.md](AVERTISSEMENT.md).

Version 1.2 (beta), octobre 2026. Historique : [CHANGELOG.md](CHANGELOG.md).

## Ce que fait l’outil

L’outil indique le dernier jour d’un délai à partir de la date de la communication. Il tient compte :

- de la suspension des délais (féries) propre à chaque procédure, y compris pour les délais en mois lorsque la loi le prévoit ;
- de la prolongation au troisième jour utile en poursuite (art. 63 LP) ;
- des samedis, dimanches et jours fériés du canton déterminant ;
- de la fiction de notification au 7e jour pour un pli recommandé non retiré ;
- du report d’un envoi postal normal reçu un samedi, un dimanche ou un jour férié, lorsque la loi le prévoit.

Il contrôle aussi le délai saisi : si l’acte choisi a un délai légal différent, l’outil affiche une alerte avec la base légale.

## Utilisation

1. **Point de départ** : date de la communication, ou date du premier avis de retrait pour un pli recommandé non retiré. Si la date tombe un samedi, un dimanche ou un jour férié, une case permet d’indiquer que l’acte est arrivé par courrier A-Post Plus (sans signature) : il est alors réputé notifié le jour ouvrable suivant, lorsque la loi le prévoit.
2. **Type de procédure** : procédure civile, poursuite et faillite, procédure pénale, Tribunal fédéral, administratif fédéral, assurances sociales, administratif cantonal ou marchés publics.
3. **Canton** : Vaud, Genève, Fribourg, Neuchâtel, Valais, Jura ou autre canton. Selon la procédure, il s’agit du canton du tribunal, de l’autorité ou du domicile de la partie ou de son mandataire. Le canton détermine les jours fériés et, en droit administratif, la loi de procédure applicable.
4. **Délai et acte** (les deux sont facultatifs, mais l’un des deux est nécessaire) :
   - délai laissé vide et acte choisi : le champ « Délai » se remplit automatiquement avec le délai légal ;
   - délai saisi sans acte : l’outil le calcule sans contrôle, selon le régime de féries choisi ;
   - délai saisi et acte choisi : l’outil indique si les deux sont compatibles et, si ce n’est pas le cas, calcule avec le délai saisi et propose de reprendre le délai légal.

En procédure sommaire ou de conciliation (CPC et procédures sommaires LP), une case indique si le tribunal a signalé l’absence de suspension (art. 145 al. 3 CPC). Si ce n’est pas le cas, l’outil applique la suspension (ATF 139 III 78).

Le résultat peut être copié (résumé pour le dossier) ou imprimé. L’affichage peut être réglé en mode clair, sombre ou automatique.

## Domaines couverts

| Domaine | Bases légales principales |
|---|---|
| Procédure civile | CPC, art. 138, 142 à 148, 209, 211, 239, 311 à 314, 321, 322, 329 |
| Poursuite et faillite | LP, art. 17, 18, 31, 56, 63, 74, 83, 107, 108, 148, 174, 250, 278, 279 ; CPC, art. 145 al. 4 |
| Procédure pénale | CPP, art. 85, 89, 90, 94, 354, 368, 396, 399 |
| Tribunal fédéral | LTF, art. 44 à 48, 100, 117 |
| Administratif fédéral | PA, art. 20 à 22a, 50 ; LMP, art. 56 |
| Assurances sociales | LPGA, art. 38 à 40, 52, 60 |
| Administratif cantonal | LPA-VD, LPA-GE, CPJA (FR), LPA-NE, LPJA (VS), Cpa (JU) |
| Marchés publics | AIMP 2019 (VD, FR, NE, VS, JU), AIMP 1994/2001 (GE), LMP, LTF |

Le détail des actes, délais, règles et jurisprudences figure dans [SOURCES.md](SOURCES.md).

## Règle de prudence

Lorsqu’il existe un doute sur le caractère férié d’un jour ou sur l’application des féries, l’outil retient la solution qui donne l’échéance la plus précoce. C.

## Limites connues

- Les délais fixés par une loi spéciale non listée ne sont pas contrôlés.
- Les suspensions particulières (par exemple art. 57 ss et 279 al. 5 LP) et la restitution de délai ne sont pas calculées.
- Les jours fériés communaux ou les fermetures exceptionnelles des greffes ne sont pas pris en compte.
- Les congés compensatoires décidés par le Conseil d’État neuchâtelois ne sont pas pris en compte.
- Genève, marchés publics : l’outil propose 10 jours (droit en vigueur au 13 octobre 2026) et, séparément, 20 jours selon le projet de loi PL 13620, à n’utiliser qu’après son entrée en vigueur.
- Envoi postal normal : la loi fédérale sur les notifications d’actes le week-end et les jours fériés (FF 2025 2891) étendra la règle de l’art. 142 al. 1bis CPC à la PA, à la LTF et à la LPGA. L’outil devra être adapté à son entrée en vigueur.

## Protection des données

id est avocats ne collecte aucune donnée dans le cadre de l’utilisation de l’outil : les calculs sont effectués dans le navigateur, et l’outil ne charge aucune ressource externe. Il mémorise uniquement, dans le stockage local du navigateur, le type de procédure, le canton et le mode d’affichage choisis (clés `idest-delais:dom`, `idest-delais:canton` et `idest-delais:theme`).

L’outil est hébergé sur GitHub, qui peut collecter certaines informations, notamment au moyen de cookies, conformément à sa propre déclaration relative à la protection des données.

## Licence

© 2026 id est avocats Sàrl.

Le code est distribué sous licence GNU Affero General Public License, version 3 ou toute version ultérieure (AGPL-3.0-or-later). Voir [LICENSE](LICENSE).

Les tableaux et textes juridiques (actes, délais, règles, notes, listes de jours fériés, ainsi que la documentation, notamment [SOURCES.md](SOURCES.md) et [CAS-DE-TEST.md](CAS-DE-TEST.md)) sont en outre mis à disposition sous licence [Creative Commons Attribution – Pas d’utilisation commerciale 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/deed.fr). Attribution : « id est avocats Sàrl, Calcul des délais ».

## Contact

id est avocats Sàrl, Lausanne.
