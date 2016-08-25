# Rails-MongoDB Playbook
Deploys a RoR application on Ubuntu 16.04 with Nginx, Passenger and MongoDB

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
app_name: {repo name>
```
