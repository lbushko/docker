# Use Ubuntu
FROM ubuntu

# Install wger & JRE
RUN apt-get clean && \
	apt-get update && \
	apt-get -qy install \
			wget \
			default-jre-headless \
			telnet \
			iputils-ping \
			unzip

# Install jmeter
RUN   mkdir /jmeter \
	&& cd /jmeter/ \
	&& wget https://archive.apache.org/dist/jmeter/binaries/apache-jmeter-3.2.tgz \
	&& tar -xzf apache-jmeter-3.2.tgz \
	&& rm apache-jmeter-3.2.tgz

# Set Jmeter Home
ENV JMETER_HOME /jmeter/apache-jmeter-3.2/

# Add Jmeter to the Path
ENV PATH $JMETER_HOME/bin:$PATH