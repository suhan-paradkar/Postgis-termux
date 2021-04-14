# Postgis-termux
Its a short script to install postgis plugin for termux.

Copy this script and run👍👍



```
pkg install build-essential
pkg install wget curl libiconv postgresql libxml2 libsqlite readline libiconv proj libgeos json-c libprotobuf-c gdal
wget https://download.osgeo.org/postgis/source/postgis-3.1.0.tar.gz
tar xfz postgis-3.1.0.tar.gz
cd postgis-3.1.0
./configure --prefix=$PREFIX --with-projdir=$PREFIX
make -j8
make install
mkdir -p $PREFIX/var/lib/postgresql
initdb $PREFIX/var/lib/postgresql
pg_ctl -D $PREFIX/var/lib/postgresql start
psql -l
createdb gis
```

Thanks for @seabre to come up with it👍
