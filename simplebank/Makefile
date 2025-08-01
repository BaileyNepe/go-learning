createdb:
	docker exec -it simplebank_postgres createdb --username=postgres --owner=postgres simple_bank

dropdb:
	docker exec -it simplebank_postgres dropdb simple_bank

migrateup:
	migrate -path db/migration -database "postgresql://postgres:password@localhost:5455/simple_bank?sslmode=disable" -verbose up

migratedown:
	migrate -path db/migration -database "postgresql://postgres:password@localhost:5455/simple_bank?sslmode=disable" -verbose down

migrateup1:
	migrate -path db/migration -database "postgresql://postgres:password@localhost:5455/simple_bank?sslmode=disable" -verbose up 1

migratedown1:
	migrate -path db/migration -database "postgresql://postgres:password@localhost:5455/simple_bank?sslmode=disable" -verbose down 1

sqlc:
	sqlc generate

test:
	go test -v ./...	

server:
	go run main.go


.PHONY: createdb dropdb migrateup migratedown migrateup1 migratedown1 sqlc test server
