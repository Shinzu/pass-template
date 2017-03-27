# pass-template
Template for a pass (https://www.passwordstore.org/) git repo

This repo contains some simple git hooks to automate some local task for a [pass](https://www.passwordstore.org/) git repo.

## Usage

first clone this repo to a directory where you want to use as password store:

    git clone git@github.com:Shinzu/pass-template.git ~/.password-store

change into the cloned repo and set the remote to your pass passwordstore repo eg:

    cd ~/.password-store
    git remote set-url origin git@github.com:user/passwords.git

link or copy hooks to .git/hooks:

    ln -s $( pwd)/.hooks/pre-commit .git/hooks
    ln -s $( pwd)/.hooks/post-merge .git/hooks
    ln -s $( pwd)/.hooks/post-checkout .git/hooks
    
init your password store:

    pass init <ids of the gpg keys you want to use>
    
That it.

Thanks to Sindre Sorhus, hooks are based on his gists.
