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
		ietf-green-power.yang
