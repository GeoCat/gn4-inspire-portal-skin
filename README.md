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

## Activate

- Change the setting `View` to `inspireportal` in  `Administration` > `Settings`

## Changes

This view is based on the `default` theme of GeoNetwork opensource. The files have been renamed to match the new name: `inspireportal`, apart from renaming the contents are still default.
