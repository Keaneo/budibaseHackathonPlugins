# Giphy
A plugin for searching and embedding Giphy gifs into a budibase page.

Find out more about [Budibase](https://github.com/Budibase/budibase).

## Instructions

To build your new  plugin run the following in your Budibase CLI:
```
budi plugins --build
```

You can also re-build everytime you make a change to your plugin with the command:
```
budi plugins --watch
```

##NOTE: 
In order to bypass the Content Security Policy, we have to overwrite the nginx config file
To do this:
1. Navigate to the budibase installation
2. Open the docker-compose.yaml file
3. Edit line 79 to say: "image: nginx"
4. Run budibase, make sure the giphy plugin is built & refresh the page
