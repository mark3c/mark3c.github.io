# my mark3c.io

[Markdown: Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)  
[Markdown: Working with advanced formatting](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting)

## Create GitHub Pages

[GitHub Pages](https://pages.github.com/)

1. Create a repository named username.github.io Public
2. `git clone https://github.com/username/username.github.io`
3. `cd username.github.io`  
`echo "Hello World" > index.html`
4. `git add --all`  
`git commit -m "Initial commit"`  
`git push -u origin main`
5. visit <https://username.github.io/>

> Hello World

## Create page with Jekyll

[Jekyll on Windows](https://jekyllrb.com/docs/installation/windows/)  
[GitHub Pages Documentation](https://docs.github.com/en/pages)

### Install

`sudo apt-get update -y && sudo apt-get upgrade -y`

#### 1. Install Git

`sudo apt-get install git`

#### 2. Install Ruby from BrightBox

`sudo apt-add-repository ppa:brightbox/ruby-ng`  
`sudo apt-get update`  
`sudo apt-get install ruby2.7 ruby2.7-dev build-essential dh-autoreconf`  
~~`sudo apt-get purge --auto-remove ruby`~~

`ruby -v`  
>ruby 2.7.5p203 (2021-11-24 revision f69aeb8314) [x86_64-linux-gnu]

`gem -v`
>3.1.12

#### 3. Update gem

[rubygems](https://rubygems.org/rubygems/rubygems-3.4.10.zip)  
`ruby ./rubygems-update-3.4.10/setup.rb`  
`gem -v`
>3.4.10

`gem sources --add <https://gems.ruby-china.com/> --remove <https://rubygems.org/>`  
`gem sources -l`
>\*\*\*CURRENT SOURCES\*\*\*  
<https://gems.ruby-china.com/>

`gem update --system`

#### 4. Install Jekyll

`gem install jekyll bundler`  
`jekyll -v`
>jekyll 4.3.2

`bundle config mirror.<https://rubygems.org> <https://gems.ruby-china.com>`

### Create
