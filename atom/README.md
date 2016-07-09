Backup : apm list --installed --bare > packages.list
files : .json, .cson, .coffee .less
for i in $(find ~/.atom/ -type f -name "*.cson" -o -name "*.json" -o -name ".coffee" -o -name "*.less" | grep -v compile-cache); do rsync -avR $i files/; done


Restore : apm install `cat packages.list
