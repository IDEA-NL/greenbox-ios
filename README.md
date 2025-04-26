# Greenbox for iOS

This is a very thin wrapper around the web app. It's basically just a WebView pointing directly to the production URL, so this **does not need to be rebuilt** when an app update is deployed.

It was generated using PWABuilder, so the following documentation will probably be helpful:

- https://docs.pwabuilder.com/#/builder/app-store
- https://docs.pwabuilder.com/#/builder/faq?id=ios

## Development setup

### Cloud Mac setup

Easy copy-pastable steps to set up a fresh macOS system for development (hint: use a Scaleway "cloud" mac mini).

```sh
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo >> ~/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"

# Install Cocoapods
brew install cocoapods

# Generate an SSH key
ssh-keygen -f ~/.ssh/id_ed25519 -q -N ""
echo
cat ~/.ssh/id_ed25519.pub
echo
```

Add the SSH key here: https://github.com/IDEA-NL/greenbox-ios/settings/keys/new

```sh
git clone git@github.com:IDEA-NL/greenbox-ios.git
cd greenbox-ios

# Install build dependencies
export LANG=en_US.UTF-8
pod install

# Open XCode
open ./Greenbox.xcworkspace
```

### Compile and run the app

- wait for Xcode to open
- wait for it to stop spinning in the title bar
- press "play"
- it will want to download something, say yes and wait
- click where it says "Any iOS Device ..." in the title bar and pick a simulator in the dropdown
- press "play" and wait

