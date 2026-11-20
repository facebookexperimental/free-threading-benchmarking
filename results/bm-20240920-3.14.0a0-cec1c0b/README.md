# Results

- fork: mpage/cec1c0b3fa171b6ab3ca
- version: 3.14.0a0
- config: 
- commit hash: [cec1c0b](https://github.com/mpage/cpython/commit/cec1c0b)
- commit date: 2024-09-20T16:53:55-07:00
- commit merge base: [342e654b8eda24c68da64cc21bc9583e480d9e8e](https://github.com/python/cpython/commit/342e654b8eda24c68da64cc21bc9583e480d9e8e)
- ref: cec1c0b3fa171b6ab3ca

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10970083145)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b-vs-3.12.6.md)
- [📈time plot](bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b-vs-3.13.0rc2.md)
- [📈time plot](bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 91.01%, 1.00x slower at 99th %ile)
- Memory usage: 0.86x
- new benchmarks: 2to3, async_generators, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, bench_mp_pool, bench_thread_pool, bpe_tokeniser, chaos, comprehensions, coroutines, coverage, create_gc_cycles, crypto_pyaes, deepcopy, deepcopy_memo, deepcopy_reduce, django_template, docutils, dulwich_log, fannkuch, float, gc_traversal, generators, genshi_text, genshi_xml, go, hexiom, html5lib, json, json_dumps, json_loads, logging_format, logging_silent, logging_simple, mako, mdp, meteor_contest, nbody, nqueens, pathlib, pickle, pickle_dict, pickle_list, pickle_pure_python, pidigits, pprint_pformat, pprint_safe_repr, pycparser, pyflate, pylint, python_startup, python_startup_no_site, raytrace, regex_compile, regex_dna, regex_effbot, regex_v8, richards_super, scimark_fft, scimark_lu, scimark_monte_carlo, scimark_sor, scimark_sparse_mat_mult, spectral_norm, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sqlite_synth, sympy_expand, sympy_integrate, sympy_str, sympy_sum, telco, thrift, tomli_loads, tornado_http, typing_runtime_protocols, unpack_sequence, unpickle, unpickle_list, unpickle_pure_python, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process
- [🧠memory plot](bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b-vs-base-mem.svg)
- [📄table](bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b-vs-base.md)
- [📈time plot](bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b-vs-base.svg)

