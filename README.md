# scala-web-sbt-spring-thyme-secure-des-encrypt-scrypt-encoded

## Description
A springboot secure web app with thymeleaf support.
Three roles are defined; USER, ADMIN, and SUPER. All roles
can access pages `/home`, `/login`, and `/about`. Only USER
can access `/user` and ADMIN only `/admin` whereas SUPER can
navigate to either and have its own `/super`. Each role
has an action USER=VIEW ONLY, ADMIN=READ/WRITE, SUPER=CREATE.
All password are encrypted with DES and encoded with scrypt
to insure strong passwords.

SALT is the
mixing of the original text with a secret key.
It is considered more secure to store the
SALT then the encrypted original text, however
this can still be cracked with rainbow tables.

## Tech stack
- scala
- sbt
  - springboot
  - thymeleaf
  - bootstrap
  - jquery
  - datatable

## Docker stack
- openjdk:8-jre-alpine

## To run
`sudo ./install.sh -u`
Available at http://localhost
- Login with id: user and password: pass
- Login with id: admin and password: pass
- Login with id: super and password: pass

## To stop (optional)
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`
