Ansible Role for Fisheye
========================

[![Build Status](https://travis-ci.org/alvistack/ansible-role-fisheye.svg?branch=master)](https://travis-ci.org/alvistack/ansible-role-fisheye)
[![GitHub tag](https://img.shields.io/github/tag/alvistack/ansible-role-fisheye.svg)](https://github.com/alvistack/ansible-role-fisheye)
[![GitHub license](https://img.shields.io/github/license/alvistack/ansible-role-fisheye.svg)](https://github.com/alvistack/ansible-role-fisheye/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/galaxy-alvistack.fisheye-blue.svg)](https://galaxy.ansible.com/alvistack/fisheye)

Ansible Role for Atlassian Fisheye Installation.

Requirements
------------

This role require Ansible 2.4 or higher.

This role was designed for Ubuntu 16.04/14.04 or CentOS 6/7.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>fisheye_catalina</td>
<td>no</td>
<td><code>/opt/atlassian/fisheye</code></td>
<td></td>
<td>Location for the Fisheye installation directory</td>
</tr>
<tr class="even">
<td>fisheye_connector_port</td>
<td>no</td>
<td><code>8060</code></td>
<td></td>
<td>Fisheye Apache Tomcat connector port</td>
</tr>
<tr class="odd">
<td>fisheye_context_path</td>
<td>no</td>
<td><code>~</code></td>
<td></td>
<td>Context path for Fisheye installation</td>
</tr>
<tr class="even">
<td>fisheye_group</td>
<td>no</td>
<td><code>daemon</code></td>
<td></td>
<td>Name of the group that should own the file</td>
</tr>
<tr class="odd">
<td>fisheye_home</td>
<td>no</td>
<td><code>/var/atlassian/application-data/fisheye</code></td>
<td></td>
<td>Location for the Fisheye home directory</td>
</tr>
<tr class="even">
<td>fisheye_jvm_maximum_memory</td>
<td>no</td>
<td><code>768m</code></td>
<td></td>
<td>Fisheye JVM maximum memory usage</td>
</tr>
<tr class="odd">
<td>fisheye_jvm_minimum_memory</td>
<td>no</td>
<td><code>384m</code></td>
<td></td>
<td>Fisheye JVM minimum memory usage</td>
</tr>
<tr class="even">
<td>fisheye_jvm_support_recommended_args</td>
<td>no</td>
<td><code>-Datlassian.plugins.enable.wait=300</code></td>
<td></td>
<td>Atlassian Support recommended JVM arguments</td>
</tr>
<tr class="odd">
<td>fisheye_owner</td>
<td>no</td>
<td><code>daemon</code></td>
<td></td>
<td>Name of the user that should own the file</td>
</tr>
<tr class="even">
<td>fisheye_proxy_name</td>
<td>no</td>
<td><code>~</code></td>
<td></td>
<td>Domain name for working with reverse proxy</td>
</tr>
<tr class="odd">
<td>fisheye_scheme</td>
<td>no</td>
<td><code>~</code></td>
<td><ul>
<li><code>http</code></li>
<li><code>https</code></li>
</ul></td>
<td>Scheme for working with reverse proxy</td>
</tr>
<tr class="even">
<td>fisheye_server_port</td>
<td>no</td>
<td><code>8059</code></td>
<td></td>
<td>Fisheye Apache Tomcat server port</td>
</tr>
<tr class="odd">
<td>fisheye_url</td>
<td>no</td>
<td><code>https://downloads.atlassian.com/software/fisheye/downloads/fisheye-4.5.0.zip</code></td>
<td></td>
<td>URL for download archive</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: fisheye
          fisheye_proxy_name: "fisheye.example.com"
          fisheye_scheme: "http"
          fisheye_owner: "fisheye"
          fisheye_group: "fisheye"

License
-------

-   Code released under [Apache License 2.0](https://github.com/alvistack/ansible-role-fisheye/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

