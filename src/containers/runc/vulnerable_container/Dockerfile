FROM golang:1.14.4-stretch
#RUN apt update -y && apt install gcc runc unzip -y
COPY run_c_vul.go .
#RUN go build run_c_vul.go
#RUN cp main exploit
COPY ttyd_linux.x86_64 /opt/ttyd
RUN ["chmod", "+x", "/opt/ttyd"]
ENTRYPOINT ["/opt/ttyd", "-p", "8081", "bash"]