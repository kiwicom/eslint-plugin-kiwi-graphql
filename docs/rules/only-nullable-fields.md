# only-nullable-fields

This rule aims to remove all uses of `GraphQLNonNull` on GraphQL type fields. Why? It's best practice to use nullable
fields and not rely on returned value. This way every frontend implementation must handle the situation when API
returns `null` because everything will break eventually.

## Rule Details

Examples of **incorrect** code for this rule:

```js
arrival: {
  type: new GraphQLNonNull(GraphQLRouteStop),
  resolve: ({ arrival }: LegType): ArrivalType => arrival,
},
```

Examples of **correct** code for this rule:

```js
arrival: {
  type: GraphQLRouteStop,
  resolve: ({ arrival }: LegType): ArrivalType => arrival,
},
```
