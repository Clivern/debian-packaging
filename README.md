<p align="center">
    <img alt="Debian Packaging Logo" src="https://raw.githubusercontent.com/clivern/debian-packaging/master/assets/img/logo.png" height="100" />
    <h3 align="center">Debian Packaging</h3>
    <p align="center">A Debian Packaging Kit.</p>
</p>


## Preparation

### Install Dependencies

```console
$ apt-get install dpkg-dev
$ apt-get install gdebi-core
$ apt-get install debhelper
$ apt-get install devscripts
$ apt-get install dput
```

### GPG Signing

Identify your private key by running

```console
$ gpg --list-secret-keys
```

Run this command to export your key

```console
$ gpg --export-secret-keys $ID > my-private-key.asc
```

To import the key

```console
$ gpg --import my-private-key.asc
```

To delete both the private and public key

```console
$ gpg --delete-keys
$ gpg --delete-secret-keys
```


## Build the package

```console
$ debuild -S
```

## Release to PPA

```console
$ dput ppa:clivern/ppa <source.changes>
```


## References

- [Ubuntu Packaging Guide.](http://packaging.ubuntu.com/)
- [Debian packaging for the modern developer.](https://github.com/phusion/debian-packaging-for-the-modern-developer)


## License

© 2019, Clivern. Released under [MIT License](https://opensource.org/licenses/mit-license.php).

**debian-packaging** is authored and maintained by [@clivern](http://github.com/clivern).
