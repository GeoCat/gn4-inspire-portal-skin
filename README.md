# Inspire Portal theme for GeoNetwork 4.x
This skin can be plugged on to geonetwork to represent the popular catalog application with a custom layout.

## Requirements

- GeoNetwork Enterprise 2020.5 or GeoNetwork opensource 4.0.x and higher

## For Developers

### If at build time (mvn install)

Add the skin as a submodule in `web-ui/src/main/resources/catalog/views/inspireportal`:
```
git submodule add -b main http://eos.geocat.net/gitlab/geocat/inspireportalview.git web-ui/src/main/resources/catalog/views/inspireportal
git submodule init
```

### If at run time (war)

- Deploy the GeoNetwork Enterprise 2020.5 or GeoNetwork opensource 4.0.x war
- Grab a zip of http://eos.geocat.net/gitlab/geocat/inspireportalview.git/tree/main
- Unzip it in `TOMCAT_DIR/webapps/geonetwork/catalog/views/inspireportal`

## Overwrite

While the view itself is completely independent, the EU style and script includes are done outside of the view.
These includes require changes to `src/main/webapp/xslt/base-layout-cssjs-loader.xsl`. This changed file is included in the view directory,,
but has to be copied to: `src/main/webapp/xslt/`.

## Activate

- Change the setting `View` to `inspireportal` in  `Administration` > `Settings`

## Changes

This view is based on the `default` theme of GeoNetwork opensource. The files have been renamed to match the new name: `inspireportal`, apart from renaming the contents are still default.
However, a couple of files have been changed or added:

### New files (follows the names of the EU)

**HTML**
- src/main/resources/catalog/views/inspireportal/templates/pageHeader.html
- src/main/resources/catalog/views/inspireportal/templates/siteHeader.html
- src/main/resources/catalog/views/inspireportal/templates/top-toolbar.html

**IMAGES/SVG**
- src/main/resources/catalog/views/inspireportal/images/icons.3cf410f9.svg
- src/main/resources/catalog/views/inspireportal/images/logo--en.5055ef4f.svg

### Changed files

**HTML**
- src/main/resources/catalog/views/inspireportal/templates/footer.html
- src/main/resources/catalog/views/inspireportal/templates/home.html
- src/main/resources/catalog/views/inspireportal/templates/index.html

**Less**
- src/main/resources/catalog/views/inspireportal/less/gn_view_inspireportal.less
