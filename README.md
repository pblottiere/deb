# Packaging

Documentation:

- https://wiki.debian.org/Packaging/
- https://wiki.debian.org/Packaging/Intro?action=show&redirect=IntroDebianPackaging

Install dependencies:

```` bash
$ apt-get install curl devscripts
````

Build deb package

```` bash
$ debuild -us -uc
````
