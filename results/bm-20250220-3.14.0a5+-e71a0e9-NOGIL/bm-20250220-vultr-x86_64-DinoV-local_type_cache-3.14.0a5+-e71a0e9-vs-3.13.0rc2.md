# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: e71a0e9
- commit date: 2025-02-20
- overall geometric mean: 1.080x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 303 ms: 1.17x slower                                              |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                            |
| html5lib       | 68.6 ms                                                                | 73.0 ms: 1.06x slower                                             |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 568 ms: 1.59x faster                                              |
| async_tree_io              | 881 ms                                                                 | 597 ms: 1.48x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.36x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 350 ms: 1.31x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 496 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 530 ms: 1.26x faster                                              |
| async_tree_none            | 353 ms                                                                 | 282 ms: 1.25x faster                                              |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| float          | 76.7 ms                                                                | 76.3 ms: 1.01x faster                                             |
| nbody          | 85.3 ms                                                                | 132 ms: 1.55x slower                                              |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                             |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                             |
| regex_compile  | 131 ms                                                                 | 155 ms: 1.18x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.4 ms: 1.07x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 96.1 ms: 1.12x slower                                             |
| json_loads           | 27.3 us                                                                | 31.3 us: 1.14x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 69.8 ms: 1.18x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 363 us: 1.24x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.72 ms: 1.31x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.4 ms: 1.21x slower                                             |
| genshi_text     | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                             |
| django_template | 34.2 ms                                                                | 44.3 ms: 1.30x slower                                             |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.90x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 568 ms: 1.59x faster                                              |
| async_tree_io              | 881 ms                                                                 | 597 ms: 1.48x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.36x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 350 ms: 1.31x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 496 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 530 ms: 1.26x faster                                              |
| async_tree_none            | 353 ms                                                                 | 282 ms: 1.25x faster                                              |
| deepcopy                   | 357 us                                                                 | 307 us: 1.16x faster                                              |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                             |
| regex_effbot               | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                             |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                              |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.4 ms: 1.07x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| scimark_sor                | 134 ms                                                                 | 130 ms: 1.03x faster                                              |
| go                         | 141 ms                                                                 | 138 ms: 1.02x faster                                              |
| float                      | 76.7 ms                                                                | 76.3 ms: 1.01x faster                                             |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                             |
| regex_v8                   | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                             |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.01x slower                                              |
| deepcopy_reduce            | 3.12 us                                                                | 3.17 us: 1.02x slower                                             |
| pathlib                    | 19.3 ms                                                                | 20.0 ms: 1.04x slower                                             |
| create_gc_cycles           | 1.33 ms                                                                | 1.39 ms: 1.04x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.71 sec: 1.06x slower                                            |
| json                       | 4.98 ms                                                                | 5.30 ms: 1.06x slower                                             |
| html5lib                   | 68.6 ms                                                                | 73.0 ms: 1.06x slower                                             |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                            |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.08x slower                                            |
| pyflate                    | 449 ms                                                                 | 494 ms: 1.10x slower                                              |
| dulwich_log                | 74.5 ms                                                                | 82.7 ms: 1.11x slower                                             |
| scimark_fft                | 348 ms                                                                 | 388 ms: 1.12x slower                                              |
| generators                 | 28.5 ms                                                                | 32.0 ms: 1.12x slower                                             |
| xml_etree_generate         | 85.4 ms                                                                | 96.1 ms: 1.12x slower                                             |
| telco                      | 7.77 ms                                                                | 8.78 ms: 1.13x slower                                             |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.14x slower                                              |
| logging_silent             | 98.2 ns                                                                | 112 ns: 1.14x slower                                              |
| json_loads                 | 27.3 us                                                                | 31.3 us: 1.14x slower                                             |
| pprint_safe_repr           | 719 ms                                                                 | 823 ms: 1.15x slower                                              |
| 2to3                       | 259 ms                                                                 | 303 ms: 1.17x slower                                              |
| pprint_pformat             | 1.46 sec                                                               | 1.70 sec: 1.17x slower                                            |
| sqlglot_optimize           | 52.7 ms                                                                | 61.7 ms: 1.17x slower                                             |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                            |
| thrift                     | 772 us                                                                 | 905 us: 1.17x slower                                              |
| xml_etree_process          | 59.2 ms                                                                | 69.8 ms: 1.18x slower                                             |
| regex_compile              | 131 ms                                                                 | 155 ms: 1.18x slower                                              |
| logging_simple             | 6.14 us                                                                | 7.24 us: 1.18x slower                                             |
| mdp                        | 2.34 sec                                                               | 2.78 sec: 1.19x slower                                            |
| logging_format             | 6.92 us                                                                | 8.22 us: 1.19x slower                                             |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.69 ms: 1.20x slower                                             |
| coverage                   | 82.5 ms                                                                | 98.9 ms: 1.20x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                              |
| comprehensions             | 16.6 us                                                                | 19.9 us: 1.20x slower                                             |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                             |
| genshi_xml                 | 49.1 ms                                                                | 59.4 ms: 1.21x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                              |
| richards                   | 44.4 ms                                                                | 54.2 ms: 1.22x slower                                             |
| sympy_expand               | 454 ms                                                                 | 557 ms: 1.23x slower                                              |
| sympy_integrate            | 19.7 ms                                                                | 24.3 ms: 1.23x slower                                             |
| sympy_str                  | 274 ms                                                                 | 340 ms: 1.24x slower                                              |
| chaos                      | 56.3 ms                                                                | 69.8 ms: 1.24x slower                                             |
| hexiom                     | 5.95 ms                                                                | 7.39 ms: 1.24x slower                                             |
| pickle_pure_python         | 292 us                                                                 | 363 us: 1.24x slower                                              |
| deltablue                  | 3.10 ms                                                                | 3.85 ms: 1.24x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 140 ms: 1.25x slower                                              |
| nqueens                    | 77.7 ms                                                                | 97.4 ms: 1.25x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.7 ms: 1.26x slower                                             |
| richards_super             | 50.4 ms                                                                | 63.4 ms: 1.26x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                              |
| genshi_text                | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                             |
| sqlglot_transpile          | 1.55 ms                                                                | 1.99 ms: 1.28x slower                                             |
| crypto_pyaes               | 68.2 ms                                                                | 88.0 ms: 1.29x slower                                             |
| django_template            | 34.2 ms                                                                | 44.3 ms: 1.30x slower                                             |
| fannkuch                   | 376 ms                                                                 | 487 ms: 1.30x slower                                              |
| meteor_contest             | 101 ms                                                                 | 132 ms: 1.30x slower                                              |
| raytrace                   | 250 ms                                                                 | 325 ms: 1.30x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.72 ms: 1.31x slower                                             |
| sqlglot_parse              | 1.25 ms                                                                | 1.68 ms: 1.34x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                             |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                             |
| nbody                      | 85.3 ms                                                                | 132 ms: 1.55x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.30 ms: 3.57x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 95.8 ms: 8.71x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (3): deepcopy_memo, asyncio_websockets, pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250220-3.14.0a5+-e71a0e9-NOGIL/bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.080x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x