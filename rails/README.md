# Rails-MongoDB Playbook
Deploys a RoR application on Ubuntu 16.04 with Nginx, Passenger and MongoDB.

## Requirements Digital Ocean.

* One DO Droplet with Ubuntu 16.04 installed.
* Create the user 'deploy' on you instance with sudo privileges (https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-16-04).


## Configuration

* Install RVM role running the following line:
```sh
sudo ansible-galaxy install rvm_io.rvm1-ruby
```

* Create the file secrets.yml with the following values (Just replace everything between curly braces):
```sh
secret_key_base: {the value obtained after runing 'rake secret'}
git_repo: https://{github username}:{github password|token}@github.com/{company|profile}/{repo name}.git
server_name: {yourdomain.com}
app_name: {repo name}
```

* Edit the hosts file and add the IP address of your droplet on the value 'ansible_ssh_host'.

* Run your playbook
```sh
./ubuntu-rails.yml
```
