Testing Docker Image
====================

Once the image has been built:
```
docker build -t "wssystems/lychee" .
```

Start it with the following:
```
docker run -p 8888:8888 wssystems/lychee
```

You will also need a MySQL DB:
```
docker run -e "MYSQL_ROOT_PASSWORD=cat" -p 3306:3306 mysql
```

Go to http://localhost:8888 and enter the DB Host (your computer's hostname,
127.0.0.1/localhost won't work), with username `root` and password `cat`. Check
the Diagnostic and try logging in/out, upload an image if you like.
