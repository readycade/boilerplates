### Vagrant is responsible for creating and supporting virtual development environments via virtual machines. Furthermore, vagrant-digitalocean, a Vagrant provider plugin, enables us to manage DigitalOcean droplets with ease. It offers several features like:

    Power on/off droplets
    Create/ destroy droplets
    Rebuild droplets
    Create an SSH key for authentication
    Set up a new user account while creating a droplet

#### Install the Vagrant provider plugin with the following command:
```
vagrant plugin install vagrant-digitalocean
```

#### After installation, it is time to configure our project to use Vagrant DigitalOcean. The configuration requirements include:

We have to specify the override.ssh.private_key_path in order to enable authentication via the Droplet. Additionally, the provider creates a new DigitalOcean SSH key with the public key that is the private_key_path with a .pub extension.
Then, mention the DigitalOcean Personal Access Token at provider.token. We can find this in the control panel under the Apps & API section.

After we create the Vagrantfile with the corresponding configuration attributes. We have to create a new droplet with the following command:
```
vagrant up –provider=digital_ocean
```

The above command creates a new droplet, sets up the SSH key for authentication, and creates a new user account.

#### Alternatively, we can install Vagrant DigitalOcean via Bundler as seen here:

    To begin with, install Bundler version 1.7.9

    sudo gem install bundler -v '1.7.9'

    Then, install vagrant-digtialocean dependencies as seen below:

    bundle _1.7.9_ install

    Next, try running the following command to ensure it is working:

    bundle _1.7.9_ exec vagrant digitalocean-list images

    Finally, we can run the following command to test if it is working:

    bundle _1.7.9_ exec rake test
