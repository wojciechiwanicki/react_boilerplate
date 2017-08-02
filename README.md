# React Boilerplate w VM
Podstawowy boilerplate Reacta w Vagrancie, używając:
- node
- nvm
- webpack

Vagrant Box: `ubunty/trusty64`

## Setup
1. Zainstaluj [VirtualBox](https://www.virtualbox.org/)
2. Zainstaluj [Vagrant](https://www.vagrantup.com/)
3. Sklonuj repozytorium
4. Przejdź do folderu z repozytorium:
```
vagrant up
vagrant ssh
cd /vagrant
```

### Dodatkowe kroki na Linuxie
```
sudo apt-get npm
npm install npm@latest -g
```

## Uruchomienie
Po `cd /vagrant`:
```
npm start
```

## TO_DO
### Project Structure

I have set up the application structure where the React development files are in the `app` directory and the final, complied files are output to the `public` directory. This can be changed to fit your projects needs. Just note that the changes would also need to be reflected in the `webpack.config.js` file.


### Running the Webpack Dev Server

To run the Webpack Dev Server, you will want to move into the aforementioned shared folder on your Vagrant server. If you haven't already, shell into your Vagrant server via the `vagrant ssh` command. From there, type `cd /vagrant`. Now that you're in the right location, you just need to run `npm start` to fire up the Webpack Dev Server.

Once you have the Webpack Dev Server up and running, you can jump over to your browser and visit `localhost:8881` and see that appication is running!

That's all there is to it. Now you have Node.js, NVM, React.js, Webpack, and PostCSS installed in a virtual machine and your local system environment is left untouched!

### Bundle the project for distribution

Running the Webpack Dev Server will not actually generate the output files. Instead it keeps and serves the resulting files from memory. When you're ready to generate the final output files for your project, run `npm run bundle`. This will generate everything into the `public` directory and you can distribute from there!
