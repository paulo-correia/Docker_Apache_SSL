# Apache SSL on Docker (Alpine Linux Image)

## Save Dockerfile on a folder Ex: Apache
**Caution: Only one dockerfile per folder**

### Generate image

docker build -t `<name>` .

`<name>` = Ex: apache or your_docker_hub_name/apache:1.0

### Running Container

docker run -d -p `<local port>`:80 -p `<other local port>`:443 `<name>`

`<local port>` = Ex 8080

`<other local port>` = Ex 8443

### If don't generate image, get from docker hub

docker run -d -p `<local port>`:80 -p `<other local port>`:443 paulocorreia/alpine_apache_ssl:1.0

### Open Browser
`http://localhost:<local port>`

`https://localhost:<other local port>`

If `<local port>` is 80 you can omit

If `<other local port>` is 443 you can omit

If you see "It works on Docker SSL!" is OK

Download certificate

`https://localhost:<other local port>/localhost.crt`

To correct the certificate on your browser import localhost.crt on Ceriticates - Authorities

Close the tab or browser reopen `https://localhost:<other local port>` and you see "It works on Docker SSL!" is OK