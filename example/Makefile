##

.PHONY: clean, build

# 设置静态编译
CLIB_ENABLE := $(go env CGO_ENABLED)
ifeq ($(CLIB_ENABLE),1)
	go env -w CGO_ENABLED=0
endif

build:
	go build -trimpath -ldflags="-s -w -X main.version=0.1.1" -o example

clean:
	rm -fr example