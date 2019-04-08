# Angress
<p>Creating a postgres through docker with ansible playbook</p>

**Ansible 2.7.9**
<br />

**Docker version 18.09.4**
<br />

**Postgres image: latest**
<br />

## Getting Started
<br />

<p>First step, open this file in your favourite editor</p>

<p>Set ports, the name and the docker's version</p>

```bash
 - hosts: localhost
   tasks: 
     - name: Init postgresql
       docker_container:
         name: postgresql
         image: postgres
         ports:
           - "5432:5432"
```
<p>Give the name of the database, username and the password</p>

```bash
  env:
           POSTGRES_USER: tucano
           POSTGRES_PASSWORD: foo
           POSTGRES_DB: cacatua
```
<p>Create a directory to bind the docker's directory</p>

```bash
    volumes: 
           - /tmp/postgres:/var/lib/postgresql/data
```
<br />

 <p>Use this command to run your playbook</p>
 
```bash
 ansible-playbook <file>.yml
 ```
 
 **Now make your changes and update this code to improve your abilities**
