<img src="./favicon.svg" height="200" align="left"/>

### Orbit Browser Update Server

Static resource server for [Orbit Browser](https://github.com/safecircleia/orbit)'s automatic updates. It is served from GitHub Pages at `orbit-updates.safecircle.tech`.

## Layout

Update manifests follow `updates/browser/<target_build>/<branch>/update.xml`, for example `updates/browser/Linux_x86_64-gcc3/release/update.xml`.

`scripts/write_redirects.py` copies the manifests of renamed branches (such as `beta` to `release`) so clients on old update URLs keep working. The `Pre-Deploy` workflow runs it on every push to `main` and publishes the result to GitHub Pages.

## Install scripts

`install.sh`, `install-beta.sh` and `appimage.sh` install Orbit on Linux from the [latest release](https://github.com/safecircleia/orbit/releases/latest).

## Security

To report a vulnerability, see [SECURITY.md](SECURITY.md).

## License

[MIT](LICENSE)
