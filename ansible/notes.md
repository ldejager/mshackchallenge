# Setup SP

```
az ad sp create-for-rbac --name TeamBlue --password 'somepassword'
```

# Delete SP

```
az ad sp delete --id [spnid]
```

# Python pip requirements

Install python virtual environment as there are loads of packages that needs to be installed;

```
pip install virtualenv
```

Create a virtual environment;

```
virtualenv -p python3 venv
```

Activate the virtual environment;

```
source venv/bin/activate
```

Install `ansible[azure]``

```
pip install 'ansible[azure]'
```

# Run ansible

```
ansible-playbook setup.yaml
```

# Get kubectl creds

```
az aks get-credentials --resource-group TeamBlueResourceGroup --name TeamBlue
```
