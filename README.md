# ------------------------------------
# Docker alias and function
# ------------------------------------

alias dcom="docker-compose"

# Run rails console
alias dcom-console="docker-compose run web rails console"

# Run shell
alias dcom-bash="docker-compose run web bash"

# Run rails migrations
alias dcom-migrate="docker-compose run web rake db:migrate"

alias dcom-create="docker-compose run web rake db:create"

alias dcom-seed="docker-compose run web rake db:seed"

alias dcom-drop="docker-compose run web rake db:reset"

# Run bundler
alias dcom-bundle="docker-compose run web bundle install"

# Run rails with service ports to use Pry
alias dcom-pry="docker-compose run --service-ports web"

# Get images
alias di="docker images"

#export container ID
alias dl="docker ps -l -q"

# Get container process
alias dps="docker ps"

# Get process including stopped container
alias dpa="docker ps -a"

# Stop all containers
dstop() { docker stop $(docker ps -a -q); }

#Start docker machine
alias dms="docker-machine start default"

#Stop docker machine
alias dmd="docker-machine stop default"
