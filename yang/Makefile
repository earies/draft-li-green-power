REQS = pyang yanglint xmllint pygmentize

I := $(foreach exec,$(REQS),\
     $(if $(shell PATH=$(PATH) which $(exec) 2>/dev/null),,$(error "$(exec) not found in $$PATH")))

tree:
	@pyang \
		-f tree \
		--tree-path /hardware/component/power \
		ietf-hardware\@2018-03-13.yang \
		ietf-green-power.yang

lint:
	@yanglint \
		-f xml data.xml \
		ietf-hardware\@2018-03-13.yang \
		iana-hardware\@2018-03-13.yang \
		ietf-green-power.yang \
		| xmllint - | pygmentize -l xml
