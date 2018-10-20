* Compte-rendu des réunions techniques concernant le choix et la mise en oeuvre d'un client web pour Regovar.
* Présents : Anne-Sophie, Jérémie, Olivier, Cyrille
* septembre - octobre 2018

S'agissant d'une application web (Single Page Application), et non d'un simple site web, il est nécessaire d'opter pour un framework adapté et non développer "à l'ancienne" avec une navigation page par page. A l'heure actuelle, 3 frameworks suffisamment matures sont utilisés par les géants du web et largement répandu à travers la toile:
* [Angular 2](https://angular.io/)
* [React JS](https://reactjs.org/)
* [Vue.JS](https://vuejs.org/)


## Présentation des frameworks

### React
**React** est une bibliothèque JavaScript libre développée par Facebook depuis 2013. Le but principal de cette bibliothèque est de faciliter la création d'application web monopage, via la création de composants dépendant d'un état et générant une page HTML à chaque changement d'état. 


### Angular
Angular est un cadriciel coté client open source basé sur TypeScript dirigée par l'équipe du projet Angular à Google et par une communauté de particuliers et de sociétés. 


### Vue
Vue.js est un framework JavaScript open-source pour la construction d'interfaces utilisateur. L'intégration dans des projets utilisant d'autres bibliothèques JavaScript est simplifiée avec Vue car elle est conçue pour être adoptée de manière incrémentielle

### Remarques

Un truc cool, c'est que quelque soit le framework utilisé, si on ne fait pas trop des trucs exotiques avec JS-HTML-CSS, le code sera compatible avec [Electron](https://github.com/maximegris/angular-electron), ce qui permet de convertir l'application web en application Desktop pour Linux/Max/Windows... Donc c'est plutôt cool :)


## Discussion

### License
Bien que issue, le plus souvent, des laboratoires privés de grandes entreprises comme Facebook ou Google, ces 3 frameworks ont la grande qualité d'être **libre et open-source**, tout en étant maintenu par une grande communauté et des grandes entreprises IT.

### Communauté : usage et popularité sur le web 
Pour ce qui est de la popularité, on peut regarder ce que nous dis [Google Trend](https://trends.google.fr/trends/explore?q=%2Fm%2F0j45p7w,%2Fg%2F11c0vmgx5d,%2Fm%2F012l1vxv). React et Angular sont clairement plus présent que Vue. Ca s'explique très simplement par le fait que Vue est le plus récent, et que les deux autres ont été développé et se sont fait connaître par Facebook et Google... donc forcement ça aide.

Reste que concrètement aujourd'hui, si on compare les github d'[Angular](https://github.com/angular/angular), [React](https://github.com/facebook/react) et de [Vue](https://github.com/vuejs/vue), c'est Angular qui a la communauté la plus active au coude avec celle de React


### Usage en production
* [Angular](https://www.madewithangular.com/)
* [React](https://github.com/facebook/react/wiki/sites-using-react)
* [Vue](https://fr.vuejs.org/) : J'ai pas trouvé de liste... mais bon on peut considérer à défaut que la liste des  sponsors sont aussi des utilisateurs en production.


### Prise en main du framework 
Les retours d'expériences sur le sujet, des personnes questionnés disent grossomodo que Angular est des 3 le plus gros framework. Il sait tout faire mais impose aussi bien souvent la façon de le faire, ce qui nécessite une période d'apprentissage non négligeable. Mais c'est un framework complet, très bien documenté

ReactJS est le plus simple des 3 frameworks, mais c'est essentiellement parce qu'il en fait beaucoup moins que les deux autres. ReactJS se concentre uniquement sur la création de composant web. Mais par exemple il ne va pas proposer de solution pour faire communiquer/interragir ces différents composant entre eux, et il faudra alors utiliser un autre framework pour le faire, et comme React existe maintenant depuis longtemps, il y a une multitude de librairie annexes pour faire la même chose. Le choix est souvent difficile, et demande soit une grande expérience pour choisir les bons, soit du temps pour chercher et tester les librairies et trouver la bonne.

VueJS étant le dernier arrivé, il a pu tirer profit de l'expérience de ses prédécesseurs et directement faire des choix d'architecture plus simple ou plus intuitif. Cependant, comme il est encore jeune, on ne sait pas si ces nouveaux choix sont si judicieux que ça. Donc au final ce qui est présenté comme un avantage par l'équipe de VueJs, ne semble pas si important que ça pour les développeurs questionnés sur le sujet, les choix sont toujours discutables, et si le plus souvent ça ne perturbe pas les développeurs habitués au développement web, ça ne révolutionne pas la chose non plus... c'est juste un peu différent.


### Courant dans les projets "bio-info" (échelle nationale)
La lecture des offres d'emploies en bioinformatique sur le site [SFBI](https://www.sfbi.fr/recherche_emplois), montre qu'on cherche plus souvent des compétences en Angular qu'en React, et jamais en Vue.


### Connaissance au sein de l'équipe Regovar
* Anne-Sophie: n'a pas d'expérience avec ces 3 frameworks
* Cyrille: Connait un peu Angular, a déjà developpé avec mais trouve que c'est trop gros et trop compliqué. N'a pas d'expérience avec React et Vue
* Jérémie: Connait un peu React, n'a jamais développé avec Vue et a eu de bon retour sur lui.
* Olivier: N'a pas d'expérience avec les 3, a eu de bon retour sur Angular et React.

Globalement l'équipe n'a jamais développé avec aucun de ces 3 frameworks, et n'a donc pas de préférence ou de raison forte pour adopter ou non un framework.
Si on met de côté les envies et les "choix du coeurs", les seuls expériences concrète et significatives sont en Angular pour Cyrille et React pour Jérémie. 


### Capacité du framework
#### Angular
**Les plus**
* Du TypeScript, la courbe d’apprentissage est certes importante, mais les avantages sont l’adoption en amont des nouvelles normes ES mais aussi du typage fort qui permet de détecter et corriger beaucoup de bug très tôt, ainsi qu'un gain de performance au runtime
* Un framework complet
* Une grande communauté
* Une architecture éprouvé
* Un moteur de DI (injection de dépendances)
* Une bonne documentation

**Les moins**
* La syntaxe complexe qui vient de l'usage de TypeScript.
* Des mises à jour qui peuvent poser des problèmes de migration.

**Selon le point de vu**
* "The Angular Way", il est difficile de sortir des sentiers battus. Une fois que vous faites votre application en Angular vous la faites jusqu’au bout en Angular. Certains verront ça comme une contrainte, d'autre comme avantage. Notre avis est que pour un projet communautaire et open-source, c'est plutôt une bonne chose d'avoir un framework qui "impose" une façon de faire, ça simplifiera la maintenance et contribuera à faciliter le travail en équipe.


#### React
**Les plus**
* Facile à apprendre. React est beaucoup plus facile à apprendre en raison de sa simplicité en termes de syntaxe. Les ingénieurs doivent simplement rappeler leurs compétences en écriture HTML, et c’est tout. Pas besoin d'apprendre en profondeur TypeScript comme dans Angular.
* Haut niveau de flexibilité et maximum de réactivité.
* DOM virtuel (modèle d'objet de document) qui permet d'organiser des documents aux formats HTML, XHTML ou XML dans une arborescence à partir de laquelle les navigateurs Web sont plus en mesure d'accepter les analyses, tout en analysant différents éléments de l'application Web.
* Combiné à l'ES6/7, ReactJS peut travailler facilement avec une charge élevée.
* Liaison de données descendante, ce qui signifie qu'avec ce type de flux de données, les éléments enfants ne peuvent pas affecter les données parent.
* Bibliothèque JavaScript 100% open source offrant de nombreuses mises à jour et améliorations au quotidien, en fonction des contributions des développeurs du monde entier.
* Absolument léger, car les données stockées du côté utilisateur peuvent être facilement représentées simultanément du côté serveur.
* La migration entre les versions est généralement très facile, avec Facebook fournissant des «codemods» pour automatiser une grande partie du processus.

**Les moins**
* Manque de documentation officielle - le développement ultrarapide de ReactJS ne laisse aucune place à la documentation appropriée qui est un peu chaotique à présent, de nombreux développeurs l'apportant individuellement sans aucune approche systématique;
* React n'est pas avisé, ce qui signifie que les développeurs ont parfois trop de choix.
* Long temps à maîtriser, ce qui signifie que React JS nécessite une connaissance approfondie de la manière d’intégrer l’interface utilisateur dans le framework MVC.


#### Vue
**Les plus**
* HTML habilité. Cela signifie que Vue.js possède de nombreuses caractéristiques similaires à Angular, ce qui peut aider à optimiser la gestion des blocs HTML avec une utilisation de différents composants.
* Documentation détaillée Vue.js a une documentation très circonstanciée qui peut accélérer l’apprentissage des développeurs et gagner beaucoup de temps pour développer une application en utilisant uniquement les connaissances de base de HTML et de JavaScript.
* Adaptabilité. Il fournit une période de commutation rapide d’autres frameworks vers Vue.js en raison de la similitude avec Angular et React en termes de conception et d’architecture.
* Intégration impressionnante. Vue.js peut être utilisé à la fois pour la création d'applications d'une page et pour les interfaces Web d'applications plus difficiles. L'essentiel est que des composants interactifs plus petits puissent être facilement intégrés à l'infrastructure existante sans aucun impact négatif sur l'ensemble du système.
* Grande échelle. Vue.js peut aider à développer de très grands modèles réutilisables qui peuvent être créés sans temps supplémentaire, selon sa structure simple.
* Petite taille. Vue.js peut peser environ 20 Ko, tout en conservant sa vitesse et sa flexibilité, ce qui lui permet d’atteindre de bien meilleures performances que d’autres cadres.
* Popularité galopante. Tout le monde en parle, il est beau, il est intelligent, il est jeune, et gna gna gna.... bref, le gars énervant quoi.

**Les moins**
* Manque de ressources. Vue.js a toujours une part de marché relativement petite par rapport à React ou Angular, ce qui signifie que le partage des connaissances dans ce cadre en est encore à ses débuts. Cependant, la communauté est bien organisé et ce retards vis à vis de ses concurrent se réduit vite, notamment grâce à des dépôts comme [awesome-vue](https://github.com/vuejs/awesome-vue).
* Risque de trop de flexibilité. Parfois, Vue.js pouvait rencontrer des problèmes lors de l’intégration dans des gros projets et il n’existait pas encore de solutions possibles, mais ces solutions viendront très bientôt.
* Manque de documentation complète (en anglais). Cela conduit à une complexité partielle à certains stades de développement, néanmoins, de plus en plus de documents sont traduits en anglais.



### Outillage (dev/debug)
Angular arrive avec des outils de débuggage et de test déjà en place, mais les autres peuvent aussi les utiliser. Donc de ce point de vue, tous sont à la même enseigne. 
* Des outils dans le navigateur web pour le débuggage dynamique au runtime;
* Des outils de packaging du code pour compresser l'application et accelérer sont déploiement sur les navigateurs web;
* Des outils de tests automatique comme selenium ou [cypress](https://www.cypress.io/).


## Conclusion

Au vu des points discutés précédemment, on peut dresser le tableau suivant. Les étoiles étant là pour les départager, on évite au maximum les ex-æquos (même quand la différence est minime), ce classement n'est là que pour synthétiser les choses et faire pencher la balance vers le framework qui sera utilisé pour Regovar. Ces notes n'ont pas de valeur "qualitative".


| Fait | React | Angular | Vue |
| ---- | ----- | ------- | --- |
| Libre et Open-source | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Usage/popularité sur le web (Communauté) | :star: | :star: :star: :star: | :star: :star: |
| Usage en production | :white_check_mark: | :white_check_mark: | :white_check_mark: |
| Simplicité d'usage | :star: :star: | :star: | :star: :star: :star: |
| Courant dans les projets "bio-info" (échelle nationale) | :star: :star: | :star: :star: :star: | :star: |
| Connaissance au sein de l'équipe Regovar | :star: :star: :star: | :star: :star: | :star: |
| Capacité du framework | :star: | :star: :star: :star: | :star: :star: |
| Outillage (dev/debug) | :white_check_mark: | :white_check_mark: | :white_check_mark: |

|      | React | Angular | Vue |
| ---- | ----- | ------- | --- |
| **Total** | 9 | 12 | 9 |

Bien que très séduisant et prometteur, **Vue** souffre d'être le petit dernier arrivé. Sa communauté est moins grande, les projets moins nombreux et donc l'aide potentiel moins grande.

**React** pèche surtout par le fait qu'il ne permet pas de faire tout ce dont on aura besoin pour le développement d'une application web. Il faura alors faire appel a d'autres framework ou brique logiciel pour palier à ce qui manque et complexifiera le développement et la maintenance.

**Angular** est le plus gros et le plus complexe à prendre en main des 3 frameworks, mais il permet de tout faire, et sa popularité en fait d'office une référence auprès des bioinformaticiens. De fait, Angular est le plus souvent cité dans les offres d'emploi ou les papiers en bioinformatique.

CHOIX FINAL : Angular ou Vue ... :s

