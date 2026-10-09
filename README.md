# Unraid templates

Docker templates and icons for my Unraid server. To install one, copy its `.xml` to
`\\<server>\flash\config\plugins\dockerMan\templates-user\` **renamed to `my-<Name>.xml`**
(e.g. `my-ARTscale.xml`), then Docker > Add Container > pick it from Template.

Why the `my-` name matters: Unraid saves a container's settings as `my-<Name>.xml` in that same
folder. When it updates a container, it uses the first file there whose `<Name>` matches, in
alphabetical order, so a separate `artscale.xml` would win over `my-ARTscale.xml` and recreate
the container from the blank template, losing your settings. Saving the template as
`my-<Name>.xml` means Unraid edits that one file. If you already copied a template under its own
name, delete that copy after installing (keep the `my-` file).

- [solar-assistant-overlay](solar-assistant-overlay/): live dashboard for Solar Assistant
- [artscale](artscale/): self-hosted Tailscale control server (headscale) with a console for switching customer subnet routes on demand
