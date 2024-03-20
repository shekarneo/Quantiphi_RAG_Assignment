# Quantiphi_RAG_Assignment

This project contains a Gradio application designed for answering questions from the "Concepts of Biology" textbook. It utilizes a Docker container to run the application.

## Instructions

Before running the application, please download the [Concepts of Biology PDF](https://openstax.org/details/books/concepts-biology) and place it in the same directory as this README.

### Building the Docker Image

```bash
docker build -t gradio-app:latest .

docker run -d -it --privileged --net=host -e DISPLAY=unix$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix --name RAG-app gradio-app:latest
```

The gradio-app is integrated with gradio which give the link to run the QA chatbot.

### Colab Link
[Google Colab Notebook](https://colab.research.google.com/drive/1yo12IKDokIp7HhpJ4B4At3uOIDtmsK-j#scrollTo=ilAPBJ2KC0Il)


### areas to improve are 

1) To improve the retrieval process, we could have extracted metadata from chunks of text, and used it for keyword retrieval like BM25 along with dense vector embeddings.
2) To improve the inference time, we could have used ctransformer or vLLM (paged attention) for the LLM model.
3) Experiment with many new models like "openchat 3.5" etc for better answers.
4) Due to time constraint not able to add API's.
