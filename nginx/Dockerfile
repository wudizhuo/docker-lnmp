FROM nginx
MAINTAINER wudizhuo

ENV LANG en_US.UTF-8

# Setup and Install
#   * texlive-*: for LaTeX
#   * zip: for review-epubmaker
#   * curl & bzip2: for installing jlisting.sty
RUN apt-get update && \
	apt-get install -y locales && \
	echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen && \
	locale-gen en_US.UTF-8 && \
	update-locale en_US.UTF-8 && \
	apt-get install -y \
		texlive-lang-cjk \
		texlive-fonts-recommended \
		zip \
		curl \
		bzip2 && \
	apt-get clean && rm -rf /var/cache/apt/archives/* /var/lib/apt/lists/*