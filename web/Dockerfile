FROM golang AS build

WORKDIR /app
COPY dispatcher.go .
RUN go build dispatcher.go

FROM ubuntu

WORKDIR /app
COPY --from=build /app/dispatcher .
COPY static ./static

EXPOSE 80
CMD ["./dispatcher"]