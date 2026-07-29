# Axis Metal Works

Parent repo tying together the two Axis Metal Works projects. Each lives in
its own repo and is pulled in here as a git submodule.

- [`axis-metal-works-pricing`](https://github.com/nick-zanobini/axis-metal-works-pricing) —
  the internal desktop pricing calculator (PySide6 app + Windows installer).
- [`axis-metal-works-website`](https://github.com/nick-zanobini/axis-metal-works-website) —
  the public marketing site.

## Cloning

```
git clone --recurse-submodules https://github.com/nick-zanobini/axis-metal-works.git
```

If you already cloned without `--recurse-submodules`:

```
git submodule update --init --recursive
```

## Pulling in submodule updates

Each submodule is pinned to a specific commit of its own repo. To bump a
submodule to its latest commit:

```
git submodule update --remote pricing-calculator
git submodule update --remote website
git add pricing-calculator website
git commit -m "Bump submodules"
```
