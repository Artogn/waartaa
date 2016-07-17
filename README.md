# waartaa

A web IRC client written on top of React and Pyramid. It is aimed towards being an intuitive, collaborative IRC client across
multiple devices of the user along with centralized logging.

## System dependencies

```
# Dependency for crossbar
sudo dnf install -y libsodium libsodium-devel
```

## Development

1. Install the virtualenvwrapper package  
``sudo dnf install python-virtualenvwrapper``

2. Create a virtualenv  
``mkvirtualenv waartaa``

3. Install the required packages  
``pip install -r dev_requirements.txt``

4. Create authentication token to authenticate via iddev.fedorainfracloud.org  
``oidc-register --debug https://iddev.fedorainfracloud.org/ http://localhost:6543``

   Replace httplib2's own ca cert file (to adjust as needed):  

   ``
   cp /etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem
        ~/.virtualenvs/waartaa/lib/python2.7/site-packages/httplib2/cacerts.txt
   ``

   Copy the client-id to oidcHelpers.jsx to ``waartaa/client/app/helpers/oidcHelpers.jsx``  

5. Run the pyramid development server  
``pserve development.ini``

6. Move to the waartaa client folder in another window  
``cd waartaa/client/``

7. Start the server  
``npm start``

## Contribute

1. Setup and run **waartaa** locally.
2. Report bugs or submit feature requests at https://github.com/waartaa/waartaa/issues/new.
3. Feel free to pick up open issues from https://github.com/waartaa/waartaa/issues?state=open. Don't hesitate to ask for help.


## Comunicate

1. Mailing list: https://groups.google.com/forum/#!forum/waartaa
1. IRC: **#waartaa** on Freenode



[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/waartaa/waartaa/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

