FROM oven/bun:1 AS base

COPY . .

RUN chown -R bun:bun /home/bun/app
USER bun

RUN bun install
RUN bunx --bun vite build

EXPOSE 5173/tcp
ENTRYPOINT [ "bun", "run", "dev", "--host=0.0.0.0" ]

