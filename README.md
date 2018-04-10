# Problem with Pydio

This repository contains the Docker infrastructure for creating a fresh install of Pydio 8.0.2

This is supposed to be supplemental for the forum thread at https://forum.pydio.com/t/uploader-form-retrieval-of-config-yields-empty-response

## Usage

To run this thing with docker-compose you'll need to add two folders:
- certs
    - Insert all the certificates for the SSL server here
- private_key
    - Insert the private key for the server certificate here

and you'll have to edit the "pydio.conf" file and replace the certificate paths so that it will match your filenames (lines 21, 24 and 27).

Then you should be able to run this thing using `docker-compose up -d --build`