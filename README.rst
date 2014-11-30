Vince's ancient Perl programming blog. This is a baked-down static HTML version
of the site that previously ran on a custom HTML::Mason based site. Someday I
might revive it, but for the moment, it is maintained only because `cool URLs
don't change <http://www.w3.org/Provider/Style/URI.html>`_.

Deployment now uses Ansible.

    ansible-playbook -i <host_inventory> deploy.yml

The Ansible host must declare the following host vars:

* website_root - directory where sites are installed
* website_user - owner of site files
* website_group - group owner of site files
* http_service - apache2 or nginx

For the moment, the only virtual host config provided is for Apache 2.4.
