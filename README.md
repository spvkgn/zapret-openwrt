[![build](https://github.com/spvkgn/zapret-openwrt/actions/workflows/build.yml/badge.svg)](https://github.com/spvkgn/zapret-openwrt/actions/workflows/build.yml)
# zapret-openwrt
```
docker run --rm -it --name openwrt openwrt/rootfs
```
```shell
cat << "EOF" > /tmp/public.key
untrusted comment: Zapret OpenWrt repo
RWSTOuDF+DZrAwxYFMJP+U1YZpaukPIXAn7mTZrs8FNKM5qlsGBw8fXj
EOF
```
```shell
opkg-key add /tmp/public.key && \
echo 'src/gz zapret_repo https://spvkgn.github.io/zapret-openwrt/SNAPSHOT/x86_64' >> /etc/opkg/customfeeds.conf && \
mkdir -p /var/lock/ && opkg update
```
