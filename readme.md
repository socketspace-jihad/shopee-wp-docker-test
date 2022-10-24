## Build Image
Make sure you create the folder on the host before starting the container and obtain the correct permissions.

```
git clone
cd shopee-wp-docker-test
docker build -t <image_name>:<image tag> .
```

## Creating an instance
Make sure you create the folder on the host before starting the container and obtain the correct permissions.

```
mkdir -p /data/{domain}/html
docker run -e VIRTUAL_HOST={domain}.com,www.{domain}.com -v /data/{domain}/html:/usr/html -p 80:80 <image_name>
```