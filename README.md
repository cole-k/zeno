# zeno

This is a repository based off of the copy of [Zeno on Hackage](https://hackage.haskell.org/package/zeno)
with modifications to get it to run on modern versions of GHC.

For more info on the Zeno theorem prover, see its [wiki page](https://wiki.haskell.org/Zeno).

# Prereqs

1. Install GHC 8.10 (I recommend using [GHCup](https://www.haskell.org/ghcup/))

# Building

``` shell
cabal build zeno
```

# Running

``` shell
cabal run zeno -- file [flags]
```

I recommend adding the `-I` flag unless you have Isabelle installed. I did
not check that the 12-year-old Isabelle output is valid.

Prove insertion sort sorts a list from the included file `Example.hs`:

``` shell
cabal run zeno -- -m insert_sorts -I Example.hs
```

# Installing

``` shell
cabal install zeno
```

This will install the `zeno` executable for you to use. You may need to update
your path to include wherever cabal installs (although GHCup probably should do
that for you).
