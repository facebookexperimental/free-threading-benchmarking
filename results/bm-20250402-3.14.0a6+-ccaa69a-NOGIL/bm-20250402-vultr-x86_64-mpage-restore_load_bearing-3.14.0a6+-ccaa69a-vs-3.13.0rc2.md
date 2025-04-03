# Results vs. 3.13.0rc2

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.035x slower
- HPT reliability: 97.72%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 289 ms: 1.11x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| html5lib       | 68.6 ms                                                                | 70.6 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 535 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 564 ms: 1.56x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 232 ms: 1.44x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 322 ms: 1.42x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 292 ms: 1.41x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 482 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 511 ms: 1.30x faster                                                  |
| async_generators           | 375 ms                                                                 | 365 ms: 1.03x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.30x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| float          | 76.7 ms                                                                | 70.0 ms: 1.10x faster                                                 |
| nbody          | 85.3 ms                                                                | 113 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.04x faster                                                  |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.3 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.23 sec: 1.11x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                 |
| json_loads           | 27.3 us                                                                | 30.7 us: 1.12x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 69.3 ms: 1.17x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 343 us: 1.17x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.6 ms: 1.17x slower                                                 |
| django_template | 34.2 ms                                                                | 40.8 ms: 1.19x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                                 |
| mako            | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.86x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.35 sec: 1.74x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 535 ms: 1.68x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 564 ms: 1.56x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 232 ms: 1.44x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 322 ms: 1.42x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 292 ms: 1.41x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 482 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 511 ms: 1.30x faster                                                  |
| deepcopy                   | 357 us                                                                 | 298 us: 1.20x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                                 |
| pidigits                   | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                 |
| float                      | 76.7 ms                                                                | 70.0 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.3 ms: 1.08x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 126 ms: 1.06x faster                                                  |
| go                         | 141 ms                                                                 | 133 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 36.6 us: 1.04x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.04 us: 1.03x faster                                                 |
| async_generators           | 375 ms                                                                 | 365 ms: 1.03x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 106 ms: 1.02x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 73.5 ms: 1.01x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 347 ms: 1.00x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.58 sec: 1.03x slower                                                |
| html5lib                   | 68.6 ms                                                                | 70.6 ms: 1.03x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                                |
| pyflate                    | 449 ms                                                                 | 471 ms: 1.05x slower                                                  |
| json                       | 4.98 ms                                                                | 5.25 ms: 1.05x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.01 ms: 1.06x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.58 ms: 1.10x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.23 sec: 1.11x slower                                                |
| 2to3                       | 259 ms                                                                 | 289 ms: 1.11x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 802 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.7 us: 1.12x slower                                                 |
| generators                 | 28.5 ms                                                                | 32.1 ms: 1.12x slower                                                 |
| chaos                      | 56.3 ms                                                                | 63.9 ms: 1.13x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 112 ns: 1.14x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 75.6 ms: 1.15x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.68 sec: 1.15x slower                                                |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 90.4 ms: 1.16x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.18 us: 1.17x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 69.3 ms: 1.17x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.1 ms: 1.17x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 132 ms: 1.17x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 57.6 ms: 1.17x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 343 us: 1.17x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.16 us: 1.18x slower                                                 |
| django_template            | 34.2 ms                                                                | 40.8 ms: 1.19x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.11 ms: 1.19x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 544 ms: 1.20x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.72 ms: 1.20x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.21x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 331 ms: 1.21x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                 |
| raytrace                   | 250 ms                                                                 | 302 ms: 1.21x slower                                                  |
| richards                   | 44.4 ms                                                                | 53.7 ms: 1.21x slower                                                 |
| comprehensions             | 16.6 us                                                                | 20.2 us: 1.22x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                                 |
| richards_super             | 50.4 ms                                                                | 61.5 ms: 1.22x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 461 ms: 1.23x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 85.8 ms: 1.26x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 197 us: 1.26x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                  |
| nbody                      | 85.3 ms                                                                | 113 ms: 1.33x slower                                                  |
| coverage                   | 82.5 ms                                                                | 113 ms: 1.37x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.15 ms: 3.41x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 96.2 ms: 8.74x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (3): pylint, pathlib, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250402-3.14.0a6+-ccaa69a-NOGIL/bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.035x slower

# HPT report

- Reliability score: 97.72% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x