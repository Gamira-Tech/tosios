# TOSIOS · Gamira client

Client integration patches for [TOSIOS](https://github.com/halftheopposite/TOSIOS),
connecting browser players to Gamira matchmaking and an authentication platform.

## Apply the patch

Run these commands from a new working directory. Git and tar are required.

```bash
git clone https://github.com/Gamira-Tech/tosios.git tosios-patches
git clone https://github.com/halftheopposite/TOSIOS.git tosios-upstream
mkdir -p tosios-client/TOSIOS
git -C tosios-upstream archive 98de136e524d25c5877adc9523c9445bc2b4a262 \
  LICENSE README.md .gitignore package.json tsconfig.json yarn.lock \
  packages/client packages/common | tar -x -C tosios-client/TOSIOS
cd tosios-client
git apply --check ../tosios-patches/patches/0001-gamira-integration.patch
git apply ../tosios-patches/patches/0001-gamira-integration.patch
```

The upstream revision and patch checksum are recorded in [upstream.json](upstream.json).

## Configure and run

Edit `TOSIOS/packages/client/public/client-config.js`:

```javascript
window.GAMIRA_CONFIG = {
    gamiraUrl: "https://gamira.example.com",
    platformUrl: "https://platform.example.com"
};
```

Use the authentication platform's base URL without `/api/v1`. These are public
service URLs. Both services must allow the browser client's origin through CORS,
and authentication redirects must return to the client origin.

With Node.js, Yarn Classic and Python 3 installed:

```bash
cd TOSIOS
yarn install --frozen-lockfile
BUILD_MODE=production yarn build
yarn serve
```

Open http://localhost:8080. The generated files in `packages/client/public/` can
also be hosted on a static web server. Edit `client-config.js` to change service
URLs without rebuilding. Game servers and the two services are operated separately.

The client uses game mode `gm_tosios`, configured in the Gamira instance.
Patch reconstruction and the production web build have been checked.

## Credits

Original game: Aymeric Chauvin and TOSIOS contributors, MIT.
See [CREDITS.md](CREDITS.md) for third-party acknowledgements. Preserve upstream
licence notices with the reconstructed client.

## Licence

Gamira’s client integration changes are licensed under [MIT](LICENSE). Original
upstream copyright and licence notices are preserved in [NOTICE.md](NOTICE.md)
and [LICENSES/](LICENSES/). Third-party assets and dependencies retain their own terms.
