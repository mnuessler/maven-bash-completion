# Maven Bash Completion

Maven by default does not distribute with a Bash auto completion script, only [a very simple guide](http://maven.apache.org/guides/mini/guide-bash-m2-completion.html) is provided. This script gives you more to help your daily Maven build.

## Installation

1. Download bash_completion.bash and save it to any place you want, like *~/.maven_bash_completion.bash*.
2. Make your login shell load the script automatically by adding the line below to *~/.bash_profile* (note the space after dot):  
`. ~/.maven_bash_completion.bash`

An example install as a one-line command line call for Debian and other distro is

`sudo wget https://raw.github.com/juven/maven-bash-completion/master/bash_completion.bash --output-document /etc/bash_completion.d/mvn`

Example install for MacOS X using the [Homebrew](http://brew.sh/) package manager:

1. `brew tap homebrew/completions` (add Git repository with completions to list of formulae, if not already done)
2. `brew install maven-completion` (install maven-completion formula)

## Usage

To list common lifecycle phases:  
`$ mvn [TAB][TAB]` (list all common used lifecycle phases)  
`$ mvn cl[TAB][TAB]` (complete to 'clean')  

To list prefix of common used plugins:  
`$ mvn ar[TAB][TAB]` (complete to 'archetype:')  
`$ mvn depe[TAB][TAB]` (complete to 'dependency:')  

To list available goals for common used plugins:  
`$ mvn help:[TAB][TAB]` (list all available goals of maven-help-plugin)  
`$ mvn dependency:[TAB][TAB]` (list all available goals of maven-dependency-plugin)  

To list available options:  
`$ mvn -[TAB][TAB]`  

To list -D options (like -DskipTests):  
`$ mvn -D[TAB][TAB]`  

To list available profiles (from settings.xml and pom.xml):  
`$ mvn -P [TAB][TAB]`  
`$ mvn -P myapp-core,[TAB][TAB]` (multiple profles supported) 

To list simple reactor projects:  
`$ mvn -pl [TAB][TAB]`  
`$ mvn -pl myapp-core,[TAB][TAB]`  
`$ mvn -rf [TAB][TAB]`
