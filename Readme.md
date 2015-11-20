
# vagrant-python-lambda-local

## Setup

- pyenv
- virtualenv
- python-lambda-local
- lambda-uploader

## Usage

- Edit Vagrantfile (ip, vm_name, synced_folder)
- Edit python version : ansible/site.yml#pyenv_python_version
- vagrant up
- vagrant ssh (or vagrant 192.168.200.60 default settings)
- Set AWS Credentials (ex. ~/.aws/credentials)
- cd your lambda directory or create new
- execute lambda (aliased 'python-lambda-local -f lambda_handler lambda_function.py event.json')
- execute lambda-uploader

--------------------------------------------------------
