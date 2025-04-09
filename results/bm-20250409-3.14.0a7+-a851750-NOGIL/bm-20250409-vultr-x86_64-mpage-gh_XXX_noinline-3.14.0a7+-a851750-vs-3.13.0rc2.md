# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_XXX_noinline
- machine: linux-x86_64
- commit hash: a851750
- commit date: 2025-04-09
- overall geometric mean: 1.001x slower
- HPT reliability: 92.74%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 279 ms: 1.08x slower                                             |
| docutils       | 2.63 sec                                                               | 2.69 sec: 1.03x slower                                           |
| html5lib       | 68.6 ms                                                                | 64.8 ms: 1.06x faster                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 513 ms: 1.76x faster                                             |
| async_tree_io              | 881 ms                                                                 | 538 ms: 1.64x faster                                             |
| async_tree_none_tg         | 333 ms                                                                 | 223 ms: 1.50x faster                                             |
| async_tree_memoization     | 459 ms                                                                 | 307 ms: 1.50x faster                                             |
| async_tree_memoization_tg  | 410 ms                                                                 | 278 ms: 1.47x faster                                             |
| async_tree_none            | 353 ms                                                                 | 254 ms: 1.39x faster                                             |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 515 ms: 1.23x faster                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 542 ms: 1.23x faster                                             |
| async_generators           | 375 ms                                                                 | 356 ms: 1.05x faster                                             |
| coroutines                 | 23.3 ms                                                                | 22.4 ms: 1.04x faster                                            |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                             |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.3 ms: 1.14x faster                                            |
| pidigits       | 216 ms                                                                 | 222 ms: 1.03x slower                                             |
| nbody          | 85.3 ms                                                                | 109 ms: 1.27x slower                                             |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                            |
| regex_dna      | 189 ms                                                                 | 174 ms: 1.09x faster                                             |
| regex_v8       | 23.2 ms                                                                | 22.0 ms: 1.06x faster                                            |
| regex_compile  | 131 ms                                                                 | 142 ms: 1.08x slower                                             |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 83.9 ms: 1.13x faster                                            |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                             |
| tomli_loads          | 2.01 sec                                                               | 2.09 sec: 1.04x slower                                           |
| xml_etree_generate   | 85.4 ms                                                                | 91.9 ms: 1.08x slower                                            |
| unpickle_pure_python | 208 us                                                                 | 224 us: 1.08x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 323 us: 1.11x slower                                             |
| xml_etree_process    | 59.2 ms                                                                | 65.6 ms: 1.11x slower                                            |
| json_loads           | 27.3 us                                                                | 30.7 us: 1.12x slower                                            |
| json_dumps           | 10.6 ms                                                                | 12.6 ms: 1.18x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                            |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                            |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 54.9 ms: 1.12x slower                                            |
| django_template | 34.2 ms                                                                | 39.6 ms: 1.16x slower                                            |
| genshi_text     | 21.7 ms                                                                | 25.6 ms: 1.18x slower                                            |
| mako            | 11.2 ms                                                                | 15.0 ms: 1.33x slower                                            |
| Geometric mean  | (ref)                                                                  | 1.19x slower                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.87x faster                                            |
| mdp                        | 2.34 sec                                                               | 1.29 sec: 1.81x faster                                           |
| async_tree_io_tg           | 901 ms                                                                 | 513 ms: 1.76x faster                                             |
| async_tree_io              | 881 ms                                                                 | 538 ms: 1.64x faster                                             |
| async_tree_none_tg         | 333 ms                                                                 | 223 ms: 1.50x faster                                             |
| async_tree_memoization     | 459 ms                                                                 | 307 ms: 1.50x faster                                             |
| async_tree_memoization_tg  | 410 ms                                                                 | 278 ms: 1.47x faster                                             |
| async_tree_none            | 353 ms                                                                 | 254 ms: 1.39x faster                                             |
| deepcopy                   | 357 us                                                                 | 285 us: 1.25x faster                                             |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 515 ms: 1.23x faster                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 542 ms: 1.23x faster                                             |
| float                      | 76.7 ms                                                                | 67.3 ms: 1.14x faster                                            |
| go                         | 141 ms                                                                 | 124 ms: 1.14x faster                                             |
| regex_effbot               | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                            |
| xml_etree_iterparse        | 94.4 ms                                                                | 83.9 ms: 1.13x faster                                            |
| sqlite_synth               | 2.25 us                                                                | 2.00 us: 1.12x faster                                            |
| scimark_sor                | 134 ms                                                                 | 119 ms: 1.12x faster                                             |
| deepcopy_memo              | 38.1 us                                                                | 34.9 us: 1.09x faster                                            |
| regex_dna                  | 189 ms                                                                 | 174 ms: 1.09x faster                                             |
| spectral_norm              | 108 ms                                                                 | 100 ms: 1.07x faster                                             |
| deepcopy_reduce            | 3.12 us                                                                | 2.91 us: 1.07x faster                                            |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                             |
| html5lib                   | 68.6 ms                                                                | 64.8 ms: 1.06x faster                                            |
| regex_v8                   | 23.2 ms                                                                | 22.0 ms: 1.06x faster                                            |
| async_generators           | 375 ms                                                                 | 356 ms: 1.05x faster                                             |
| dulwich_log                | 74.5 ms                                                                | 70.8 ms: 1.05x faster                                            |
| scimark_fft                | 348 ms                                                                 | 335 ms: 1.04x faster                                             |
| coroutines                 | 23.3 ms                                                                | 22.4 ms: 1.04x faster                                            |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.47 sec: 1.00x slower                                           |
| logging_silent             | 98.2 ns                                                                | 99.0 ns: 1.01x slower                                            |
| pyflate                    | 449 ms                                                                 | 456 ms: 1.01x slower                                             |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                           |
| docutils                   | 2.63 sec                                                               | 2.69 sec: 1.03x slower                                           |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.87 ms: 1.03x slower                                            |
| pidigits                   | 216 ms                                                                 | 222 ms: 1.03x slower                                             |
| generators                 | 28.5 ms                                                                | 29.4 ms: 1.03x slower                                            |
| tomli_loads                | 2.01 sec                                                               | 2.09 sec: 1.04x slower                                           |
| pprint_safe_repr           | 719 ms                                                                 | 755 ms: 1.05x slower                                             |
| json                       | 4.98 ms                                                                | 5.26 ms: 1.05x slower                                            |
| telco                      | 7.77 ms                                                                | 8.29 ms: 1.07x slower                                            |
| chaos                      | 56.3 ms                                                                | 60.4 ms: 1.07x slower                                            |
| 2to3                       | 259 ms                                                                 | 279 ms: 1.08x slower                                             |
| xml_etree_generate         | 85.4 ms                                                                | 91.9 ms: 1.08x slower                                            |
| unpickle_pure_python       | 208 us                                                                 | 224 us: 1.08x slower                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.57 sec: 1.08x slower                                           |
| nqueens                    | 77.7 ms                                                                | 84.0 ms: 1.08x slower                                            |
| regex_compile              | 131 ms                                                                 | 142 ms: 1.08x slower                                             |
| hexiom                     | 5.95 ms                                                                | 6.48 ms: 1.09x slower                                            |
| pickle_pure_python         | 292 us                                                                 | 323 us: 1.11x slower                                             |
| xml_etree_process          | 59.2 ms                                                                | 65.6 ms: 1.11x slower                                            |
| deltablue                  | 3.10 ms                                                                | 3.46 ms: 1.12x slower                                            |
| scimark_monte_carlo        | 65.8 ms                                                                | 73.5 ms: 1.12x slower                                            |
| genshi_xml                 | 49.1 ms                                                                | 54.9 ms: 1.12x slower                                            |
| json_loads                 | 27.3 us                                                                | 30.7 us: 1.12x slower                                            |
| sympy_integrate            | 19.7 ms                                                                | 22.2 ms: 1.12x slower                                            |
| scimark_lu                 | 112 ms                                                                 | 127 ms: 1.13x slower                                             |
| richards                   | 44.4 ms                                                                | 50.1 ms: 1.13x slower                                            |
| logging_format             | 6.92 us                                                                | 7.83 us: 1.13x slower                                            |
| logging_simple             | 6.14 us                                                                | 6.95 us: 1.13x slower                                            |
| raytrace                   | 250 ms                                                                 | 285 ms: 1.14x slower                                             |
| richards_super             | 50.4 ms                                                                | 57.5 ms: 1.14x slower                                            |
| sympy_sum                  | 154 ms                                                                 | 178 ms: 1.15x slower                                             |
| sympy_expand               | 454 ms                                                                 | 524 ms: 1.16x slower                                             |
| sympy_str                  | 274 ms                                                                 | 317 ms: 1.16x slower                                             |
| django_template            | 34.2 ms                                                                | 39.6 ms: 1.16x slower                                            |
| comprehensions             | 16.6 us                                                                | 19.3 us: 1.16x slower                                            |
| genshi_text                | 21.7 ms                                                                | 25.6 ms: 1.18x slower                                            |
| json_dumps                 | 10.6 ms                                                                | 12.6 ms: 1.18x slower                                            |
| fannkuch                   | 376 ms                                                                 | 446 ms: 1.19x slower                                             |
| crypto_pyaes               | 68.2 ms                                                                | 82.0 ms: 1.20x slower                                            |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.22x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 190 us: 1.22x slower                                             |
| nbody                      | 85.3 ms                                                                | 109 ms: 1.27x slower                                             |
| coverage                   | 82.5 ms                                                                | 108 ms: 1.30x slower                                             |
| mako                       | 11.2 ms                                                                | 15.0 ms: 1.33x slower                                            |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                            |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                            |
| bench_thread_pool          | 924 us                                                                 | 3.13 ms: 3.39x slower                                            |
| bench_mp_pool              | 11.0 ms                                                                | 94.7 ms: 8.61x slower                                            |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                     |

Benchmark hidden because not significant (3): pylint, create_gc_cycles, pathlib
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250409-3.14.0a7+-a851750-NOGIL/bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 92.74% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x