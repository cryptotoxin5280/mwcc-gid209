# Local WordPress Container Setup

The purpose of this directory is to assist students with setting up a local development instance of WordPress and its database in a set of microservice containers.

## Install Dependencies

_These instructions assume that Apple macOS users already have [Homebrew](https://brew.sh/) installed._

1\. Install Git.

**Apple macOS:**

```bash
brew install git
```

**Microsoft Windows:**

```bash
winget install --id Git.Git --exact
```

2\. Install Podman.

**Apple macOS:**

```bash
brew install podman
podman machine init
podman machine start
```

**Microsoft Windows:**

```bash
winget install --id RedHat.Podman --exact
```

## Pull Down the WordPress Service Containers

1. From the command-line, navigate to the `wordpress-container` directory of this cloned repo.

2. Start the containers.

```bash
podman compose up -d
```

## Access WordPress

1\. Once the containers are running, open a web browser and navigate to:

```bash
http://localhost:8080
```

2\. The first time you visit the WordPress site, you'll be prompted to configure it.

Set the following fields, check the `Confirm use of weak password` box, and click `Install WordPress`.

| FIELD | VALUE |
| ---: | --- |
| **Site Title:** | GID209 |
| **Username:** | student |
| **Password:** | password |
| **Your Email:** | student@mwcc.edu |

3\. Click `Log In`.

You should now be logged into your local development WordPress site.

## 4. Stop the Containers

The WordPress containers can be stopped at any time via the following command:

```bash
podman compose down
```

## 5. Starting WordPress

After the intial container deployment, WordPress can be started up again by navigating to MWCC-GID209/wordpress-container and executing the following command:

```bash
podman compose up -d
```
