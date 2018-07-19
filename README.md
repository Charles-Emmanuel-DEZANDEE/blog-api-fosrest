blog-api-fosrest
================

A Symfony project created on February 15, 2017, 10:40 am.

parametrer le parameter.yaml avec les infos de connection de la base de données.

ensuite faire :
composer install
php bin/console doctrine:database:create
php bin/console doctrine:schema:update --force

alimenter la base avec postman en post sur [chemin du projet]/articles

{
	"title": "Le titre de mon article ",
	"content": "Le contenu de mon article.",
	"author": {
		"fullname": "Sarah Khalil",
		"biography": "Ma biographie."
	}
}
{
	"title": "Le titre de mon deuxieme article ",
	"content": "Le contenu de mon deuxieme article.",
	"author": {
		"fullname": "Sarah Khalil",
		"biography": "Ma biographie."
	}
}

modif :
avec put et le chemin : /articles/1 (id)
{
	"title": "Le titre de mon article est modifié ",
	"content": "Le contenu de mon deuxieme article est modifié."
}

suppression :
avec delete et le chemin : /articles/1 (id)

