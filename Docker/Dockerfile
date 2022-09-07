# Initial Build
FROM golang:alpine AS step1
WORKDIR /app

COPY /Go /app/
RUN GOOS=linux go build -o HelloGo

# Optimization Build
FROM scratch

COPY --from=step1 /app/HelloGo /HelloGo
ENTRYPOINT [ "/HelloGo" ]
