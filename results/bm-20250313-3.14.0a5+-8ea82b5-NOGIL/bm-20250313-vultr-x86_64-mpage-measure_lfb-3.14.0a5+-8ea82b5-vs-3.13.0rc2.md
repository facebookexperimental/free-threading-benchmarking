# Results vs. 3.13.0rc2

- fork: mpage
- ref: measure_lfb
- machine: linux-x86_64
- commit hash: 8ea82b5
- commit date: 2025-03-13
- overall geometric mean: 1.057x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 290 ms: 1.12x slower                                         |
| docutils       | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                       |
| html5lib       | 68.6 ms                                                                | 70.4 ms: 1.03x slower                                        |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 538 ms: 1.68x faster                                         |
| async_tree_io              | 881 ms                                                                 | 573 ms: 1.54x faster                                         |
| async_tree_none_tg         | 333 ms                                                                 | 230 ms: 1.45x faster                                         |
| async_tree_memoization     | 459 ms                                                                 | 330 ms: 1.39x faster                                         |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.38x faster                                         |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.31x faster                                         |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 563 ms: 1.13x faster                                         |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 595 ms: 1.12x faster                                         |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                         |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                         |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 71.2 ms: 1.08x faster                                        |
| pidigits       | 216 ms                                                                 | 226 ms: 1.04x slower                                         |
| nbody          | 85.3 ms                                                                | 118 ms: 1.39x slower                                         |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.79 ms: 1.15x faster                                        |
| regex_dna      | 189 ms                                                                 | 183 ms: 1.03x faster                                         |
| regex_v8       | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                        |
| regex_compile  | 131 ms                                                                 | 153 ms: 1.16x slower                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                        |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                         |
| json_loads           | 27.3 us                                                                | 29.1 us: 1.06x slower                                        |
| tomli_loads          | 2.01 sec                                                               | 2.24 sec: 1.12x slower                                       |
| xml_etree_generate   | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                        |
| unpickle_pure_python | 208 us                                                                 | 238 us: 1.14x slower                                         |
| xml_etree_process    | 59.2 ms                                                                | 68.7 ms: 1.16x slower                                        |
| pickle_pure_python   | 292 us                                                                 | 340 us: 1.17x slower                                         |
| json_dumps           | 10.6 ms                                                                | 12.5 ms: 1.18x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                        |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                        |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 58.6 ms: 1.19x slower                                        |
| django_template | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                        |
| genshi_text     | 21.7 ms                                                                | 26.8 ms: 1.23x slower                                        |
| mako            | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                        |
| Geometric mean  | (ref)                                                                  | 1.26x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.74 ms: 1.91x faster                                        |
| async_tree_io_tg           | 901 ms                                                                 | 538 ms: 1.68x faster                                         |
| async_tree_io              | 881 ms                                                                 | 573 ms: 1.54x faster                                         |
| async_tree_none_tg         | 333 ms                                                                 | 230 ms: 1.45x faster                                         |
| async_tree_memoization     | 459 ms                                                                 | 330 ms: 1.39x faster                                         |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.38x faster                                         |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.31x faster                                         |
| deepcopy                   | 357 us                                                                 | 300 us: 1.19x faster                                         |
| regex_effbot               | 3.21 ms                                                                | 2.79 ms: 1.15x faster                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 563 ms: 1.13x faster                                         |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 595 ms: 1.12x faster                                         |
| sqlite_synth               | 2.25 us                                                                | 2.06 us: 1.09x faster                                        |
| go                         | 141 ms                                                                 | 130 ms: 1.08x faster                                         |
| float                      | 76.7 ms                                                                | 71.2 ms: 1.08x faster                                        |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                        |
| deepcopy_memo              | 38.1 us                                                                | 35.7 us: 1.07x faster                                        |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                         |
| scimark_sor                | 134 ms                                                                 | 128 ms: 1.05x faster                                         |
| regex_dna                  | 189 ms                                                                 | 183 ms: 1.03x faster                                         |
| deepcopy_reduce            | 3.12 us                                                                | 3.07 us: 1.02x faster                                        |
| dulwich_log                | 74.5 ms                                                                | 73.6 ms: 1.01x faster                                        |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                         |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                         |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                        |
| json                       | 4.98 ms                                                                | 5.05 ms: 1.01x slower                                        |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                         |
| scimark_fft                | 348 ms                                                                 | 357 ms: 1.02x slower                                         |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                        |
| html5lib                   | 68.6 ms                                                                | 70.4 ms: 1.03x slower                                        |
| regex_v8                   | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                        |
| pidigits                   | 216 ms                                                                 | 226 ms: 1.04x slower                                         |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                       |
| bpe_tokeniser              | 4.46 sec                                                               | 4.70 sec: 1.06x slower                                       |
| docutils                   | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                       |
| logging_silent             | 98.2 ns                                                                | 104 ns: 1.06x slower                                         |
| pyflate                    | 449 ms                                                                 | 477 ms: 1.06x slower                                         |
| json_loads                 | 27.3 us                                                                | 29.1 us: 1.06x slower                                        |
| mdp                        | 2.34 sec                                                               | 2.58 sec: 1.10x slower                                       |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.25 ms: 1.10x slower                                        |
| telco                      | 7.77 ms                                                                | 8.59 ms: 1.11x slower                                        |
| tomli_loads                | 2.01 sec                                                               | 2.24 sec: 1.12x slower                                       |
| 2to3                       | 259 ms                                                                 | 290 ms: 1.12x slower                                         |
| sqlglot_normalize          | 106 ms                                                                 | 118 ms: 1.12x slower                                         |
| xml_etree_generate         | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                        |
| thrift                     | 772 us                                                                 | 869 us: 1.13x slower                                         |
| generators                 | 28.5 ms                                                                | 32.1 ms: 1.13x slower                                        |
| pprint_safe_repr           | 719 ms                                                                 | 811 ms: 1.13x slower                                         |
| sqlglot_optimize           | 52.7 ms                                                                | 60.0 ms: 1.14x slower                                        |
| pprint_pformat             | 1.46 sec                                                               | 1.66 sec: 1.14x slower                                       |
| unpickle_pure_python       | 208 us                                                                 | 238 us: 1.14x slower                                         |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.0 ms: 1.15x slower                                        |
| xml_etree_process          | 59.2 ms                                                                | 68.7 ms: 1.16x slower                                        |
| regex_compile              | 131 ms                                                                 | 153 ms: 1.16x slower                                         |
| coverage                   | 82.5 ms                                                                | 96.2 ms: 1.17x slower                                        |
| pickle_pure_python         | 292 us                                                                 | 340 us: 1.17x slower                                         |
| deltablue                  | 3.10 ms                                                                | 3.64 ms: 1.18x slower                                        |
| logging_simple             | 6.14 us                                                                | 7.23 us: 1.18x slower                                        |
| chaos                      | 56.3 ms                                                                | 66.3 ms: 1.18x slower                                        |
| sqlglot_transpile          | 1.55 ms                                                                | 1.83 ms: 1.18x slower                                        |
| json_dumps                 | 10.6 ms                                                                | 12.5 ms: 1.18x slower                                        |
| logging_format             | 6.92 us                                                                | 8.26 us: 1.19x slower                                        |
| genshi_xml                 | 49.1 ms                                                                | 58.6 ms: 1.19x slower                                        |
| richards                   | 44.4 ms                                                                | 53.3 ms: 1.20x slower                                        |
| sympy_expand               | 454 ms                                                                 | 546 ms: 1.20x slower                                         |
| scimark_lu                 | 112 ms                                                                 | 135 ms: 1.20x slower                                         |
| raytrace                   | 250 ms                                                                 | 302 ms: 1.21x slower                                         |
| sympy_integrate            | 19.7 ms                                                                | 23.9 ms: 1.21x slower                                        |
| sqlglot_parse              | 1.25 ms                                                                | 1.51 ms: 1.21x slower                                        |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                         |
| sympy_str                  | 274 ms                                                                 | 333 ms: 1.22x slower                                         |
| nqueens                    | 77.7 ms                                                                | 94.6 ms: 1.22x slower                                        |
| richards_super             | 50.4 ms                                                                | 61.4 ms: 1.22x slower                                        |
| hexiom                     | 5.95 ms                                                                | 7.27 ms: 1.22x slower                                        |
| comprehensions             | 16.6 us                                                                | 20.3 us: 1.22x slower                                        |
| django_template            | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                        |
| fannkuch                   | 376 ms                                                                 | 460 ms: 1.22x slower                                         |
| genshi_text                | 21.7 ms                                                                | 26.8 ms: 1.23x slower                                        |
| typing_runtime_protocols   | 156 us                                                                 | 193 us: 1.24x slower                                         |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.25x slower                                         |
| crypto_pyaes               | 68.2 ms                                                                | 85.3 ms: 1.25x slower                                        |
| mako                       | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                        |
| nbody                      | 85.3 ms                                                                | 118 ms: 1.39x slower                                         |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                        |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                        |
| bench_thread_pool          | 924 us                                                                 | 3.13 ms: 3.39x slower                                        |
| bench_mp_pool              | 11.0 ms                                                                | 96.2 ms: 8.75x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                 |

Benchmark hidden because not significant (2): pylint, create_gc_cycles
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250313-3.14.0a5+-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.057x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x