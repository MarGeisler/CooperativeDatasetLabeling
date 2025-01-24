FROM ubuntu:20.04

WORKDIR /root

COPY run.sh .

RUN apt update && apt install -y python3-pip git wget

RUN pip install --upgrade pip

# RUN git clone --depth 1 https://github.com/naurril/SUSTechPOINTS.git
#RUN cd CooperativeDatasetLabeling && \
#        wget https://github.com/naurril/SUSTechPOINTS/releases/download/0.1/deep_annotation_inference.h5 -P algos/models && \
#        python3 -m pip install -r ./requirement.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

#ENTRYPOINT ["/root/run.sh"]

#EXPOSE 8081
RUN mkdir CooperativeDatasetLabeling
COPY requirement.txt /root/CooperativeDatasetLabeling/

RUN cd CooperativeDatasetLabeling && \
        python3 -m pip install -r ./requirement.txt -i https://pypi.tuna.tsinghua.edu.cn/simple


#CMD python3 -m pip install -r /root/CooperativeDatasetLabeling/requirement.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
