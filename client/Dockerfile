ARG NODE_VERSION=16.13.0

FROM node:${NODE_VERSION}-alpine AS build

ENV NODE_ENV production

WORKDIR /21I-1103_frontend

RUN --mount=type=bind,source=package.json,target=package.json \
    --mount=type=bind,source=package-lock.json,target=package-lock.json \
    --mount=type=cache,target=/root/.npm \
    npm ci --omit=dev

# Change ownership of the /21I-1103_frontend directory to the node user
RUN chown -R node:node /21I-1103_frontend

USER node

COPY . .

RUN npm run build

FROM nginx:alpine

COPY --from=build /21I-1103_frontend/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
