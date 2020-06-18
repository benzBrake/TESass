<table width="100%">
    <tr>
        <td align="left" width="100%" colspan="2">
            <h1><strong>TESass</strong></h1><br />
            Use Sass with Typecho via NPM Scripts. Copy from ahmadawais/WPSass.
        </td>
    </tr>
    <tr>
        <td>
            A FOSS (Free & Open Source Software) project. Maintained by <a href="https://github.com/benzBrake">@benzBrake</a>.
        </td>
    </tr>
</table>

Use Sass with Typecho, Node Script in SCSS flavor.

![TESass](https://fakeimg.pl/600x200/75387D/FFF/?retina=1&text=TESass)

# 🎗 TE Sass — Getting Set up

Make sure you have node installed. If not [download and install node](https://nodejs.org/en/download/).

## → STEP #1: Install NodeJS & NPM
After installing NodeJS you can verify the install of both NodeJS and Node Package Manager by typing the following commands. This step needs to be followed only once i.e. if you don't have NodeJS installed. No need to repeat it ever again.

```bash
node -v
# v7.10.0

npm -v
# 4.2.0
```

## → Step #2. Clone this repo
```bash
cd usr/themes
git clone https://www.github.com/benzBrake/TESass ${YOUR_THEME}
```

## → STEP #3: Installing Node Dependencies

We are in the root folder of our WordPress plugin or WordPress theme at the moment, let's install the Node Dependencies. In the terminal run this command and wait for it to download all the NodeJS dependencies. It's a one time process and can take about a minute depending on the internet speed of your connection.

```bash
# For MAC OS X run the following command with super user
sudo npm install

# For Linux run the following command
npm install
```

## → STEP #4: Configure NPM Scripts

Now, configure the NPM scripts. There are only two of them. If you open the [`package.json`](https://git.io/vHLHg) file. There are two scripts as follows:

```json
"scripts": {
  "css": "node-sass --output-style compressed --include-path scss assets/css/source.scss style.css",
  "watch": "nodemon -e scss -x \"npm run css\""
},
```

In the `css` script, you need to change
- SCSS Source File Path & Name — `assets/css/source.scss`
- Destination CSS File Path & Name — `style.css`

> NOTE: That currently this little app has following file structure
```bash
    ├── assets
    |  └── css
    |     ├── partial
    |     |  ├── base.scss
    |     |  └── variables.scss
    |     ├── source.scss
    |     └── vendor
    |        └── normalize.css
    ├── index.html
    ├── package.json
    └── style.css
```

`source.scss` is the source file for SCSS files, which imports files from `partials` and `vendor` directory. This gets compiled into a `style.css` file in the root of our project as configured in the npm script.


## → STEP #5: Run NPM Scripts

All that's left now is for you to run the NPM script in the root folder of your WP project — where you downloaded the [`package.json`](https://git.io/vHLHg) file.

> NOTE: Before you run, make sure there is a source SCSS file. Otherwise running the script will display this error `An output directory must be specified when compiling a directory`.

```bash
# Compile CSS.
npm run css
```

```bash
# Watch changes in SCSS files and compile CSS automatically.
npm run watch
```

```bash
# Pack your theme.
npm run zip
```

![Run](https://i.imgur.com/tIelJwy.gif)


## → STEP #6: Share!

Yup, there are no more steps. Just share it with your friends. Or [Click to Tweet about it on Weibo](http://service.weibo.com/share/share.php?url=https://www.github.com/benzBrake/TESass&title=TESass%20Typecho使用SASS制作主题).

## Contribute
Feel free to contribute. PR's are welcomed.

## Changelog

### Version 1.0.1 
- Compile: SCSS to CSS
- Watch: Changes in SCSS
- Zip: Pack theme


## License
Released under MIT License.

CopyLeft [Ryan](https://xiamp.net/)

Copyright [Ahmad Awais](https://AhmadAwais.com/)