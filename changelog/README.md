# Changelog generator

The changelog generator can convert changelogs which are in the format (more or less) of [Keep a Changelog](http://keepachangelog.com/en/0.3.0/) to a computer readable yaml format and the other way around. The output it generates is in asciidoc format (not markdown).

The idea was to generate out of one large yaml file multiple user readable release notes. This can be useful if a project as multiple sub projects like plugins where each has its own changelog.


## Scripts

* changelog_to_yml.py: Converts and Asciidoc changelog to yaml
* changelog_to_asciidoc.py: Converts a yaml changelog to asciidoc and can collect multiple yaml files from different directories and combine them in one lager changelog based on the versions.
