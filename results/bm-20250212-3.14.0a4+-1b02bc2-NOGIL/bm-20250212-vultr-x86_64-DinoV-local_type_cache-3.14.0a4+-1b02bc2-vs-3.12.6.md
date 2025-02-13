# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 1b02bc2
- commit date: 2025-02-12
- overall geometric mean: 1.048x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.15x slower                                              |
| docutils       | 2.64 sec                                               | 2.83 sec: 1.07x slower                                            |
| html5lib       | 63.6 ms                                                | 71.8 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                              |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.71x faster                                              |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 541 ms: 1.32x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                             |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                              |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.4 ms: 1.06x faster                                             |
| pidigits       | 184 ms                                                 | 203 ms: 1.10x slower                                              |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                              |
| Geometric mean | (ref)                                                  | 1.15x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.16x faster                                             |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                              |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.3 ms: 1.10x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                              |
| unpickle_pure_python | 221 us                                                 | 247 us: 1.12x slower                                              |
| tomli_loads          | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| xml_etree_generate   | 85.2 ms                                                | 96.3 ms: 1.13x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 68.1 ms: 1.16x slower                                             |
| json_loads           | 26.5 us                                                | 31.0 us: 1.17x slower                                             |
| pickle_pure_python   | 308 us                                                 | 372 us: 1.21x slower                                              |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                             |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.63 ms: 1.35x slower                                             |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                             |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.9 ms: 1.17x slower                                             |
| django_template | 34.7 ms                                                | 41.7 ms: 1.20x slower                                             |
| genshi_text     | 22.8 ms                                                | 28.0 ms: 1.23x slower                                             |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                             |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.98x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                              |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.71x faster                                              |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 541 ms: 1.32x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.16x faster                                             |
| deepcopy                   | 352 us                                                 | 305 us: 1.15x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 88.3 ms: 1.10x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                              |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 37.6 us: 1.07x faster                                             |
| float                      | 80.8 ms                                                | 76.4 ms: 1.06x faster                                             |
| spectral_norm              | 110 ms                                                 | 106 ms: 1.04x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                             |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                              |
| generators                 | 32.2 ms                                                | 31.7 ms: 1.02x faster                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.69 sec: 1.01x faster                                            |
| comprehensions             | 19.8 us                                                | 19.9 us: 1.00x slower                                             |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.01x slower                                            |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.18 us: 1.03x slower                                             |
| dulwich_log                | 78.9 ms                                                | 82.4 ms: 1.05x slower                                             |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                              |
| docutils                   | 2.64 sec                                               | 2.83 sec: 1.07x slower                                            |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                              |
| json                       | 5.02 ms                                                | 5.41 ms: 1.08x slower                                             |
| logging_simple             | 6.63 us                                                | 7.15 us: 1.08x slower                                             |
| raytrace                   | 299 ms                                                 | 328 ms: 1.09x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                              |
| pprint_safe_repr           | 743 ms                                                 | 815 ms: 1.10x slower                                              |
| pyflate                    | 448 ms                                                 | 493 ms: 1.10x slower                                              |
| pidigits                   | 184 ms                                                 | 203 ms: 1.10x slower                                              |
| chaos                      | 62.8 ms                                                | 69.3 ms: 1.10x slower                                             |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.3 ms: 1.11x slower                                             |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.12x slower                                            |
| unpickle_pure_python       | 221 us                                                 | 247 us: 1.12x slower                                              |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                              |
| tomli_loads                | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                              |
| logging_format             | 7.35 us                                                | 8.28 us: 1.13x slower                                             |
| html5lib                   | 63.6 ms                                                | 71.8 ms: 1.13x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 96.3 ms: 1.13x slower                                             |
| scimark_fft                | 342 ms                                                 | 388 ms: 1.14x slower                                              |
| thrift                     | 791 us                                                 | 901 us: 1.14x slower                                              |
| mdp                        | 2.42 sec                                               | 2.76 sec: 1.14x slower                                            |
| sqlglot_optimize           | 53.3 ms                                                | 60.9 ms: 1.14x slower                                             |
| crypto_pyaes               | 76.6 ms                                                | 87.8 ms: 1.15x slower                                             |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                              |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                             |
| 2to3                       | 264 ms                                                 | 304 ms: 1.15x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 68.1 ms: 1.16x slower                                             |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                             |
| json_loads                 | 26.5 us                                                | 31.0 us: 1.17x slower                                             |
| sympy_expand               | 468 ms                                                 | 546 ms: 1.17x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 58.9 ms: 1.17x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.36 ms: 1.19x slower                                             |
| nqueens                    | 80.1 ms                                                | 96.1 ms: 1.20x slower                                             |
| django_template            | 34.7 ms                                                | 41.7 ms: 1.20x slower                                             |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 197 us: 1.21x slower                                              |
| pickle_pure_python         | 308 us                                                 | 372 us: 1.21x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 83.4 ms: 1.22x slower                                             |
| genshi_text                | 22.8 ms                                                | 28.0 ms: 1.23x slower                                             |
| richards                   | 45.9 ms                                                | 56.5 ms: 1.23x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                             |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                              |
| richards_super             | 51.9 ms                                                | 65.3 ms: 1.26x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.28x slower                                             |
| telco                      | 6.53 ms                                                | 8.45 ms: 1.30x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.76 ms: 1.31x slower                                             |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.32x slower                                              |
| python_startup_no_site     | 7.16 ms                                                | 9.63 ms: 1.35x slower                                             |
| deltablue                  | 3.45 ms                                                | 4.72 ms: 1.37x slower                                             |
| coverage                   | 71.4 ms                                                | 98.0 ms: 1.37x slower                                             |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                             |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                              |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.2 ms: 8.81x slower                                             |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (4): pylint, asyncio_websockets, go, logging_silent
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250212-3.14.0a4+-1b02bc2-NOGIL/bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.048x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x