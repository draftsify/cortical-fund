# Cortical Fund

Landing page for **Cortical Fund** — an independent protocol that routes on-chain
trading fees into research contributions for [Cortical Labs](https://corticallabs.com),
the lab building CL1, a computer that runs on living human neurons.

Single self-contained `index.html`. No build step, no dependencies.

## Editing

All the numbers live in one config object at the top of the `<script>` block:

```js
const CFG = {
  contributed : 128450,   // $ wired to Cortical Labs
  feesTotal   : 141900,   // $ total pool fees generated
  cl1Price    : 35000,    // $ per CL1 unit
  neuronHour  : 0.42,     // $ per neuron-hour of compute
  liveDrip    : true      // slow live increments
};
```

Everything else — the CL1 progress bar, the unit count, the neuron-hours — is derived.

Other placeholders to replace before going live:

| What | Where |
|---|---|
| Contract address | FAQ, `0x000…000` |
| Ledger rows | `ROWS` array in the script |
| Buy button links | `href="#"` on the `.btn-a` elements |

## Hero

The hero animation is a generative ASCII neural field rendered at ~18fps into a
`<pre>`: 15 nodes, 24 synapses, and pulses travelling along each edge. No images,
no canvas, no libraries.

## Disclaimer

Cortical Fund is an independent project. It is not affiliated with, endorsed by,
sponsored by, or operated by Cortical Labs Pty Ltd.
