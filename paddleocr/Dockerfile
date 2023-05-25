FROM python:3.7
RUN apt-get update && apt-get install ffmpeg libsm6 libxext6 -y
#RUN apt-get update && apt-get install -y python3-levenshtein gcc libgl-dev libglib2.0-dev
RUN python3 -m pip install paddlepaddle paddlehub -i https://mirror.baidu.com/pypi/simple
RUN hub install ch_pp-ocrv3
COPY ./test.jpg ./test.jpg
RUN hub run ch_pp-ocrv3 --input_path ./test.jpg
RUN rm ./test.jpg
CMD ["hub", "serving", "start", "-m", "ch_pp-ocrv3"]
EXPOSE 8866