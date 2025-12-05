# Architecture de l'application MonkeyFinderHybrid
L'application MonkeyFinderHybrid est construite en utilisant une architecture MVVM (Model-View-ViewModel) pour séparer les préoccupations et faciliter la maintenance du code. Voici une vue d'ensemble de l'architecture de l'application :
1. **Modèle (Model)** :
       - Le modèle représente les données de l'application et la logique métier. Dans MonkeyFinderHybrid, le modèle inclut des classes telles que `Monkey`, qui contient les propriétés des singes (nom, espèce, image, etc.), et des services de données qui gèrent la récupération des informations sur les singes à partir d'une source de données (API, base de données locale, etc.).
       
2. **Vue (View)** : 
       - La vue est responsable de l'affichage de l'interface utilisateur et de la présentation des données. Dans MonkeyFinderHybrid, les vues sont construites à l'aide de XAML et incluent des pages telles que `MonkeyListPage` et `MonkeyDetailPage`, qui affichent respectivement la liste des singes et les détails d'un singe sélectionné.
3. **Modèle de Vue (ViewModel)** :
       - Le modèle de vue agit comme un intermédiaire entre le modèle et la vue. Il gère la logique de présentation et les interactions utilisateur. Dans MonkeyFinderHybrid, les ViewModels tels que `MonkeyListViewModel` et `MonkeyDetailViewModel` contiennent des propriétés et des commandes qui lient les données du modèle aux éléments de la vue, permettant ainsi une interaction fluide.
4. **Services** :
       - L'application utilise également des services pour gérer des fonctionnalités spécifiques telles que la navigation, la gestion des données, et les interactions avec des API externes. Ces services sont injectés dans les ViewModels pour promouvoir la réutilisabilité et la testabilité du code.
5. **Navigation** :
       - La navigation entre les différentes pages de l'application est gérée par un service de navigation qui permet de passer d'une vue à une autre tout en maintenant l'état de l'application.
           