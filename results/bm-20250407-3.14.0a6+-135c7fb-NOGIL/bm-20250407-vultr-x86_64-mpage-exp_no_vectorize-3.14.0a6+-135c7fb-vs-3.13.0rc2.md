# Results vs. 3.13.0rc2

- fork: mpage
- ref: exp_no_vectorize
- machine: linux-x86_64
- commit hash: 135c7fb
- commit date: 2025-04-07
- overall geometric mean: 1.043x slower
- HPT reliability: 99.05%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 291 ms: 1.12x slower                                              |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                            |
| html5lib       | 68.6 ms                                                                | 68.2 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 534 ms: 1.69x faster                                              |
| async_tree_io              | 881 ms                                                                 | 567 ms: 1.56x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.42x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 325 ms: 1.41x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 295 ms: 1.39x faster                                              |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 486 ms: 1.30x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 514 ms: 1.30x faster                                              |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                             |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.29x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 198 ms: 1.09x faster                                              |
| float          | 76.7 ms                                                                | 73.1 ms: 1.05x faster                                             |
| nbody          | 85.3 ms                                                                | 120 ms: 1.41x slower                                              |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                             |
| regex_v8       | 23.2 ms                                                                | 20.7 ms: 1.12x faster                                             |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                              |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                              |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.8 ms: 1.07x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| json_loads           | 27.3 us                                                                | 29.5 us: 1.08x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.28 sec: 1.13x slower                                            |
| xml_etree_generate   | 85.4 ms                                                                | 96.8 ms: 1.13x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 245 us: 1.18x slower                                              |
| xml_etree_process    | 59.2 ms                                                                | 70.4 ms: 1.19x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 348 us: 1.19x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                             |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.48x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.3 ms: 1.21x slower                                             |
| django_template | 34.2 ms                                                                | 42.0 ms: 1.23x slower                                             |
| genshi_text     | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                             |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.86x faster                                             |
| mdp                        | 2.34 sec                                                               | 1.36 sec: 1.72x faster                                            |
| async_tree_io_tg           | 901 ms                                                                 | 534 ms: 1.69x faster                                              |
| async_tree_io              | 881 ms                                                                 | 567 ms: 1.56x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 234 ms: 1.42x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 325 ms: 1.41x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 295 ms: 1.39x faster                                              |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 486 ms: 1.30x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 514 ms: 1.30x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                             |
| deepcopy                   | 357 us                                                                 | 302 us: 1.18x faster                                              |
| regex_v8                   | 23.2 ms                                                                | 20.7 ms: 1.12x faster                                             |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                             |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.09x faster                                              |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                              |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.8 ms: 1.07x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| float                      | 76.7 ms                                                                | 73.1 ms: 1.05x faster                                             |
| deepcopy_reduce            | 3.12 us                                                                | 3.02 us: 1.03x faster                                             |
| go                         | 141 ms                                                                 | 136 ms: 1.03x faster                                              |
| dulwich_log                | 74.5 ms                                                                | 72.7 ms: 1.02x faster                                             |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                              |
| deepcopy_memo              | 38.1 us                                                                | 37.5 us: 1.01x faster                                             |
| scimark_sor                | 134 ms                                                                 | 132 ms: 1.01x faster                                              |
| html5lib                   | 68.6 ms                                                                | 68.2 ms: 1.01x faster                                             |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                             |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                              |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.01x slower                                              |
| json                       | 4.98 ms                                                                | 5.04 ms: 1.01x slower                                             |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                             |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                             |
| scimark_fft                | 348 ms                                                                 | 360 ms: 1.03x slower                                              |
| bpe_tokeniser              | 4.46 sec                                                               | 4.70 sec: 1.05x slower                                            |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.06x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                            |
| telco                      | 7.77 ms                                                                | 8.35 ms: 1.07x slower                                             |
| json_loads                 | 27.3 us                                                                | 29.5 us: 1.08x slower                                             |
| pyflate                    | 449 ms                                                                 | 490 ms: 1.09x slower                                              |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.20 ms: 1.09x slower                                             |
| pprint_safe_repr           | 719 ms                                                                 | 803 ms: 1.12x slower                                              |
| 2to3                       | 259 ms                                                                 | 291 ms: 1.12x slower                                              |
| tomli_loads                | 2.01 sec                                                               | 2.28 sec: 1.13x slower                                            |
| xml_etree_generate         | 85.4 ms                                                                | 96.8 ms: 1.13x slower                                             |
| logging_silent             | 98.2 ns                                                                | 113 ns: 1.15x slower                                              |
| nqueens                    | 77.7 ms                                                                | 89.3 ms: 1.15x slower                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.68 sec: 1.16x slower                                            |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                              |
| chaos                      | 56.3 ms                                                                | 65.4 ms: 1.16x slower                                             |
| generators                 | 28.5 ms                                                                | 33.3 ms: 1.17x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.3 ms: 1.17x slower                                             |
| sympy_integrate            | 19.7 ms                                                                | 23.2 ms: 1.17x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 245 us: 1.18x slower                                              |
| logging_simple             | 6.14 us                                                                | 7.26 us: 1.18x slower                                             |
| logging_format             | 6.92 us                                                                | 8.20 us: 1.19x slower                                             |
| xml_etree_process          | 59.2 ms                                                                | 70.4 ms: 1.19x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 134 ms: 1.19x slower                                              |
| pickle_pure_python         | 292 us                                                                 | 348 us: 1.19x slower                                              |
| sympy_expand               | 454 ms                                                                 | 543 ms: 1.20x slower                                              |
| sympy_str                  | 274 ms                                                                 | 328 ms: 1.20x slower                                              |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.20x slower                                              |
| genshi_xml                 | 49.1 ms                                                                | 59.3 ms: 1.21x slower                                             |
| hexiom                     | 5.95 ms                                                                | 7.26 ms: 1.22x slower                                             |
| django_template            | 34.2 ms                                                                | 42.0 ms: 1.23x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.80 ms: 1.23x slower                                             |
| raytrace                   | 250 ms                                                                 | 309 ms: 1.24x slower                                              |
| richards                   | 44.4 ms                                                                | 55.0 ms: 1.24x slower                                             |
| fannkuch                   | 376 ms                                                                 | 467 ms: 1.24x slower                                              |
| comprehensions             | 16.6 us                                                                | 20.6 us: 1.24x slower                                             |
| richards_super             | 50.4 ms                                                                | 63.2 ms: 1.25x slower                                             |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                              |
| crypto_pyaes               | 68.2 ms                                                                | 86.3 ms: 1.27x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 200 us: 1.28x slower                                              |
| genshi_text                | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                             |
| coverage                   | 82.5 ms                                                                | 108 ms: 1.31x slower                                              |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                             |
| nbody                      | 85.3 ms                                                                | 120 ms: 1.41x slower                                              |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                             |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                             |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.42x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 96.2 ms: 8.75x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250407-3.14.0a6+-135c7fb-NOGIL/bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.043x slower

# HPT report

- Reliability score: 99.05% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x