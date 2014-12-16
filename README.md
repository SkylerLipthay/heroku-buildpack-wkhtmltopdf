# Heroku Buildpack: wkhtmltopdf

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [wkhtmltopdf](http://wkhtmltopdf.org/) in your application.

It is designed to be used with [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) to combine it with the appropriate real buildpack for your app.

This is based on https://github.com/jayzes/heroku-buildpack-pngquant.

### Version

It is configures with wkhtmltopdf version 0.12.2-dev-5dea253 released on November 22, 2014.

### Stack

This is designed to be used on [Cedar-14 Stack](https://devcenter.heroku.com/articles/cedar).

## Usage

Add a `.buildpacks` file to the root of your repo that contains this buildpack URL and your real buildpack URL:

    https://github.com/rafaelp/heroku-buildpack-wkhtmltopdf
    https://github.com/heroku/heroku-buildpack-ruby

Then create an application using the multi buildpack:

    $ heroku create --stack cedar-14 --buildpack https://github.com/ddollar/heroku-buildpack-multi

or configure an existing application:

    $ heroku config BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi

You can verify that everything is properly installed by running the following command:

    $ heroku run "wkhtmltopdf -V"

The output should be:

    wkhtmltopdf 0.12.2-dev-5dea253 (with patched qt)

## Issues

If you have problems, please create a [Github Issue](https://github.com/rafaelp/heroku-buildpack-wkhtmltopdf/issues).

## Credits

heroku-buildpack-wkhtmltopdf was originally written by [Rafael Lima](http://rafael.adm.br).

Working at [Boleto Simples](https://boletosimples.com.br)

Github: [http://github.com/rafaelp](http://github.com/rafaelp)

Twitter: [http://twitter.com/rafaelp](http://twitter.com/rafaelp)

## License

heroku-buildpack-wkhtmltopdf is Copyright © 2014 Rafael Lima. It is free software, and may be redistributed under the terms specified in the [LICENSE](https://github.com/rafaelp/heroku-buildpack-wkhtmltopdf/blob/master/LICENSE) file.
