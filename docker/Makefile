all: lachesis tx-storm

TAG ?= "latest"

.PHONY: lachesis
lachesis: test_accs.json
	cd ../ && \
	docker build \
	    --network=host \
	    --build-arg GOPROXY=$(GOPROXY) \
	    -f docker/Dockerfile.lachesis -t "lachesis:$(TAG)" .


.PHONY: tx-storm
tx-storm:
	cd ../ && \
	docker build \
	    --network=host \
	    --build-arg GOPROXY=$(GOPROXY) \
	    -f docker/Dockerfile.tx-storm -t "tx-storm:$(TAG)" .


.PHONY: snapshots
snapshots:
	cd ../ && \
	docker build \
	    --network=host \
	    --build-arg GOPROXY=$(GOPROXY) \
	    -f docker/Dockerfile.snapshots -t "lachesis-snapshots:$(TAG)" .


test_accs.json:
	./_test_accs.sh