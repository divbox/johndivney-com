# JohnDivney.com Drupal code

This is the drupal code that powers johndivney.com.

## Local environment

Make sure you have Docker installed, then run the following:

    1. Bulid the local docker image:

      ```
      docker build -t johndivney-com:latest .
      ```

    2. Start local environment with docker-compose:

      ```
      docker-compose up -d
      ```

After environment starts up you can visit http://localhost:88

### Installing Drupal

Install using Drush:

  ```
  docker-compose exec drupal bash -c 'drush site:install minimal --db-url="mysql://drupal:$DRUPAL_DATABASE_PASSWORD@$DRUPAL_DATABASE_HOST/drupal" --site-name="My Drupal Site" -y'
  ```


