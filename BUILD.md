How to build
==========

ExQuilla is currently built as part of the Thunderbird build.

1. Copy the ExQuilla source directory into your Thunderbird source, into directory mozilla/extensions/exquilla/ (yes, mozilla/, not mail/)

2. In your `.mozconfig`, add:
```
ac_add_options --enable-extensions=default,exquilla
ac_add_options --enable-calendar
```

3. (Optional) If you want to build a release version of ExQuilla, set the environment variable:
```
export EXQUILLA_VERSION=60
```
or whatever version number you want. It will be added to install.rdf. It should normally match the Thunderbird version. If you don't set this, it will automatically take the Thunderbird major version, and add ".0pre1", e.g. "60.0pre1".

4. Re-run configure and build Thunderbird

5. You find the finished ExQuilla XPI in obj/`dist/xpi-stage/exquilla-(version).xpi`. It will also be unpacked in obj/`dist/bin/extensions/exquilla@mesquilla.com/`, ready to run with your Thunderbird build.
