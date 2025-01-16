# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 65a6ad3
- commit date: 2025-01-16
- overall geometric mean: 1.090x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 306 ms: 1.18x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                                |
| html5lib       | 67.0 ms                                                      | 70.9 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 583 ms: 1.57x faster                                                  |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 499 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 540 ms: 1.23x faster                                                  |
| async_generators           | 377 ms                                                       | 367 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 209 ms: 1.04x faster                                                  |
| float          | 77.5 ms                                                      | 78.5 ms: 1.01x slower                                                 |
| nbody          | 85.1 ms                                                      | 135 ms: 1.58x slower                                                  |
| Geometric mean | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.82 ms: 1.10x faster                                                 |
| regex_dna      | 180 ms                                                       | 183 ms: 1.01x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                 |
| regex_compile  | 132 ms                                                       | 152 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.0 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.4 ms: 1.13x slower                                                 |
| json_loads           | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.35 sec: 1.17x slower                                                |
| unpickle_pure_python | 210 us                                                       | 252 us: 1.20x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 13.0 ms: 1.24x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 377 us: 1.28x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.54 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.2 ms: 1.39x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.4 ms: 1.24x slower                                                 |
| django_template | 34.1 ms                                                      | 43.0 ms: 1.26x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 28.2 ms: 1.31x slower                                                 |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 583 ms: 1.57x faster                                                  |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 499 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 540 ms: 1.23x faster                                                  |
| deepcopy                   | 355 us                                                       | 316 us: 1.13x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.82 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.0 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                  |
| pidigits                   | 217 ms                                                       | 209 ms: 1.04x faster                                                  |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                                  |
| async_generators           | 377 ms                                                       | 367 ms: 1.03x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.7 ms: 1.03x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                  |
| scimark_sor                | 134 ms                                                       | 133 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.32 ms: 1.01x faster                                                 |
| go                         | 141 ms                                                       | 139 ms: 1.01x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.13 ms: 1.00x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 39.3 us: 1.01x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| float                      | 77.5 ms                                                      | 78.5 ms: 1.01x slower                                                 |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.01x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 70.9 ms: 1.06x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.74 sec: 1.07x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.07x slower                                                |
| deepcopy_reduce            | 3.11 us                                                      | 3.33 us: 1.07x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                                |
| json                       | 4.93 ms                                                      | 5.33 ms: 1.08x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.52 ms: 1.09x slower                                                 |
| generators                 | 28.8 ms                                                      | 31.5 ms: 1.09x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 82.1 ms: 1.10x slower                                                 |
| scimark_fft                | 349 ms                                                       | 387 ms: 1.11x slower                                                  |
| pyflate                    | 449 ms                                                       | 502 ms: 1.12x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 828 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 96.4 ms: 1.13x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.14x slower                                                |
| json_loads                 | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| logging_silent             | 103 ns                                                       | 118 ns: 1.15x slower                                                  |
| regex_compile              | 132 ms                                                       | 152 ms: 1.15x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 122 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.35 sec: 1.17x slower                                                |
| thrift                     | 778 us                                                       | 914 us: 1.17x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.77 sec: 1.18x slower                                                |
| 2to3                       | 260 ms                                                       | 306 ms: 1.18x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 62.1 ms: 1.18x slower                                                 |
| coverage                   | 83.0 ms                                                      | 97.9 ms: 1.18x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.63 ms: 1.20x slower                                                 |
| logging_simple             | 6.16 us                                                      | 7.37 us: 1.20x slower                                                 |
| chaos                      | 57.3 ms                                                      | 68.7 ms: 1.20x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 252 us: 1.20x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 188 ms: 1.21x slower                                                  |
| sympy_expand               | 457 ms                                                       | 552 ms: 1.21x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 24.3 ms: 1.22x slower                                                 |
| sympy_str                  | 275 ms                                                       | 336 ms: 1.23x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 138 ms: 1.23x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.43 us: 1.23x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 96.9 ms: 1.23x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 13.0 ms: 1.24x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 60.4 ms: 1.24x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.44 ms: 1.24x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 82.2 ms: 1.26x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.96 ms: 1.26x slower                                                 |
| django_template            | 34.1 ms                                                      | 43.0 ms: 1.26x slower                                                 |
| richards                   | 45.2 ms                                                      | 57.3 ms: 1.27x slower                                                 |
| comprehensions             | 16.5 us                                                      | 20.9 us: 1.27x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 377 us: 1.28x slower                                                  |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.54 ms: 1.29x slower                                                 |
| richards_super             | 51.6 ms                                                      | 66.9 ms: 1.30x slower                                                 |
| fannkuch                   | 370 ms                                                       | 480 ms: 1.30x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 88.3 ms: 1.30x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.63 ms: 1.30x slower                                                 |
| raytrace                   | 253 ms                                                       | 330 ms: 1.31x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 28.2 ms: 1.31x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 204 us: 1.32x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.2 ms: 1.39x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 4.66 ms: 1.49x slower                                                 |
| nbody                      | 85.1 ms                                                      | 135 ms: 1.58x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.33 ms: 3.62x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 94.7 ms: 8.61x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250116-3.14.0a4+-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x