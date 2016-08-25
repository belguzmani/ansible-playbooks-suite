# Setup

* Install RVM role running the following line:

    sudo ansible-galaxy install rvm_io.rvm1-ruby

* Create the file secrets.yml with the following values:

    secret_key_base: <the value obtained after runing 'rake secret'>
    git_repo: https://<github username>:<github password|token>@github.com/<company|profile>/<repo name>.git
    server_name: <yourdomain.com>
    app_name: <repo name>