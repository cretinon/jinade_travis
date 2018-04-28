ARG ARCH=frommakefile
ARG DISTRIB=frommakefile
ARG DOCKERSRC=frommakefile
ARG USERNAME=frommakefile
#
FROM ${USERNAME}/${DOCKERSRC}:${DISTRIB}_${ARCH}
#
RUN set -xe \
    && gem install travis \
    && gem cleanup \
    && rm -rf /usr/lib/ruby/gems/*/cache/* \
    && echo "y" | travis version

CMD ["travis"]

