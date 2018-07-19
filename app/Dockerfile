FROM alpine

RUN apk add --no-cache git

RUN git clone https://github.com/Microsoft/monaco-editor-samples.git

FROM node:slim

COPY --from=0  monaco-editor-samples monaco-editor-samples

WORKDIR monaco-editor-samples
RUN npm install .

EXPOSE 8888

ENTRYPOINT ["npm", "run", "simpleserver"]

