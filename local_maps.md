1. download local North American maps (.pbf) https://download.geofabrik.de/north-america.html  US South for smallest (https://download.geofabrik.de/north-america/us-south-latest.osm.pbf)
2. WSL
3. ```bash
   sudo apt update -y
   sudo apt install postgresql postgresql-contrib -y
   sudo -u postgres -i
   createuser openstreetmap -s -P
   createdb -E UTF8 -O openstreetmap openstreetmap 
   createdb -E UTF8 -O openstreetmap osm_test
   createdb -E UTF8 -O openstreetmap osm
   shared_buffers = 512MB
   bgwriter_delay = 2000ms
   ./setup_docker.sh
   sudo usermod -aG docker $USER
   git clone git://git.openstreetmap.org/rails.git
   sudo apt install ruby-full build-essential ruby-dev -y
   ruby --version
   gem --version
   echo 'export GEM_HOME="$HOME/.gem"' >> ~/.bashrc
   echo 'export PATH="$HOME/.gem/bin:$PATH"' >> ~/.bashrc
   source ~/.bashrc
   sudo apt-get install -y libxml2-dev libxslt-dev build-essential
   # Install Rails 2.3.8 (using ~> matches 2.3.8 and any tiny releases like 2.3.8.1)
   gem install rails -v '~> 2.3.8'
   gem install rack -v '~> 1.1.0'
   gem install libxml-ruby -v '>= 1.1.1'
   gem install timecop
   gem install oauth
   https://github.com/openstreetmap/openstreetmap-website.git
   ```
4.
