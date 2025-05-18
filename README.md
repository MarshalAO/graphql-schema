# Arweave GraphQL Schemas

The purpose of this repo is to visualize the differences between different GraphQL schemas available in the Arweave ecosystem.

Most importantly, let's see the differences between [arweave.net](https://arweave.net/graphql) and [arweave-search.goldsky.com](https://arweave-search.goldsky.com/graphql).

## Dates of Schemas in this Repo

All schemas were fetched around 2025-05-18T03:00:00Z.

## Branches in this Repo

There is a branch for each GraphQL server we are interested in.

This is so that you can quickly compare (i.e. `diff`) the gateways you are interested in.

## Type of Schemas in this Repo

`raw` - The exact `schema.graphql` file that you get if you download the SDL from the GraphQL playground.

`sorted` - A simple re-ordering of the `raw` schema, in the following order:

- Copyright/licensing info
- GraphQL `directive`s, in alphabetical order.
- GraphQL `enum`s, in alphabetical order.
- GraphQL `input`s, in alphabetical order.
- GraphQL `type`s, in alphabetical order (excluding the `Query` type).
- The `Query` type.

Additionally: Ensure one blank line between top-level elements, ensure one blank line between fields/params, sort fields/params alphabetically, and retain comments at every level.

`compact` - Strip all comments and collapse blank lines between fields/params from the `sorted` schema. Produces the cleanest diffs.
