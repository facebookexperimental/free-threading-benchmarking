# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 68b535b
- commit date: 2025-02-13
- overall geometric mean: 1.059x slower
- HPT reliability: 99.92%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 297 ms: 1.15x slower                                              |
| docutils       | 2.63 sec                                                               | 2.74 sec: 1.04x slower                                            |
| html5lib       | 68.6 ms                                                                | 70.3 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 566 ms: 1.59x faster                                              |
| async_tree_io              | 881 ms                                                                 | 598 ms: 1.47x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 346 ms: 1.33x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 254 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 494 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 526 ms: 1.27x faster                                              |
| async_tree_none            | 353 ms                                                                 | 283 ms: 1.25x faster                                              |
| coroutines                 | 23.3 ms                                                                | 22.1 ms: 1.05x faster                                             |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 193 ms: 1.12x faster                                              |
| float          | 76.7 ms                                                                | 74.1 ms: 1.04x faster                                             |
| nbody          | 85.3 ms                                                                | 125 ms: 1.46x slower                                              |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                             |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.8 ms: 1.03x slower                                             |
| regex_compile  | 131 ms                                                                 | 145 ms: 1.10x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.3 ms: 1.07x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                              |
| tomli_loads          | 2.01 sec                                                               | 2.23 sec: 1.11x slower                                            |
| xml_etree_generate   | 85.4 ms                                                                | 94.9 ms: 1.11x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 237 us: 1.14x slower                                              |
| json_loads           | 27.3 us                                                                | 31.4 us: 1.15x slower                                             |
| xml_etree_process    | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 347 us: 1.19x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.72 ms: 1.31x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 56.7 ms: 1.16x slower                                             |
| django_template | 34.2 ms                                                                | 41.3 ms: 1.21x slower                                             |
| genshi_text     | 21.7 ms                                                                | 27.0 ms: 1.24x slower                                             |
| mako            | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.90x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 566 ms: 1.59x faster                                              |
| async_tree_io              | 881 ms                                                                 | 598 ms: 1.47x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 346 ms: 1.33x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 254 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 494 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 526 ms: 1.27x faster                                              |
| async_tree_none            | 353 ms                                                                 | 283 ms: 1.25x faster                                              |
| deepcopy                   | 357 us                                                                 | 302 us: 1.18x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                             |
| pidigits                   | 216 ms                                                                 | 193 ms: 1.12x faster                                              |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.3 ms: 1.07x faster                                             |
| scimark_sor                | 134 ms                                                                 | 127 ms: 1.05x faster                                              |
| coroutines                 | 23.3 ms                                                                | 22.1 ms: 1.05x faster                                             |
| go                         | 141 ms                                                                 | 134 ms: 1.05x faster                                              |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                              |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                              |
| float                      | 76.7 ms                                                                | 74.1 ms: 1.04x faster                                             |
| deepcopy_memo              | 38.1 us                                                                | 37.4 us: 1.02x faster                                             |
| spectral_norm              | 108 ms                                                                 | 106 ms: 1.02x faster                                              |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                              |
| deepcopy_reduce            | 3.12 us                                                                | 3.08 us: 1.01x faster                                             |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                             |
| html5lib                   | 68.6 ms                                                                | 70.3 ms: 1.03x slower                                             |
| regex_v8                   | 23.2 ms                                                                | 23.8 ms: 1.03x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.60 sec: 1.03x slower                                            |
| pycparser                  | 1.12 sec                                                               | 1.16 sec: 1.03x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.74 sec: 1.04x slower                                            |
| generators                 | 28.5 ms                                                                | 29.9 ms: 1.05x slower                                             |
| create_gc_cycles           | 1.33 ms                                                                | 1.40 ms: 1.05x slower                                             |
| pyflate                    | 449 ms                                                                 | 474 ms: 1.05x slower                                              |
| scimark_fft                | 348 ms                                                                 | 376 ms: 1.08x slower                                              |
| json                       | 4.98 ms                                                                | 5.39 ms: 1.08x slower                                             |
| dulwich_log                | 74.5 ms                                                                | 80.7 ms: 1.08x slower                                             |
| regex_compile              | 131 ms                                                                 | 145 ms: 1.10x slower                                              |
| sqlglot_normalize          | 106 ms                                                                 | 117 ms: 1.11x slower                                              |
| tomli_loads                | 2.01 sec                                                               | 2.23 sec: 1.11x slower                                            |
| pprint_safe_repr           | 719 ms                                                                 | 798 ms: 1.11x slower                                              |
| xml_etree_generate         | 85.4 ms                                                                | 94.9 ms: 1.11x slower                                             |
| mdp                        | 2.34 sec                                                               | 2.62 sec: 1.12x slower                                            |
| logging_silent             | 98.2 ns                                                                | 111 ns: 1.13x slower                                              |
| telco                      | 7.77 ms                                                                | 8.81 ms: 1.13x slower                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.65 sec: 1.13x slower                                            |
| unpickle_pure_python       | 208 us                                                                 | 237 us: 1.14x slower                                              |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.41 ms: 1.14x slower                                             |
| sqlglot_optimize           | 52.7 ms                                                                | 60.1 ms: 1.14x slower                                             |
| thrift                     | 772 us                                                                 | 881 us: 1.14x slower                                              |
| logging_simple             | 6.14 us                                                                | 7.02 us: 1.14x slower                                             |
| logging_format             | 6.92 us                                                                | 7.92 us: 1.14x slower                                             |
| 2to3                       | 259 ms                                                                 | 297 ms: 1.15x slower                                              |
| json_loads                 | 27.3 us                                                                | 31.4 us: 1.15x slower                                             |
| genshi_xml                 | 49.1 ms                                                                | 56.7 ms: 1.16x slower                                             |
| xml_etree_process          | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                             |
| coverage                   | 82.5 ms                                                                | 96.7 ms: 1.17x slower                                             |
| comprehensions             | 16.6 us                                                                | 19.5 us: 1.18x slower                                             |
| chaos                      | 56.3 ms                                                                | 66.3 ms: 1.18x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 133 ms: 1.18x slower                                              |
| hexiom                     | 5.95 ms                                                                | 7.08 ms: 1.19x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 183 ms: 1.19x slower                                              |
| sympy_expand               | 454 ms                                                                 | 540 ms: 1.19x slower                                              |
| pickle_pure_python         | 292 us                                                                 | 347 us: 1.19x slower                                              |
| nqueens                    | 77.7 ms                                                                | 92.9 ms: 1.19x slower                                             |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                             |
| sympy_str                  | 274 ms                                                                 | 331 ms: 1.21x slower                                              |
| django_template            | 34.2 ms                                                                | 41.3 ms: 1.21x slower                                             |
| sqlglot_transpile          | 1.55 ms                                                                | 1.89 ms: 1.21x slower                                             |
| sympy_integrate            | 19.7 ms                                                                | 23.9 ms: 1.21x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.79 ms: 1.22x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 80.8 ms: 1.23x slower                                             |
| genshi_text                | 21.7 ms                                                                | 27.0 ms: 1.24x slower                                             |
| richards                   | 44.4 ms                                                                | 55.1 ms: 1.24x slower                                             |
| sqlglot_parse              | 1.25 ms                                                                | 1.58 ms: 1.27x slower                                             |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.27x slower                                              |
| raytrace                   | 250 ms                                                                 | 316 ms: 1.27x slower                                              |
| fannkuch                   | 376 ms                                                                 | 477 ms: 1.27x slower                                              |
| richards_super             | 50.4 ms                                                                | 64.0 ms: 1.27x slower                                             |
| crypto_pyaes               | 68.2 ms                                                                | 86.7 ms: 1.27x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 199 us: 1.28x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.72 ms: 1.31x slower                                             |
| mako                       | 11.2 ms                                                                | 15.5 ms: 1.38x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                             |
| nbody                      | 85.3 ms                                                                | 125 ms: 1.46x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.30 ms: 3.56x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 95.0 ms: 8.63x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                      |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250213-3.14.0a5+-68b535b-NOGIL/bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.059x slower

# HPT report

- Reliability score: 99.92% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x