FROM amazoncorretto:11

RUN yum update -y && \
	yum install -y \
		sudo \
		curl \
		bzip2 \
		tar \
		wget \
		unzip \
		gnupg
		
RUN yum update -y && \
	yum install -y \
		freetype \
		freetype-devel \
		libpng-devel \
		mesa-libGL-devel \
		mesa-libGLU-devel \
		libX11-devel \
		libsm6 \
		libXi \
		libXrender \
		libSM.x86_64 \
		perl-Time-HiRes

WORKDIR /jooby
RUN wget https://repo1.maven.org/maven2/io/jooby/jooby-cli/2.8.7/jooby-cli-2.8.7.zip
RUN unzip jooby-cli-2.8.7.zip
RUN rm jooby-cli-2.8.7.zip
ENV PATH $PATH:/jooby/bin:/jooby/lib


ENTRYPOINT ["/bin/bash"]

