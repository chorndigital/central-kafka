# Kafka Agent Guide

This repository lives at `C:\Projects\smartfood-system\kafka` and provides shared messaging infrastructure for the Smartfood workspace.

## Purpose

- Run ZooKeeper, Kafka, and Kafdrop for local or staging-style integration.
- Provide the broker endpoint used by other services as `kafka:9092` on the Docker network.
- Support future event-driven integration even though Kafka is not yet the primary active business path.

## Current Runtime

- `zookeeper` host port `12181`
- `kafka` host port `19092`
- `kafdrop` host port `19000`
- Docker network: external `shared-net`

## Working Rules

- Prefer minimal changes to image versions, listener configuration, and port mapping.
- Treat broker names, container names, and advertised listeners as contract surfaces for other repos.
- Update docs when changing topics, listeners, ports, or bootstrap addresses.
- Verify Compose config before making broader claims about integration.

## Key Files

- `docker-compose.yml`
- `README.md`

## Verification

- `docker compose config`
- `docker compose ps`
