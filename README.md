# litlife/sitemap

This package for create sitemap

## Installation

Use the package manager [composer](https://getcomposer.org/) to install.

```bash
composer require litlife/sitemap
```

## Usage

### Generate new sitemap and add new url

```bash
use Litlife\Sitemap\Sitemap;

$location = 'https://www.example.com';
$lastmod = '2005-01-01';
$changefreq = 'weekly';
$priority = 0.8;

$sitemap = new Sitemap();
$sitemap->addUrl($location, $lastmod, $changefreq, $priority);
```

### Get an array with locations

```bash
$sitemap = new Sitemap();
$sitemap->getUrls();
```

### Get xml string

```bash
$sitemap = new Sitemap();
$sitemap->getContent();
```

### Get size of xml in bytes

```bash
$sitemap = new Sitemap();
$sitemap->getSize();
```

### Get the number of locations in the current sitemap file

```bash
$sitemap = new Sitemap();
$sitemap->getUrlCount();
```

### Get the number of locations in the current sitemap file

```bash
$sitemap = new Sitemap();
$sitemap->getUrlCount();
```

### Open sitemap file

```bash
$sitemap = new Sitemap();
$sitemap->open('/path/to/file.xml');
```

### Open sitemap index file

```bash
use Litlife\Sitemap\SitemapIndex;

$index = new SitemapIndex();
$index->open('/path/to/sitemap_index.xml');
```

### Add a sitemap

```bash
$location = 'https://www.example.com/sitemap_index.xml';
$lastmod = '2005-01-01';

$index = new SitemapIndex();
$index->addSitemap($location, $lastmod);
```

### Get the number of sitemaps

```bash
$index = new SitemapIndex();
$index->getSitemapsCount();
```

### Get a list of sitemaps

```bash
$index = new SitemapIndex();
$index->getSitemaps();
```

### Get the xml string of the sitemaps

```bash
$index = new SitemapIndex();
$index->getContent();
```

## Testing
```bash
composer test
```
## License
[MIT](https://choosealicense.com/licenses/mit/)
