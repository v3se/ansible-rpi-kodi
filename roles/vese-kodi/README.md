vese kodi
=========

This role installs and configures [Kodi](https://kodi.tv/) Media Center to Raspberry Pi 4 running Raspberry Pi OS. It's utilizing [kodi-standalone](https://github.com/graysky2/kodi-standalone-service) to run as a systemd service. This role also installs addons from Github. You can install additional addons by adding the Github repository links to defaults/main.yml.

Role Variables
--------------

| Name                           | Description                                                                                |
|--------------------------------|--------------------------------------------------------------------------------------------|
| vese_kodi_local_git_path       | Path where the kodi-standalone repo will be cloned. Defaults to the Ansible user home dir. |
| vese_kodi_standalone_repo      | URL to the kodi-standalone repo                                                            |
| vese_kodi_standalone_version   | Version of the kodi-standalone                                                             |
| vese_kodi_packages             | Packages to be installed including Kodi itself                                             |
| vese_kodi_inputsreamhelper_url | URL to inputstreamhelper Github repo                                                       |
| vese_kodi_plugins              | List of kodi plugins that will be clone from Github to the addons dir                      |
| vese_kodi_home_dir             | Defaults to /var/lib/kodi                                                                  |
| nordvpn_token             | Nordvpn token to login to your account                                                                  |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: vese-kodi, become: yes }
