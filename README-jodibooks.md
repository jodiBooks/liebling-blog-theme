# Readme

Source: <https://github.com/eddiesigner/liebling/wiki/Theme-development-with-Docker>

## Always

1. Open a shell, terminal or command window to `liebling-blog-theme/src`

## Install / prepare

1. Run `yarn install`
2. Run `yarn get-database`

## Develop (doesn't work)

1. Start docker (if on Windows)
2. Run `docker compose pull`
3. Run `yarn docker-watch`
4. Close the auto-opened browser tab to `localhost:3000` and open a new one to `localhost:2368s`
5. Develop theme using vscode or other editor

## Develop workaround

1. Develop theme using vscode or other editor
2. Create production "build" and upload to `blog.acc.jodibooks.com/ghost`, see below

## Create production theme

1. OS dependent
    1. Linux: Run `yarn production`
    2. Windows: Run `yarn build`, `cd ..` and `7z a -xr'!.git' -xr'!src' -x'!liebling.zip' liebling.zip *`
2. Upload zip file <https://acc-blog.jodibooks.com/ghost/#/settings/design/change-theme>
    Settings (bottom left corner) --> Design (settings screen) --> Change Theme (bottom left corner) --> Upload theme (button top)

## Possible issues

1. You really need to do the install steps first. Docker will create empty folders otherwise and crash.
2. If you did start docker first, run `docker system prune -a` to clean up docker environment (cache).
