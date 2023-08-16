# Readme

Source: <https://github.com/eddiesigner/liebling/wiki/Theme-development-with-Docker>

## Always

1. Open a shell, terminal or command window to `liebling-blog-theme/src`

## Install / prepare

1. Run `yarn install`
2. Run `yarn get-database`

## Develop

1. Start docker (if on Windows)
2. Run `yarn docker-watch`
3. Develop theme using vscode or other editor

## Create production theme

1. Run `yarn production`
2. Upload zip file <https://acc-blog.jodibooks.com/ghost/#/settings/design/change-theme>
    Settings (bottom left corner) --> Design (settings screen) --> Change Theme (bottom left corner) --> Upload theme (button top)

## Possible issues

1. You really need to do the install steps first. Docker will create empty folders otherwise and crash.
2. If you did start docker first, run `docker system prune -a` to clean up docker environment (cache).
