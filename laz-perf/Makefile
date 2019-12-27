VERSION=1.3.0

clean:
	rm -rf laz-perf*

wget:
	curl -LJ https://github.com/hobu/laz-perf/tarball/$(VERSION) -o laz-perf-tarball.tar.gz

prepare:
	tar zxf laz-perf-tarball.tar.gz --one-top-level=laz-perf-tarball --strip-components 1
	rm laz-perf-tarball.tar.gz
	mv laz-perf-tarball laz-perf-$(VERSION)
	tar zcf laz-perf_$(VERSION).orig.tar.gz laz-perf-$(VERSION)

	cp -r debian laz-perf-$(VERSION)

deb:
	cd laz-perf-$(VERSION)/debian && debuild -us -uc && cd -
