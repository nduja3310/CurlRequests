#Curl requests 

## List of teams

curl -L \
 -H "Accept: application/vnd.github+json" \
 -H "Authorization: Bearer $(head -n 1 config.txt)" \
 https://api.github.com/orgs/$(head -n 2 config.txt | tail -1)/teams -o output.json 
