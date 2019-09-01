FROM registry.access.redhat.com/ubi7/ubi-minimal:latest

ENV OPERATOR=/usr/local/bin/advanced-deployment \
    USER_UID=1001 \
    USER_NAME=advanced-deployment

# install operator binary
COPY build/_output/bin/advanced-deployment ${OPERATOR}

COPY build/bin /usr/local/bin
RUN  /usr/local/bin/user_setup

ENTRYPOINT ["/usr/local/bin/entrypoint"]

USER ${USER_UID}
