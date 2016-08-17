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

## Dependencies

wget, HTML::Entities, convert.
