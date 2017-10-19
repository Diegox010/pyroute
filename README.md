# WIP:
## Setup dev environemnt

 1. Clone this repo, we use `develop` branch for development.
 2. Install pipenv on global python from your machine `pip install pipenv`
 3. Run `pipenv --three`
 4. Run `pipenv install '-e .' --dev`
 5. Go to your *~/.bashrc* or *~/.zshrc*
 6. Edit the file and issue these commands to setup an alias
 7. Restart your terminal


**This works with zsh shell:**
```
# ——— PYROUTE ——— #
export PYROUTEPATH=$HOME/Projects/pyroute

pyroute_activate(){
    ssh-add ~/.ssh/id_rsa
    cd $PYROUTEPATH
    pipenv shell
}
alias pyrouteenv=pyroute_activate
```

* Create a test folder in different location than pyroute code

* Create a subfolder named `config`

* Create a `config.json` file, copy and save the following to it:

```
{
    "tests": {
        "path": [
            "tests/sprint01_features"
             ],
        "preffix": "test_",
        "data": "$PATH"
    },
    "modules": {
        "REST": {
            "timeout": "50000",
            "endpoint": "http://google.com",
            "reset_headers": "True",
            "otro_param": "here"
        },
        "SSH": {
            "computer": "computer_Service"
        }
    }

}
```

* Create a `pyroute_tests_folder` folder

* Create a file named `features.py`

* From this folder you're going to run `pyroute run` command