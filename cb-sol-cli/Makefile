SOL_URL=https://github.com/cypherium/meshbridge-solidity
SOL_VERSION="v1.0.0"

fetch-contracts:
	@echo " > \033[32mFetching meshbridge-solidity contracts... \033[0m "
	git clone ${SOL_URL} && cd meshbridge-solidity && git checkout ${SOL_VERSION}

compile:
	cd meshbridge-solidity && npm install && npx truffle compile

install: fetch-contracts compile
	@echo " > \033[32mInstalling cb-sol-cli... \033[0m "
	npm link .

clean:
	rm -rf meshbridge-solidity/
