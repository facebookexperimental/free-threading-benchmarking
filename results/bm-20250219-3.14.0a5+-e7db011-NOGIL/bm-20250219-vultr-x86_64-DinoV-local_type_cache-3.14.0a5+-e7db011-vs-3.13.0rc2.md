# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: e7db011
- commit date: 2025-02-19
- overall geometric mean: 1.081x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 303 ms: 1.17x slower                                              |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                            |
| html5lib       | 68.6 ms                                                                | 71.5 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 579 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 609 ms: 1.45x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 354 ms: 1.30x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 508 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.23x faster                                              |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                              |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                             |
| Geometric mean             | (ref)                                                                  | 1.23x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 198 ms: 1.09x faster                                              |
| float          | 76.7 ms                                                                | 77.2 ms: 1.01x slower                                             |
| nbody          | 85.3 ms                                                                | 133 ms: 1.56x slower                                              |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                             |
| regex_dna      | 189 ms                                                                 | 184 ms: 1.02x faster                                              |
| regex_v8       | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                             |
| regex_compile  | 131 ms                                                                 | 155 ms: 1.18x slower                                              |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 95.9 ms: 1.12x slower                                             |
| json_loads           | 27.3 us                                                                | 31.5 us: 1.15x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 69.6 ms: 1.18x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 249 us: 1.20x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 363 us: 1.25x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.69 ms: 1.31x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.1 ms: 1.22x slower                                             |
| django_template | 34.2 ms                                                                | 42.7 ms: 1.25x slower                                             |
| genshi_text     | 21.7 ms                                                                | 28.1 ms: 1.29x slower                                             |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.73 ms: 1.91x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 579 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 609 ms: 1.45x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 354 ms: 1.30x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 508 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.23x faster                                              |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                              |
| deepcopy                   | 357 us                                                                 | 306 us: 1.17x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                             |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.09x faster                                              |
| sqlite_synth               | 2.25 us                                                                | 2.06 us: 1.09x faster                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| scimark_sor                | 134 ms                                                                 | 130 ms: 1.03x faster                                              |
| regex_dna                  | 189 ms                                                                 | 184 ms: 1.02x faster                                              |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                             |
| deepcopy_memo              | 38.1 us                                                                | 37.8 us: 1.01x faster                                             |
| float                      | 76.7 ms                                                                | 77.2 ms: 1.01x slower                                             |
| deepcopy_reduce            | 3.12 us                                                                | 3.15 us: 1.01x slower                                             |
| pathlib                    | 19.3 ms                                                                | 19.9 ms: 1.03x slower                                             |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.03x slower                                             |
| html5lib                   | 68.6 ms                                                                | 71.5 ms: 1.04x slower                                             |
| regex_v8                   | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.67 sec: 1.05x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                            |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                            |
| json                       | 4.98 ms                                                                | 5.37 ms: 1.08x slower                                             |
| pyflate                    | 449 ms                                                                 | 487 ms: 1.08x slower                                              |
| telco                      | 7.77 ms                                                                | 8.53 ms: 1.10x slower                                             |
| logging_silent             | 98.2 ns                                                                | 110 ns: 1.12x slower                                              |
| dulwich_log                | 74.5 ms                                                                | 83.5 ms: 1.12x slower                                             |
| xml_etree_generate         | 85.4 ms                                                                | 95.9 ms: 1.12x slower                                             |
| scimark_fft                | 348 ms                                                                 | 392 ms: 1.13x slower                                              |
| generators                 | 28.5 ms                                                                | 32.3 ms: 1.13x slower                                             |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.13x slower                                              |
| thrift                     | 772 us                                                                 | 879 us: 1.14x slower                                              |
| json_loads                 | 27.3 us                                                                | 31.5 us: 1.15x slower                                             |
| mdp                        | 2.34 sec                                                               | 2.71 sec: 1.16x slower                                            |
| pprint_safe_repr           | 719 ms                                                                 | 833 ms: 1.16x slower                                              |
| tomli_loads                | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                            |
| sqlglot_optimize           | 52.7 ms                                                                | 61.4 ms: 1.17x slower                                             |
| 2to3                       | 259 ms                                                                 | 303 ms: 1.17x slower                                              |
| xml_etree_process          | 59.2 ms                                                                | 69.6 ms: 1.18x slower                                             |
| regex_compile              | 131 ms                                                                 | 155 ms: 1.18x slower                                              |
| pprint_pformat             | 1.46 sec                                                               | 1.72 sec: 1.18x slower                                            |
| logging_simple             | 6.14 us                                                                | 7.28 us: 1.19x slower                                             |
| comprehensions             | 16.6 us                                                                | 19.7 us: 1.19x slower                                             |
| coverage                   | 82.5 ms                                                                | 98.4 ms: 1.19x slower                                             |
| logging_format             | 6.92 us                                                                | 8.27 us: 1.20x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 249 us: 1.20x slower                                              |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                              |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                             |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.77 ms: 1.21x slower                                             |
| sympy_expand               | 454 ms                                                                 | 553 ms: 1.22x slower                                              |
| genshi_xml                 | 49.1 ms                                                                | 60.1 ms: 1.22x slower                                             |
| sympy_integrate            | 19.7 ms                                                                | 24.3 ms: 1.23x slower                                             |
| hexiom                     | 5.95 ms                                                                | 7.35 ms: 1.23x slower                                             |
| sympy_str                  | 274 ms                                                                 | 338 ms: 1.23x slower                                              |
| chaos                      | 56.3 ms                                                                | 69.7 ms: 1.24x slower                                             |
| nqueens                    | 77.7 ms                                                                | 96.4 ms: 1.24x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 140 ms: 1.24x slower                                              |
| richards                   | 44.4 ms                                                                | 55.3 ms: 1.25x slower                                             |
| pickle_pure_python         | 292 us                                                                 | 363 us: 1.25x slower                                              |
| sqlglot_transpile          | 1.55 ms                                                                | 1.94 ms: 1.25x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.87 ms: 1.25x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.3 ms: 1.25x slower                                             |
| django_template            | 34.2 ms                                                                | 42.7 ms: 1.25x slower                                             |
| richards_super             | 50.4 ms                                                                | 64.3 ms: 1.27x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 199 us: 1.28x slower                                              |
| crypto_pyaes               | 68.2 ms                                                                | 87.8 ms: 1.29x slower                                             |
| fannkuch                   | 376 ms                                                                 | 485 ms: 1.29x slower                                              |
| sqlglot_parse              | 1.25 ms                                                                | 1.61 ms: 1.29x slower                                             |
| genshi_text                | 21.7 ms                                                                | 28.1 ms: 1.29x slower                                             |
| meteor_contest             | 101 ms                                                                 | 132 ms: 1.30x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.69 ms: 1.31x slower                                             |
| raytrace                   | 250 ms                                                                 | 330 ms: 1.32x slower                                              |
| python_startup             | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                             |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                             |
| nbody                      | 85.3 ms                                                                | 133 ms: 1.56x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.31 ms: 3.58x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 95.5 ms: 8.69x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (4): go, asyncio_websockets, pylint, spectral_norm
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250219-3.14.0a5+-e7db011-NOGIL/bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x