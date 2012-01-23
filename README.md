# Template for creating Vagrant projects with Bundler and chef-solo

## Install

Clone this repository

    $ git clone https://textgoeshere@github.com/kapoq/vagrant-chef-solo-project-template.git

Delete the git history (you'll want your own) by deleting the `.git` folder

    $ # rm -rf .git <-- steady now, partner

Optionally setup `rvm`

    $ cp .rvmrc.example .rvmrc
    $ . .rvmrc

Install the gems

    $ bundle

Initialize the Vagrant box (defaults to lucid32)

    $ vagrant init
    
## Usage

Edit `Vagrantfile`

Install a cookbook   

    $ knife cookbook github install fnichol/chef-jenkins -c solo.rb 

Provision the box (assuming the box is up)

    $ vagrant provision
