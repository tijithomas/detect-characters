From ocdr/dkube-datascience-tf-cpu:v1.12

USER root
RUN apt-get update && apt install -y python3-lxml
RUN pip3 install contextlib2

RUN mkdir -p /home/dkube/object_detection

WORKDIR /home/dkube/object_detection
CMD ["python", "create_tf_record.py", "--label_map_path=label_map.pbtxt", "--data_dir=.", "--year=VOC2012", "--set=train", "--output_dir=./TFRecords" ]

