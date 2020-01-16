GOCMD=go
SQLBOILERCMD=sqlboiler
PSQLCMD=psql
REALIZECMD=realize

test:
	$(GOCMD) test ./...

debug:
	$(DLVCMD) debug /urge-app --listen=:40000 --headless=true --api-version=2 --log

run:
	$(REALIZECMD) start --run 

build:
	$(GOCMD) build -o ./build/app-go main.go

migrate:
	$(SQLBOILERCMD) --wipe psql
