FROM golang:1.17.3-alpine3.14
WORKDIR /app
COPY . .
ENV IPSTACK_API_KEY = http://api.ipstack.com/190.251.146.218?access_key=4a9355295da7ed5babd11364dbbd328e
ENV PORT=4001
RUN go build -o server .

EXPOSE 4001

CMD ["/app/server"]