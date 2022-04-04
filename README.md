# DevOps assignment

Minimal environment with `keycloak` and a custom `python` app behind
`nginx`, in `docker`, orchestrated with `docker-compose`.

## Development

Start the environment: `docker-compose up -d`

Create a new user in the `keycloak` admin: http://localhost/keycloak/admin

**_Tip_**: add credentials for `keycloak` and `postgres` in a `.env` file.

### Endpoints

1. http://localhost/: "Hello world!" index page
1. http://localhost/login: redirects to `keycloak` auth
1. http://localhost/auth/callback: `keycloak` callback after login

### Known issues

1. The `python` app builds correctly but does not work in production mode
only in development mode.
1. The app's `login` is broken.
1. Connections to the `keycloak` endpoints fail with "502 Bad Gateway".
1. The `python` app's `Dockerfile` does not follow best practices.

### Fixed issues

* The /app login endpoint was broken because of a typo (/loogin) in the app.py 

* The Keycloak endpoints were failing since the nginx redirects was configured to reach the service with the wrong port instead of 8080 it was mentioned 8090.

_Add On_

 As an improvement we could also reduce the length of nginx file but moving the server block out to different file from the main config file.

 As a common best practices it is wise to move the gunicorn paramenter as a separate module so the issue during cmd and entrypoint will be completed resolved in future.


### Notes

1. Any `git` commits should follow the
[conventional commits](https://www.conventionalcommits.org/en/v1.0.0/)
specifications.
1. `git` formatted patches are preferred.


## <font color = "red"> Follow-Me </font>

[![Portfolio](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/premkumar-palanichamy)

<p align="left">
<a href="https://linkedin.com/in/premkumarpalanichamy" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="premkumarpalanichamy" height="25" width="25" /></a>
</p>

[![youtube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCJKEn6HeAxRNirDMBwFfi3w)