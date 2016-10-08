FROM python:2.7
MAINTAINER Allen Zou <yalong.zou@hyku.com>

COPY requirements.txt /env/requirements.txt
RUN pip install -i https://pypi.douban.com/simple/ -r /env/requirements.txt

WORKDIR /workspace/src
CMD python -m internal.content.main --config-file=/config/internal-content.yaml \
    --rpc-config=/config/rpc.hjson
EXPOSE 80
