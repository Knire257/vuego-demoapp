FROM golang:1.17.3-alpine3.14
WORKDIR /app
COPY . .
RUN go build -o server .

EXPOSE 4001
ENV PORT=4001
CMD ["/app/server"]