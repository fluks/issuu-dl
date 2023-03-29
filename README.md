# issuu-dl

issuu-dl downloads documents from [issuu.com](https://issuu.com). It downloads
the document's pages in the jpg format and saves those in /tmp to some temporary
directory. The images are not deleted. The images are then converted to a pdf
and it will be saved in the current directory and named by the title of the
document.

## Usage

```
./issuu-dl <url of the magazine/book on issuu.com>
```

The URL needs to be for the whole document, for example
[https://issuu.com/jmadler/docs/modern_perl](https://issuu.com/jmadler/docs/modern_perl),
not anything else, like not a URL for a single page.

You might need to change a couple of ImageMagick policies. The file is
/etc/ImageMagick-6/policy.xml in Linux.

Uncomment this one or set to rights="read|write".

```
<policy domain="coder" rights="none" pattern="PDF" />
```

Set disk cache usage higher, I set it to 8GiB here.

```
<policy domain="resource" name="disk" value="8GiB"/>
```

## Dependencies

wget, ImageMagick (convert).

## WWW

If you can't or don't want to use this command line tool, there is also a
website at https://issuudownloader.tech/.
