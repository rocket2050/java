# Ansible Role: Java

Installs Java for RedHat/CentOS linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values:

    # The defaults provided by this role are specific to each distribution.
    java_packages:
      - java-1.7.0-openjdk

Set the version/development kit of Java to install, along with any other necessary Java packages.

    java_home: ""

If set, the role will set the global environment variable `JAVA_HOME` to this value.

## Dependencies

None.

## Example Playbook (using default package, usually OpenJDK 7)

    - hosts: centos 
      roles:
        - java

## Example Playbook (install OpenJDK 7)

For RHEL / CentOS:

    - hosts: centos
      roles:
        - role: java
          when: "ansible_os_family == 'RedHat'"
          java_packages:
            - java-1.7.0-openjdk

## License

MIT / BSD

## Author Information

www.opstree.com

blog.opstree.com
