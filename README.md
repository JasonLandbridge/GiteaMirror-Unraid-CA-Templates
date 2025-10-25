# Unraid CA Templates

This repository hosts Community Applications (CA) templates for Unraid that are maintained by RayLabsHQ. Each XML file in `templates/` describes how Unraid should deploy one of our container images, including port mappings, persistent storage, and the environment variables that unlock advanced features.

## Available Templates

- `templates/gitea-mirror.xml` – Deploys the Gitea Mirror application (`ghcr.io/raylabshq/gitea-mirror`). It exposes the web UI on port 4321, persists state in `/app/data`, optionally consumes custom CA certificates from `/app/certs`, and surfaces the key authentication, GitHub, Gitea, and scheduling variables.

## Using These Templates Locally

1. Enable **Docker Authoring Mode** in Unraid (`Settings → Docker`).
2. Clone or download this repository to a location that your Unraid server can read.
3. On the **Docker** tab choose **Add Container**, then switch to **Template repositories** and point Unraid at this folder, or manually paste the XML content into the **Advanced View** editor.
4. Adjust the template defaults (ports, paths, secrets) to suit your environment, then deploy.

## Publishing to Community Applications

If you intend to submit one of these templates to the public CA feed:

1. Confirm the `<TemplateURL>` in the XML points to the raw GitHub path on the `main` branch.
2. Ensure a public support location is referenced via `<Support>` (eg. GitHub Discussions).
3. Create or update the accompanying maintainer profile (`ca_profile.xml`).
4. Run through a clean install on an Unraid test system to validate default mappings and automated secret generation.
5. Submit the repository using the official CA submission form outlined in the [Docker FAQ](https://forums.unraid.net/topic/57181-docker-faq/) and monitor for any feedback from the CA maintainers.

## Maintainer

RayLabsHQ – https://github.com/RayLabsHQ

Contributions and bug reports are welcome. Open an issue or discussion in the respective application repository so we can keep the template and container behaviour aligned.
