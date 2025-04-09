# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_XXX_noinline
- machine: linux-x86_64
- commit hash: a851750
- commit date: 2025-04-09
- overall geometric mean: 1.074x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 246 ms: 1.05x faster                                             |
| docutils       | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                           |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 603 ms: 1.49x faster                                             |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                             |
| async_tree_io              | 881 ms                                                                 | 608 ms: 1.45x faster                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 498 ms: 1.34x faster                                             |
| async_tree_memoization_tg  | 410 ms                                                                 | 315 ms: 1.30x faster                                             |
| async_tree_none_tg         | 333 ms                                                                 | 256 ms: 1.30x faster                                             |
| async_tree_none            | 353 ms                                                                 | 273 ms: 1.29x faster                                             |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 492 ms: 1.29x faster                                             |
| async_generators           | 375 ms                                                                 | 325 ms: 1.15x faster                                             |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                     |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 69.2 ms: 1.11x faster                                            |
| pidigits       | 216 ms                                                                 | 201 ms: 1.07x faster                                             |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                            |
| regex_compile  | 131 ms                                                                 | 123 ms: 1.07x faster                                             |
| regex_v8       | 23.2 ms                                                                | 22.1 ms: 1.05x faster                                            |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                             |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.89 sec: 1.07x faster                                           |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                             |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                            |
| xml_etree_generate   | 85.4 ms                                                                | 83.9 ms: 1.02x faster                                            |
| unpickle_pure_python | 208 us                                                                 | 212 us: 1.02x slower                                             |
| json_loads           | 27.3 us                                                                | 28.3 us: 1.04x slower                                            |
| pickle_pure_python   | 292 us                                                                 | 303 us: 1.04x slower                                             |
| json_dumps           | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                     |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.62 ms: 1.16x slower                                            |
| python_startup         | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                            |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.3 ms: 1.07x faster                                            |
| genshi_xml      | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                            |
| django_template | 34.2 ms                                                                | 34.9 ms: 1.02x slower                                            |
| mako            | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                            |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.06x faster                                           |
| async_tree_io_tg           | 901 ms                                                                 | 603 ms: 1.49x faster                                             |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                             |
| async_tree_io              | 881 ms                                                                 | 608 ms: 1.45x faster                                             |
| deepcopy                   | 357 us                                                                 | 251 us: 1.42x faster                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 498 ms: 1.34x faster                                             |
| go                         | 141 ms                                                                 | 106 ms: 1.33x faster                                             |
| async_tree_memoization_tg  | 410 ms                                                                 | 315 ms: 1.30x faster                                             |
| async_tree_none_tg         | 333 ms                                                                 | 256 ms: 1.30x faster                                             |
| async_tree_none            | 353 ms                                                                 | 273 ms: 1.29x faster                                             |
| deepcopy_memo              | 38.1 us                                                                | 29.5 us: 1.29x faster                                            |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 492 ms: 1.29x faster                                             |
| scimark_sor                | 134 ms                                                                 | 108 ms: 1.23x faster                                             |
| deepcopy_reduce            | 3.12 us                                                                | 2.65 us: 1.18x faster                                            |
| spectral_norm              | 108 ms                                                                 | 91.3 ms: 1.18x faster                                            |
| async_generators           | 375 ms                                                                 | 325 ms: 1.15x faster                                             |
| pylint                     | 317 ms                                                                 | 277 ms: 1.14x faster                                             |
| regex_effbot               | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                            |
| pyflate                    | 449 ms                                                                 | 398 ms: 1.13x faster                                             |
| scimark_fft                | 348 ms                                                                 | 309 ms: 1.13x faster                                             |
| dulwich_log                | 74.5 ms                                                                | 67.0 ms: 1.11x faster                                            |
| float                      | 76.7 ms                                                                | 69.2 ms: 1.11x faster                                            |
| scimark_monte_carlo        | 65.8 ms                                                                | 60.0 ms: 1.10x faster                                            |
| richards                   | 44.4 ms                                                                | 40.7 ms: 1.09x faster                                            |
| telco                      | 7.77 ms                                                                | 7.15 ms: 1.09x faster                                            |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.37 ms: 1.09x faster                                            |
| richards_super             | 50.4 ms                                                                | 46.8 ms: 1.08x faster                                            |
| pidigits                   | 216 ms                                                                 | 201 ms: 1.07x faster                                             |
| regex_compile              | 131 ms                                                                 | 123 ms: 1.07x faster                                             |
| chaos                      | 56.3 ms                                                                | 52.6 ms: 1.07x faster                                            |
| genshi_text                | 21.7 ms                                                                | 20.3 ms: 1.07x faster                                            |
| tomli_loads                | 2.01 sec                                                               | 1.89 sec: 1.07x faster                                           |
| generators                 | 28.5 ms                                                                | 26.8 ms: 1.06x faster                                            |
| bpe_tokeniser              | 4.46 sec                                                               | 4.20 sec: 1.06x faster                                           |
| hexiom                     | 5.95 ms                                                                | 5.64 ms: 1.06x faster                                            |
| 2to3                       | 259 ms                                                                 | 246 ms: 1.05x faster                                             |
| regex_v8                   | 23.2 ms                                                                | 22.1 ms: 1.05x faster                                            |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                             |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                             |
| logging_format             | 6.92 us                                                                | 6.63 us: 1.04x faster                                            |
| docutils                   | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                           |
| sympy_integrate            | 19.7 ms                                                                | 19.0 ms: 1.04x faster                                            |
| coverage                   | 82.5 ms                                                                | 79.7 ms: 1.04x faster                                            |
| genshi_xml                 | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                            |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                            |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.03x faster                                           |
| logging_simple             | 6.14 us                                                                | 5.99 us: 1.03x faster                                            |
| meteor_contest             | 101 ms                                                                 | 99.2 ms: 1.02x faster                                            |
| nqueens                    | 77.7 ms                                                                | 76.1 ms: 1.02x faster                                            |
| pathlib                    | 19.3 ms                                                                | 18.9 ms: 1.02x faster                                            |
| xml_etree_generate         | 85.4 ms                                                                | 83.9 ms: 1.02x faster                                            |
| crypto_pyaes               | 68.2 ms                                                                | 67.1 ms: 1.02x faster                                            |
| pprint_safe_repr           | 719 ms                                                                 | 707 ms: 1.02x faster                                             |
| sqlite_synth               | 2.25 us                                                                | 2.22 us: 1.01x faster                                            |
| raytrace                   | 250 ms                                                                 | 246 ms: 1.01x faster                                             |
| sympy_str                  | 274 ms                                                                 | 271 ms: 1.01x faster                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.44 sec: 1.01x faster                                           |
| logging_silent             | 98.2 ns                                                                | 97.4 ns: 1.01x faster                                            |
| comprehensions             | 16.6 us                                                                | 16.6 us: 1.00x slower                                            |
| scimark_lu                 | 112 ms                                                                 | 113 ms: 1.01x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 157 us: 1.01x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 212 us: 1.02x slower                                             |
| django_template            | 34.2 ms                                                                | 34.9 ms: 1.02x slower                                            |
| json                       | 4.98 ms                                                                | 5.12 ms: 1.03x slower                                            |
| json_loads                 | 27.3 us                                                                | 28.3 us: 1.04x slower                                            |
| deltablue                  | 3.10 ms                                                                | 3.21 ms: 1.04x slower                                            |
| pickle_pure_python         | 292 us                                                                 | 303 us: 1.04x slower                                             |
| json_dumps                 | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                            |
| mako                       | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                            |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.13x slower                                            |
| python_startup_no_site     | 7.41 ms                                                                | 8.62 ms: 1.16x slower                                            |
| gc_traversal               | 3.32 ms                                                                | 4.19 ms: 1.26x slower                                            |
| python_startup             | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                            |
| create_gc_cycles           | 1.33 ms                                                                | 1.85 ms: 1.39x slower                                            |
| bench_mp_pool              | 11.0 ms                                                                | 88.2 ms: 8.02x slower                                            |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                     |

Benchmark hidden because not significant (7): nbody, xml_etree_process, fannkuch, asyncio_websockets, sympy_sum, coroutines, sympy_expand
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250409-3.14.0a7+-a851750/bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.13x