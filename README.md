# hiv-orderly-proxy

Proxy for HIV orderly setup

## Usage

This is designed to work with [orderly-web-deploy](https://github.com/vimc/orderly-web-deploy/)

```
docker run --name proxy --network network mrcide/hiv-orderly-proxy:latest example.com 80 443 service
```

## Update patch

* Copy and modify https://github.com/reside-ic/proxy-nginx/blob/master/nginx.conf to match your required config
* Get a diff from plain nginx.conf to modified version `diff -u <unmodified> <modified> > new_patch`
* Move the new patch to `./nginx.conf.patch`

## Modifying the patch

You can add new lines to the patch itself. If you do, remember to update the line length to work with any changes. This is the number `10` in the example below for the no of lines to be added.

```
@@ -74,8 +74,10 @@
```