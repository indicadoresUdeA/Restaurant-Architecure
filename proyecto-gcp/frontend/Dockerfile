FROM nginx:alpine AS base
COPY static/ /usr/share/nginx/html/
ENV PORT=80

# Development stage
FROM base AS dev
ENV ENVIRONMENT=dev

# QA stage
FROM base AS qa
ENV ENVIRONMENT=qa

# Production stage (default)
FROM base AS prod
ENV ENVIRONMENT=prod

CMD ["nginx", "-g", "daemon off;"]
