Cloudlens agent installation ansible role
=========

Requirements
------------
The role works on both windows and linux distributions hosts. It will automatically detect the OS type and run the script accordingly. For linux distributions, docker must be installed.

Role Variables
--------------

| Variable                | Required | Default | Choices                   | Comments                                 |
|-------------------------|----------|---------|---------------------------|------------------------------------------|
| project_key             | yes      |         |                           | Project key available in project overview |
| server_ip               | yes      |         |                           | kubernetes cluster ip               |
| accept_eula             | yes      | false   | true, false               | must be true for the script to run    |
| ssl_verify              | yes      |         | "true", "false"           | "true" if sensor should use ssl          |
| uninstall               | yes      | false   | true, false               | true if script should uninstall sensor |
| handle_docker_unsecure_registeries | yes |     | true, false           | if true, script will add the server ip in docker's unsecure register - only for linux |
| path_to_ca              | no       |         |                           | path to the security certificate - only linux |
| auto_update             | yes      |         | "true", "false"           | "true" if sensor should auto update - windows only |
