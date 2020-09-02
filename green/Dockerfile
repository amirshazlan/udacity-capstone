## Step 1: Create base image from nginx
FROM nginx

## Step 2: remove default nginx page
RUN rm /usr/share/nginx/html/index.html

## Step 3: Copy new index page to working directory
COPY index.html /usr/share/nginx/html