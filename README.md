# yay-docker
Dockerfile for yay, handy for testing and building AUR packages

### Test Package
`docker run --rm thann/yay <package names>`

### Build and Recover Packages
```
mkdir /tmp/yay
docker run --rm -v "/tmp/yay:/home/build/.cache/yay" thann/yay <package names>
find /tmp/yay | grep pkg.tar.xz
```
Install with: `sudo pacman -U /tmp/yay/**/*.pkg.tar.xz`
