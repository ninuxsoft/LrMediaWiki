# LrMediaWiki

**LrMediaWiki** is a plugin for Adobe Photoshop Lightroom that allows users
to upload images to Wikimedia Commons or any other MediaWiki installation
directly from Lightroom.

## Usage information

Usage information can be found on the page [Commons:LrMediaWiki][comlrmw] on
Wikimedia Commons.

## Developer information

LrMediaWiki is developed in Lua using the [Lightroom SDK][lrsdk].  It is
released under the MIT/X11 license.  LrMediaWiki should work with all 
Lightroom 5 installations both on Windows and on Mac OS.

### Code structure

The plugin code is located in the `mediawiki.lrdevplugin` directory.
`Info.lua` defines the plugin metadata to be read by Lightroom.
`MediaWikiExportServiceProvider.lua` defines the user interfaces and passes
all necessary information to `MediaWikiInterface.lua`.  This file evaluates
the user input and prepares the file description and the file itself for the
MediaWiki upload.  The upload is done in `MediaWikiApi.lua`.
`MediaWikiUtils.lua` provides common utility functions, and
`MediaWikiMetadataProvider.lua` defines the custom metadata containing e. g.
the file description and additional categories and templates.

[comlrmw]: https://commons.wikimedia.org/wiki/Commons:LrMediaWiki
[lrsdk]: http://www.adobe.com/devnet/photoshoplightroom.html
