# Find And Sed
## remove comments
```zsh
find . -name *.swift -exec sed -i "" "s/\/\/.*//g" {} \;
```
