# Fixes to SMUI

It is widely known that SMUI is broken with SvelteKit/PNPM.

You get `can't find stylesheet to import` errors regarding various sub-modules in material.

To get around this you have to manually install those missing sub-modules `@material/*` into the top level node_modules.

For more info on the workaround, see [issue-348](https://github.com/hperrin/svelte-material-ui/issues/348)

I repeatedly ran

    pnpm run prepare

and then

    pnpm i -d @material/[name]

for whatever came up as missing for the prepare.

I only added enough to get Button, Card and Drawer working.
