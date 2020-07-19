FROM centos
RUN yum install wget -y
RUN wget https://dl.grafana.com/oss/release/grafana-7.0.6-1.x86_64.rpm
RUN yum install grafana-7.0.6-1.x86_64.rpm -y
WORKDIR /usr/share/grafana
ENTRYPOINT ["/usr/sbin/grafana-server", "--config=/etc/grafana/grafana.ini", "cfg:default.paths.logs=/var/log/grafana", "cfg:default.paths.data=/var/lib/grafana", "LimitNOFILE=10000"]
