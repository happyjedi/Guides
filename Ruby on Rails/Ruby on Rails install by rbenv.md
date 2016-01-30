# Ruby on Rails Installation by [rbenv](https://github.com/rbenv/rbenv.git)

1) Create folder .rbenv in home user repository, download rbenv source and compile it
     
    $ mkdir ~/.rbenv 
    $ git clone https://github.com/rbenv/rbenv.git ~/.rbenv
    $ cd ~/.rbenv && src/configure && make -C src
    
2) Export environment variables
     
    $ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
    $ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
    $ source ~/.bash_profile
    
    or if you have .bashrc
    
    $ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
    $ echo 'eval "$(rbenv init -)"' >> ~/.bashrc
    $ source ~/.bashrc
    
3) Initialize rbenv
    
    $ rbenv init
    
4) Install dependencies
    
    $ sudo apt-get install autoconf bison build-essential libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libncurses5-dev libffi-dev libgdbm3 libgdbm-dev
    
5) Install ruby (version 2.2.2)
    
    $ git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
    $ rbenv install 2.2.2
    $ rbenv global 2.2.2
    
6) Check ruby installation by 
     
    $ ruby -v
    $ irb  ## for ruby console
    
7) Just add this to your home directory in <home_directory>/.gemrc file if you wouldn't install documents for Gems
    
    $ echo 'gem: --no-document # skip installation of all documentation' >> ~/.gemrc
    
    Or add these to skip either ri or rdoc documentation for old version of ruby
    
    $ echo 'gem: --no-ri' >> ~/.gemrc
    $ echo 'gem: --no-rdoc' >> ~/.gemrc
    
8) Install Ruby on Rails framework
    
    $ gem install rails -v '4.2.3' --no-document
    
