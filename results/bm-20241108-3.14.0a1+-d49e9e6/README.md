# Results

- fork: Eclips4/ft_specialize_unpack
- version: 3.14.0a1+
- config: 
- commit hash: [d49e9e6](https://github.com/Eclips4/cpython/commit/d49e9e6)
- commit date: 2024-11-08T23:57:27+02:00
- commit merge base: [85036c8d612007356d2118eb25b460505078b023](https://github.com/python/cpython/commit/85036c8d612007356d2118eb25b460505078b023)
- ref: ft_specialize_unpack

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11804452687)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 98.49%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-3.12.6.md)
- [📈time plot](bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 77.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-3.13.0rc2.md)
- [📈time plot](bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 93.71%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-base-mem.svg)
- [📄table](bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-base.md)
- [📈time plot](bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-base.svg)

