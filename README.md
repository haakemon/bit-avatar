# &lt;bit-avatar&gt;

> A custom webcomponent for avatars. Currently full support for Gravatar, facebook, twitter, google+ and skype avatars.

## Demo

[Check it live!](http://hbogs.github.io/bit-avatar)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install bit-avatar --save
```

Or [download as ZIP](https://github.com/hbogs/bit-avatar/archive/master.zip).

## Usage

1. Import Web Components' polyfill:

    ```html
    <script src="bower_components/platform/platform.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/bit-avatar/dist/bit-avatar.html">
    ```

3. Start using it!

    ```html
    <bit-avatar></bit-avatar>
    ```

## Options

Attribute     | Options     | Default      | Description
---           | ---         | ---          | ---
`user-id`     | *string*   | *None*        | Gravatar: Email hash.<br>Facebook: Facebook ID.<br>Skype: Skype username.<br>Twitter: Twitter username.<br>Google+: Google ID. To find your Google ID, go to [https://picasaweb.google.com/data/entry/api/user/XXX?alt=json](https://picasaweb.google.com/data/entry/api/user/XXX?alt=json) where XXX is your Google username. Your ID will be at the bottom (gphoto$user).
`provider`    | `gravatar`, `facebook`, `google+`, `twitter`, `skype` | `gravatar` | What provider to use when fetching the avatar.
`name` | *string* | '' | The name for the avatar user (alt-attribute)
`size` | *int* OR *string* (facebook: `small`, `normal`, `large`, `square`), (twitter: `mini`, `normal`, `bigger`, `original`) | | Facebook and twitter uses strings. Gravatar and google+ uses an int. Skype has no size options.<br> Facebook sizes: small=80\*auto, normal=100\*auto, large=200\*auto, square=50\*50.<br> Twitter sizes: mini=24\*24, normal=48\*48, bigger=73\*73, original=original size.
`gravatar-rating` | `g`, `pg`, `r`, `x` | *None* | See [gravatar documentation](https://en.gravatar.com/site/implement/images/) (rating) for more information.
`gravatar-default` | `404`, `mm`, `identicon`, `monsterid`, `wavatar`, `retro`, `blank`, *URL to custom default* | *None* | See [gravatar documentation](https://en.gravatar.com/site/implement/images/) (default image) for more information.
`gravatar-force-default` | *None* | | If this attribute is present, the default gravatar will be forced even if an avatar exists for that user. See [gravatar documentation](https://en.gravatar.com/site/implement/images/) (force default) for more information.



## Development

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

* Install [Bower](http://bower.io/) & [Grunt](http://gruntjs.com/):

    ```sh
    $ [sudo] npm install -g bower grunt-cli
    ```

* Install local dependencies:

    ```sh
    $ bower install && npm install
    ```

* To test your project, start the development server and open `http://localhost:8000`.

    ```sh
    $ grunt server
    ```

* To build the distribution files before releasing a new version.

    ```sh
    $ grunt build
    ```

* To provide a live demo, send everything to `gh-pages` branch.

    ```sh
    $ grunt deploy
    ```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

For detailed changelog, check [Releases](https://github.com/hbogs/bit-avatar/releases).

## License

[MIT License](http://opensource.org/licenses/MIT)
