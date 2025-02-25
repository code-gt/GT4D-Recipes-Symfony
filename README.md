﻿# 🌟 TP : Créer une Application Symfony de Gestion de Recettes !

Bienvenue dans ce TP qui va mettre à l'épreuve tout ce que vous avez appris en Symfony jusqu'ici 🎉 ! **Votre mission** : concevoir une petite application web pour gérer des recettes de cuisine. Vous utiliserez vos connaissances pour connecter votre backend à une base de données et afficher les recettes sur une interface sympa et fonctionnelle. 👩‍🍳👨‍🍳

## 🎯 Objectifs pédagogiques
* **Consolider vos bases en Symfony** : maîtrise des contrôleurs, modèles, vues et interaction avec une base de données via les Repository.

* **Apprendre à structurer une application** : organiser les fichiers et données pour un projet clair et efficace.

* **Créer une application fonctionnelle** : relier vos données de la base au frontend avec Twig et Symfony.

* **S'immerger dans un workflow pratique** : reproduire des étapes clés comme dans un vrai projet !

## 📝 Consignes générales

Vous avez **6 à 7 heures** pour réaliser un mini-site permettant de :

1. Lister toutes les recettes dans une page.
2. Afficher les détails d’une recette individuelle.
3. Ajouter des catégories de recettes et les associer à des recettes.

Pas d’inquiétude : chaque étape est guidée et expliquée dans les consignes ci-dessous ! 🚀

## 🛠️ Étapes du TP

**1. Préparer le projet**

* Créez un nouveau projet Symfony avec l’option `--webapp`.

* Configurez votre base de données dans le fichier `.env.local`. Exemple :

```dotenv
DATABASE_URL="mysql://root@127.0.0.1:3306/recipes_db?serverVersion=8.0.32&charset=utf8mb4"
```

* Testez votre configuration avec :

```dotenv
symfony serve
```

Vérifiez que tout fonctionne bien. ✅ 

**2. Créer les Entités**

* Une entité `Recipe` avec les champs suivants :

| Champ      | Type          | Description                          |
|------------|---------------|--------------------------------------|
| name       | String        | Nom de la recette                    |
| description| Text          | Description détaillée de la recette  |
| created_at | Datetime      | Date de création                     |


* Une entité `Category` avec les champs :

| Champ      | Type          | Description                          |
|------------|---------------|--------------------------------------|
| name       | String        | Nom de la catégorie                  |

* Relation entre `Recipe` et `Category` : Une recette appartient à une catégorie, mais une catégorie peut avoir plusieurs recettes.

**3. Créer la Base de Données**

* Générez les migrations pour vos entités
* Appliquez-les

(Pour ces 2 étapes, retrouvez les commandes Symfony associées)

**4. Le Routing et les Contrôleurs**

* **Page d'accueil** : Liste toutes les recettes.

* **Page d'une recette** : Affiche les détails d'une recette sélectionnée.

* **Page d'une catégorie** : Liste toutes les recettes d'une catégorie.

* Utilisez les Repository pour récupérer les données de la base et les envoyer aux vues Twig.

⚠️ Il vous manque une connaissance pour faire les pages descriptif d'**un** objet. Il faut voir ce que sont les `route parameters` : [https://symfony.com/doc/current/routing.html#route-parameters](https://symfony.com/doc/current/routing.html#route-parameters)

**5. Les Vues Twig**

* Créez une structure HTML simple pour :

    * Lister toutes les recettes (nom, catégorie, date).

    * Afficher les détails d'une recette (nom, description, catégorie).

    * Afficher les recettes d’une catégorie.

* Intégrez des liens entre les pages pour naviguer dans le site.

## 💡 Exemple de fonctionnalités attendues
1. **Page d'accueil :**

* URL : `/`
* Liste toutes les recettes avec leur nom et leur catégorie.

2. **Détail d'une recette :**

* URL : `/recipe/{id}`
* Affiche toutes les informations d'une recette.

3. **Recettes par catégorie :** 

* URL : `/category/{id}`
* Affiche toutes les recettes associées à une catégorie.

## ✅ Livrables

À la fin de ce TP, vous devriez avoir :

1. Une base de données fonctionnelle avec des données de test.

2. Un site Symfony minimaliste mais opérationnel pour gérer des recettes.

3. Une structure de projet claire et cohérente.

## 🏁 Mot de fin
Ce TP est votre premier vrai challenge en Symfony, alors donnez le meilleur de vous-même ! 💪 Profitez de l’occasion pour poser des questions et explorer les docs officielles si besoin. Bon courage et surtout… amusez-vous ! 🍲
