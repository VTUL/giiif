# giiif

giiif library is inspired by ruby gem iiif_s3 (https://github.com/cmoa/iiif_s3). It serves as a generator for IIIF level 0 compatible image tiles and metadata from a collection of source images. The generated image stack can also be uploaded to Amazon S3 and used for static serving.

## Installation

This library assumes that you have ImageMagick installed.  If you need to install it, follow the instructions:

on OSX, `brew install imagemagick ` should be sufficient.

If you have issues with TIFF files, try

```shell

brew update
brew reinstall --with-libtiff --ignore-dependencies imagemagick

```

If you plan to work with PDFs, you should also have a copy of GostScript installed.

on OSX, `brew install gs`


Add this line to your application's Gemfile:

    gem 'giiif'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install giiif

## Usage

If choose to upload to Amazon S3 , giiif assumes that you have an Amazon S3 account configured for use.  By default, it uses the same locations that the Amazon S3 ruby library searches:

>
  ENV['AWS_ACCESS_KEY_ID'] and ENV['AWS_SECRET_ACCESS_KEY']
  The shared credentials ini file at ~/.aws/credentials (more information)
  From an instance profile when running on EC2.
  The SDK also searches the following locations for a bucket name and a region:
  ENV['AWS_BUCKET_NAME'] and ENV['AWS_REGION']


## Contributing

1. Fork it ( https://github.com/VTUL/giiif/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
