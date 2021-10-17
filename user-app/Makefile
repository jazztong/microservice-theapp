migrate:
	npx prisma migrate dev

server:
	npm run dev

test:
	npm run test

cover:
	jest --collect-coverage

docker:
	docker build -f ../templates/Dockerfile --platform linux/amd64 . -t userapp

run-docker:
	docker run -it --rm \
	-e DATABASE_URL="postgresql://postgres:password@host.docker.internal:5432/user-db?schema=public" \
	-p 3000:3000 userapp

schema:
	prisma generate --schema=./src/prisma/schema.prisma
