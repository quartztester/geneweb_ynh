## Access control

GeneWeb has no built-in user system in this package: neither daemon asks for a login. Who can reach what is decided by YunoHost permissions:

- `geneweb` (main URL): browsing the bases. Default `visitors` = fully public. Change it in the webadmin (Applications → geneweb → Permissions) if the data should not be public.
- `geneweb.gwsetup` (`<path>/gwsetup`): create bases, import and export GEDCOM, edit base settings. Restricted to `admins`.

## Importing a GEDCOM file

1. Log in to the YunoHost portal as an admin.
2. Open `https://your.domain/geneweb/gwsetup/`.
3. Create a base (or pick an existing one) and use "Import from GEDCOM" / the `ged2gwb` form.
4. If the new base does not appear in the browsing interface, restart the service: `sudo systemctl restart geneweb`.

## Data location

Bases live in `/home/yunohost.app/<app>/bases` (`<name>.gwb` directories plus `<name>.gwf` config files). They are included in YunoHost app backups. Logs are in `/var/log/<app>/`.
