check-config:
	checkconfig --plugin-config=plugins.yaml --config-path=config.yaml

update-config:
	kubectl create configmap -n prow config --from-file=config.yaml=config.yaml --dry-run=client -o yaml | kubectl replace configmap -n prow config -f -

update-plugins:
	kubectl create configmap -n prow plugins --from-file=plugins.yaml=plugins.yaml --dry-run=client -o yaml | kubectl replace configmap -n prow plugins -f -
