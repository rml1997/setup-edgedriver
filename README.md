# setup-edgedriver

<p align="left">
  <a href="https://github.com/rml1997/setup-edgedriver"><img alt="GitHub Actions status" src="https://github.com/nanasess/setup-edgeFdriver/workflows/Test%20edgedriver/badge.svg"></a>
  <a href="https://github.com/rml1997/setup-edgedriver/blob/master/LICENSE"><img alt="LICENSE" src="https://img.shields.io/badge/license-MIT-428f7e.svg"></a>
</p>

This action sets up an [Edge Webdriver](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/) for use in actions

# Usage

See [action.yml](action.yml)

``` yaml
steps:
- uses: actions/checkout@master
- uses: rml1997/setup-edgedriver@master
  with:
    # Optional: do not specify to match Edge's version
    webdriver-version: '77.0.3865.40'
- run: |
    export DISPLAY=:99
    webdriver --url-base=/wd/hub &
    sudo Xvfb -ac :99 -screen 0 1280x1024x24 > /dev/null 2>&1 & # optional
 ```


