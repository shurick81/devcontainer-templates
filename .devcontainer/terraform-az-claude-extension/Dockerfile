FROM hashicorp/terraform:1.13.5

# Install Azure CLI
RUN apk add --no-cache python3 py3-pip && \
    apk add --no-cache --virtual=build gcc libffi-dev musl-dev python3-dev && \
    pip3 install --break-system-packages --no-cache-dir azure-cli && \
    apk del --purge build
