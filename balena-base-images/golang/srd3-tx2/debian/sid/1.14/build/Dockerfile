# AUTOGENERATED FILE
FROM balenalib/srd3-tx2-debian:sid-build

ENV GO_VERSION 1.14

RUN mkdir -p /usr/local/go \
	&& curl -SLO "https://storage.googleapis.com/golang/go$GO_VERSION.linux-arm64.tar.gz" \
	&& echo "cd813387f770c07819912f8ff4b9796a4e317dee92548b7226a19e60ac79eb27  go$GO_VERSION.linux-arm64.tar.gz" | sha256sum -c - \
	&& tar -xzf "go$GO_VERSION.linux-arm64.tar.gz" -C /usr/local/go --strip-components=1 \
	&& rm -f go$GO_VERSION.linux-arm64.tar.gz

ENV GOROOT /usr/local/go
ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH

RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
WORKDIR $GOPATH

CMD ["echo","'No CMD command was set in Dockerfile! Details about CMD command could be found in Dockerfile Guide section in our Docs. Here's the link: https://balena.io/docs"]

 RUN curl -SLO "https://raw.githubusercontent.com/balena-io-library/base-images/8accad6af708fca7271c5c65f18a86782e19f877/scripts/assets/tests/test-stack@golang.sh" \
  && echo "Running test-stack@golang" \
  && chmod +x test-stack@golang.sh \
  && bash test-stack@golang.sh \
  && rm -rf test-stack@golang.sh