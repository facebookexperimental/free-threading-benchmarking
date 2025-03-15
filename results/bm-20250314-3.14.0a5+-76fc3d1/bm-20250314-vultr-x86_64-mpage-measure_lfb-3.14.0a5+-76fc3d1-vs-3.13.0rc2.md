# Results vs. 3.13.0rc2

- fork: mpage
- ref: measure_lfb
- machine: linux-x86_64
- commit hash: 76fc3d1
- commit date: 2025-03-14
- overall geometric mean: 1.050x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 249 ms: 1.04x faster                                         |
| docutils       | 2.63 sec                                                               | 2.59 sec: 1.02x faster                                       |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 614 ms: 1.47x faster                                         |
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                         |
| async_tree_io              | 881 ms                                                                 | 618 ms: 1.43x faster                                         |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.32x faster                                         |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                         |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                         |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 488 ms: 1.30x faster                                         |
| async_tree_none_tg         | 333 ms                                                                 | 258 ms: 1.29x faster                                         |
| async_generators           | 375 ms                                                                 | 329 ms: 1.14x faster                                         |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                        |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                 |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 69.4 ms: 1.11x faster                                        |
| pidigits       | 216 ms                                                                 | 208 ms: 1.04x faster                                         |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                 |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                        |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.07x faster                                         |
| regex_compile  | 131 ms                                                                 | 125 ms: 1.05x faster                                         |
| regex_v8       | 23.2 ms                                                                | 24.6 ms: 1.06x slower                                        |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.89 sec: 1.07x faster                                       |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                         |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                        |
| xml_etree_generate   | 85.4 ms                                                                | 83.1 ms: 1.03x faster                                        |
| xml_etree_process    | 59.2 ms                                                                | 59.0 ms: 1.00x faster                                        |
| json_loads           | 27.3 us                                                                | 27.7 us: 1.01x slower                                        |
| unpickle_pure_python | 208 us                                                                 | 214 us: 1.03x slower                                         |
| pickle_pure_python   | 292 us                                                                 | 309 us: 1.06x slower                                         |
| json_dumps           | 10.6 ms                                                                | 11.3 ms: 1.07x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.60 ms: 1.16x slower                                        |
| python_startup         | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                        |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                        |
| genshi_xml      | 49.1 ms                                                                | 48.8 ms: 1.01x faster                                        |
| mako            | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                        |
| django_template | 34.2 ms                                                                | 35.5 ms: 1.04x slower                                        |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 614 ms: 1.47x faster                                         |
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                         |
| async_tree_io              | 881 ms                                                                 | 618 ms: 1.43x faster                                         |
| deepcopy                   | 357 us                                                                 | 252 us: 1.42x faster                                         |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.32x faster                                         |
| deepcopy_memo              | 38.1 us                                                                | 28.9 us: 1.32x faster                                        |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                         |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                         |
| go                         | 141 ms                                                                 | 108 ms: 1.30x faster                                         |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 488 ms: 1.30x faster                                         |
| async_tree_none_tg         | 333 ms                                                                 | 258 ms: 1.29x faster                                         |
| scimark_sor                | 134 ms                                                                 | 110 ms: 1.21x faster                                         |
| spectral_norm              | 108 ms                                                                 | 91.1 ms: 1.18x faster                                        |
| deepcopy_reduce            | 3.12 us                                                                | 2.65 us: 1.18x faster                                        |
| async_generators           | 375 ms                                                                 | 329 ms: 1.14x faster                                         |
| pylint                     | 317 ms                                                                 | 280 ms: 1.13x faster                                         |
| regex_effbot               | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                        |
| scimark_fft                | 348 ms                                                                 | 309 ms: 1.13x faster                                         |
| pyflate                    | 449 ms                                                                 | 406 ms: 1.11x faster                                         |
| float                      | 76.7 ms                                                                | 69.4 ms: 1.11x faster                                        |
| dulwich_log                | 74.5 ms                                                                | 67.5 ms: 1.10x faster                                        |
| scimark_monte_carlo        | 65.8 ms                                                                | 61.3 ms: 1.07x faster                                        |
| richards                   | 44.4 ms                                                                | 41.5 ms: 1.07x faster                                        |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.07x faster                                         |
| tomli_loads                | 2.01 sec                                                               | 1.89 sec: 1.07x faster                                       |
| richards_super             | 50.4 ms                                                                | 47.6 ms: 1.06x faster                                        |
| genshi_text                | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                        |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                         |
| regex_compile              | 131 ms                                                                 | 125 ms: 1.05x faster                                         |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.54 ms: 1.05x faster                                        |
| thrift                     | 772 us                                                                 | 739 us: 1.04x faster                                         |
| 2to3                       | 259 ms                                                                 | 249 ms: 1.04x faster                                         |
| pidigits                   | 216 ms                                                                 | 208 ms: 1.04x faster                                         |
| telco                      | 7.77 ms                                                                | 7.49 ms: 1.04x faster                                        |
| bpe_tokeniser              | 4.46 sec                                                               | 4.30 sec: 1.04x faster                                       |
| sqlglot_normalize          | 106 ms                                                                 | 102 ms: 1.03x faster                                         |
| sqlglot_optimize           | 52.7 ms                                                                | 51.0 ms: 1.03x faster                                        |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                        |
| generators                 | 28.5 ms                                                                | 27.7 ms: 1.03x faster                                        |
| xml_etree_generate         | 85.4 ms                                                                | 83.1 ms: 1.03x faster                                        |
| meteor_contest             | 101 ms                                                                 | 98.8 ms: 1.03x faster                                        |
| chaos                      | 56.3 ms                                                                | 55.2 ms: 1.02x faster                                        |
| coverage                   | 82.5 ms                                                                | 80.9 ms: 1.02x faster                                        |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                        |
| docutils                   | 2.63 sec                                                               | 2.59 sec: 1.02x faster                                       |
| sqlglot_parse              | 1.25 ms                                                                | 1.23 ms: 1.02x faster                                        |
| sqlite_synth               | 2.25 us                                                                | 2.22 us: 1.01x faster                                        |
| sqlglot_transpile          | 1.55 ms                                                                | 1.53 ms: 1.01x faster                                        |
| logging_format             | 6.92 us                                                                | 6.82 us: 1.01x faster                                        |
| hexiom                     | 5.95 ms                                                                | 5.88 ms: 1.01x faster                                        |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                       |
| genshi_xml                 | 49.1 ms                                                                | 48.8 ms: 1.01x faster                                        |
| xml_etree_process          | 59.2 ms                                                                | 59.0 ms: 1.00x faster                                        |
| comprehensions             | 16.6 us                                                                | 16.5 us: 1.00x faster                                        |
| crypto_pyaes               | 68.2 ms                                                                | 68.4 ms: 1.00x slower                                        |
| raytrace                   | 250 ms                                                                 | 251 ms: 1.00x slower                                         |
| sympy_sum                  | 154 ms                                                                 | 156 ms: 1.01x slower                                         |
| json_loads                 | 27.3 us                                                                | 27.7 us: 1.01x slower                                        |
| sympy_expand               | 454 ms                                                                 | 461 ms: 1.02x slower                                         |
| fannkuch                   | 376 ms                                                                 | 384 ms: 1.02x slower                                         |
| nqueens                    | 77.7 ms                                                                | 79.5 ms: 1.02x slower                                        |
| unpickle_pure_python       | 208 us                                                                 | 214 us: 1.03x slower                                         |
| mako                       | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                        |
| mdp                        | 2.34 sec                                                               | 2.42 sec: 1.04x slower                                       |
| django_template            | 34.2 ms                                                                | 35.5 ms: 1.04x slower                                        |
| deltablue                  | 3.10 ms                                                                | 3.25 ms: 1.05x slower                                        |
| regex_v8                   | 23.2 ms                                                                | 24.6 ms: 1.06x slower                                        |
| pickle_pure_python         | 292 us                                                                 | 309 us: 1.06x slower                                         |
| json_dumps                 | 10.6 ms                                                                | 11.3 ms: 1.07x slower                                        |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.13x slower                                        |
| python_startup_no_site     | 7.41 ms                                                                | 8.60 ms: 1.16x slower                                        |
| gc_traversal               | 3.32 ms                                                                | 4.32 ms: 1.30x slower                                        |
| python_startup             | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                        |
| create_gc_cycles           | 1.33 ms                                                                | 1.84 ms: 1.38x slower                                        |
| bench_mp_pool              | 11.0 ms                                                                | 88.0 ms: 8.00x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                 |

Benchmark hidden because not significant (12): logging_silent, typing_runtime_protocols, pprint_safe_repr, logging_simple, json, sympy_str, scimark_lu, asyncio_websockets, pprint_pformat, sympy_integrate, pathlib, nbody
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250314-3.14.0a5+-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-76fc3d1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x