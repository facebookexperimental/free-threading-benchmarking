# Results vs. 3.12.6

- fork: mpage
- ref: measure_lfb
- machine: linux-x86_64
- commit hash: 76fc3d1
- commit date: 2025-03-14
- overall geometric mean: 1.089x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                         |
| docutils       | 2.64 sec                                               | 2.59 sec: 1.02x faster                                       |
| Geometric mean | (ref)                                                  | 1.04x faster                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 614 ms: 1.81x faster                                         |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                         |
| async_tree_io              | 1.08 sec                                               | 618 ms: 1.75x faster                                         |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                         |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                         |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                         |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                         |
| async_generators           | 384 ms                                                 | 329 ms: 1.17x faster                                         |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                        |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                         |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.4 ms: 1.16x faster                                        |
| nbody          | 89.3 ms                                                | 86.0 ms: 1.04x faster                                        |
| pidigits       | 184 ms                                                 | 208 ms: 1.13x slower                                         |
| Geometric mean | (ref)                                                  | 1.02x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                         |
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                        |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                         |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.19x slower                                        |
| Geometric mean | (ref)                                                  | 1.00x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.12x faster                                       |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                         |
| xml_etree_iterparse  | 96.7 ms                                                | 91.6 ms: 1.06x faster                                        |
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                         |
| xml_etree_generate   | 85.2 ms                                                | 83.1 ms: 1.03x faster                                        |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.00x slower                                         |
| json_loads           | 26.5 us                                                | 27.7 us: 1.04x slower                                        |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                        |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                 |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.60 ms: 1.20x slower                                        |
| python_startup         | 9.93 ms                                                | 15.0 ms: 1.51x slower                                        |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                        |
| genshi_xml      | 50.2 ms                                                | 48.8 ms: 1.03x faster                                        |
| django_template | 34.7 ms                                                | 35.5 ms: 1.02x slower                                        |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                        |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 614 ms: 1.81x faster                                         |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                         |
| async_tree_io              | 1.08 sec                                               | 618 ms: 1.75x faster                                         |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                         |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                         |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                         |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                         |
| deepcopy_memo              | 40.3 us                                                | 28.9 us: 1.40x faster                                        |
| deepcopy                   | 352 us                                                 | 252 us: 1.39x faster                                         |
| go                         | 139 ms                                                 | 108 ms: 1.29x faster                                         |
| spectral_norm              | 110 ms                                                 | 91.1 ms: 1.21x faster                                        |
| comprehensions             | 19.8 us                                                | 16.5 us: 1.20x faster                                        |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                         |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                         |
| async_generators           | 384 ms                                                 | 329 ms: 1.17x faster                                         |
| dulwich_log                | 78.9 ms                                                | 67.5 ms: 1.17x faster                                        |
| float                      | 80.8 ms                                                | 69.4 ms: 1.16x faster                                        |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.16x faster                                        |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                        |
| chaos                      | 62.8 ms                                                | 55.2 ms: 1.14x faster                                        |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                         |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                         |
| crypto_pyaes               | 76.6 ms                                                | 68.4 ms: 1.12x faster                                        |
| logging_silent             | 109 ns                                                 | 97.5 ns: 1.12x faster                                        |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.12x faster                                       |
| scimark_monte_carlo        | 68.4 ms                                                | 61.3 ms: 1.12x faster                                        |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                        |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.11x faster                                        |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                        |
| richards                   | 45.9 ms                                                | 41.5 ms: 1.11x faster                                        |
| scimark_fft                | 342 ms                                                 | 309 ms: 1.11x faster                                         |
| sqlglot_parse              | 1.36 ms                                                | 1.23 ms: 1.10x faster                                        |
| pyflate                    | 448 ms                                                 | 406 ms: 1.10x faster                                         |
| bpe_tokeniser              | 4.74 sec                                               | 4.30 sec: 1.10x faster                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 130 ms: 1.10x faster                                         |
| sqlglot_transpile          | 1.67 ms                                                | 1.53 ms: 1.09x faster                                        |
| richards_super             | 51.9 ms                                                | 47.6 ms: 1.09x faster                                        |
| sqlalchemy_imperative      | 21.8 ms                                                | 20.1 ms: 1.08x faster                                        |
| logging_simple             | 6.63 us                                                | 6.12 us: 1.08x faster                                        |
| logging_format             | 7.35 us                                                | 6.82 us: 1.08x faster                                        |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                         |
| thrift                     | 791 us                                                 | 739 us: 1.07x faster                                         |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.07x faster                                         |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.07x faster                                         |
| deltablue                  | 3.45 ms                                                | 3.25 ms: 1.06x faster                                        |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                         |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.06x faster                                         |
| xml_etree_iterparse        | 96.7 ms                                                | 91.6 ms: 1.06x faster                                        |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                       |
| hexiom                     | 6.17 ms                                                | 5.88 ms: 1.05x faster                                        |
| meteor_contest             | 104 ms                                                 | 98.8 ms: 1.05x faster                                        |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                        |
| sqlglot_normalize          | 107 ms                                                 | 102 ms: 1.04x faster                                         |
| sqlglot_optimize           | 53.3 ms                                                | 51.0 ms: 1.04x faster                                        |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                       |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                        |
| nbody                      | 89.3 ms                                                | 86.0 ms: 1.04x faster                                        |
| pprint_safe_repr           | 743 ms                                                 | 716 ms: 1.04x faster                                         |
| unpickle_pure_python       | 221 us                                                 | 214 us: 1.03x faster                                         |
| genshi_xml                 | 50.2 ms                                                | 48.8 ms: 1.03x faster                                        |
| xml_etree_generate         | 85.2 ms                                                | 83.1 ms: 1.03x faster                                        |
| docutils                   | 2.64 sec                                               | 2.59 sec: 1.02x faster                                       |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.01x faster                                         |
| sympy_expand               | 468 ms                                                 | 461 ms: 1.01x faster                                         |
| json                       | 5.02 ms                                                | 4.97 ms: 1.01x faster                                        |
| nqueens                    | 80.1 ms                                                | 79.5 ms: 1.01x faster                                        |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                         |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.00x slower                                         |
| django_template            | 34.7 ms                                                | 35.5 ms: 1.02x slower                                        |
| fannkuch                   | 372 ms                                                 | 384 ms: 1.03x slower                                         |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.54 ms: 1.03x slower                                        |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.04x slower                                        |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                        |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                         |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                        |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.11x slower                                        |
| pidigits                   | 184 ms                                                 | 208 ms: 1.13x slower                                         |
| coverage                   | 71.4 ms                                                | 80.9 ms: 1.13x slower                                        |
| telco                      | 6.53 ms                                                | 7.49 ms: 1.15x slower                                        |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.19x slower                                        |
| python_startup_no_site     | 7.16 ms                                                | 8.60 ms: 1.20x slower                                        |
| gc_traversal               | 3.46 ms                                                | 4.32 ms: 1.25x slower                                        |
| python_startup             | 9.93 ms                                                | 15.0 ms: 1.51x slower                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                        |
| bench_mp_pool              | 10.8 ms                                                | 88.0 ms: 8.15x slower                                        |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                 |

Benchmark hidden because not significant (3): xml_etree_process, mdp, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250314-3.14.0a5+-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.12x