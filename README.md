[![Build Status](https://travis-ci.org/masa4u/pyboostnote.svg?branch=master)](https://travis-ci.org/masa4u/pyboostnote)
[![Coverage Status](https://coveralls.io/repos/github/masa4u/pyboostnote/badge.svg)](https://coveralls.io/github/masa4u/pyboostnote)

# pyboostnote

boostnote.io python data handler(importer / exporter)

## support migration
 * moniwiki
 * gollum



## export to normal markdown

Using export_to_md.py, you can export BOOSTNOTE markdown to normalized markdown.

It remove ':storage' and ':note' link and add front-meta(PANDOC) headings.

It support below attachment link types,
 * LinkRelativePath
 * CopyToMarkdownPath
 * CopyToMarkdownSubPath

```python
from boostnote.base import Boostnote
from boostnote.export_to_md import export_boostnote, AttachPathType

source_path = 'c:/temp/boostnote'
target_path = 'c:/temp/boostnote_export'

boostnote = Boostnote([source_path])
storage = boostnote.storages['Default0']

export_boostnote(storage, target_path, AttachPathType.CopyToMarkdownPath)

```



## Future Updates

### importer

* adding unittest and migration examples



### exporter

* 
