FROM arm64v8/node:16-bullseye as builder
WORKDIR /usr/src/app

COPY . .

ENV CI=1
RUN corepack enable
RUN yarn install 

RUN cd packages/backend && \
  yarn build && \
  yarn workspaces focus --production