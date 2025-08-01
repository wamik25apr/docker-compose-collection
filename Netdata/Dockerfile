FROM netdata/netdata:stable

# Install required tools
RUN apt-get update && \
    apt-get install -y smartmontools wget && \
    rm -rf /var/lib/apt/lists/*

# Create plugin directory
RUN mkdir -p /usr/lib/netdata/python.d

# Download smart.chart.py from the correct path
RUN wget -O /usr/lib/netdata/python.d/smart.chart.py \
    https://raw.githubusercontent.com/netdata/netdata/master/collectors/python.d.plugin/smart/smart.chart.py
