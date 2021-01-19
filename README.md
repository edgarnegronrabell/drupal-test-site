# Drupal Test Site
Testing how to setup a Drupal environment with Docker containers.

## Drupal Local Environment

To get the Drupal environment running:

1. Run ```docker build -t drupal-test-site:latest .``` to build your Docker Image.
2. Run  ```docker-compose up -d``` to start the local environment. 

With your environment running, visit http://localhost and see the Drupal site.


## Installing Drupal

In order to automate Drupal's installation, install with: 

```docker-compose exec drupal bash -c 'drush site:install minimal --db-url="mysql://drupal:$DRUPAL_DATABASE_PASSWORD@$DRUPAL_DATABASE_HOST/drupal" --site-name="Drupal Test Site" -y'```