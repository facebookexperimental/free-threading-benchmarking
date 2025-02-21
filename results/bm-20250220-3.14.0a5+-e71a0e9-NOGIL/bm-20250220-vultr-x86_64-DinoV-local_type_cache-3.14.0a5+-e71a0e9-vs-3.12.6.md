# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: e71a0e9
- commit date: 2025-02-20
- overall geometric mean: 1.048x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 303 ms: 1.15x slower                                              |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                            |
| html5lib       | 63.6 ms                                                | 73.0 ms: 1.15x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 568 ms: 1.96x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.82x faster                                              |
| async_tree_io              | 1.08 sec                                               | 597 ms: 1.81x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                              |
| async_tree_none            | 464 ms                                                 | 282 ms: 1.65x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 496 ms: 1.46x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 530 ms: 1.35x faster                                              |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                             |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.3 ms: 1.06x faster                                             |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                              |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                              |
| Geometric mean | (ref)                                                  | 1.13x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                             |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                              |
| regex_compile  | 142 ms                                                 | 155 ms: 1.09x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                             |
| Geometric mean | (ref)                                                  | 1.05x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.4 ms: 1.09x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                             |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.13x slower                                              |
| pickle_pure_python   | 308 us                                                 | 363 us: 1.18x slower                                              |
| json_loads           | 26.5 us                                                | 31.3 us: 1.18x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 69.8 ms: 1.18x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                             |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.72 ms: 1.36x slower                                             |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                             |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.4 ms: 1.18x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.7 ms: 1.21x slower                                             |
| django_template | 34.7 ms                                                | 44.3 ms: 1.28x slower                                             |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                             |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.98x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 568 ms: 1.96x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.82x faster                                              |
| async_tree_io              | 1.08 sec                                               | 597 ms: 1.81x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                              |
| async_tree_none            | 464 ms                                                 | 282 ms: 1.65x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 496 ms: 1.46x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 530 ms: 1.35x faster                                              |
| deepcopy                   | 352 us                                                 | 307 us: 1.14x faster                                              |
| xml_etree_iterparse        | 96.7 ms                                                | 88.4 ms: 1.09x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                             |
| pathlib                    | 21.5 ms                                                | 20.0 ms: 1.08x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 38.0 us: 1.06x faster                                             |
| float                      | 80.8 ms                                                | 76.3 ms: 1.06x faster                                             |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                             |
| go                         | 139 ms                                                 | 138 ms: 1.01x faster                                              |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                              |
| generators                 | 32.2 ms                                                | 32.0 ms: 1.01x faster                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.71 sec: 1.00x faster                                            |
| comprehensions             | 19.8 us                                                | 19.9 us: 1.00x slower                                             |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                            |
| deepcopy_reduce            | 3.08 us                                                | 3.17 us: 1.03x slower                                             |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                              |
| dulwich_log                | 78.9 ms                                                | 82.7 ms: 1.05x slower                                             |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                              |
| json                       | 5.02 ms                                                | 5.30 ms: 1.06x slower                                             |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                            |
| raytrace                   | 299 ms                                                 | 325 ms: 1.09x slower                                              |
| regex_compile              | 142 ms                                                 | 155 ms: 1.09x slower                                              |
| logging_simple             | 6.63 us                                                | 7.24 us: 1.09x slower                                             |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                              |
| pyflate                    | 448 ms                                                 | 494 ms: 1.10x slower                                              |
| pprint_safe_repr           | 743 ms                                                 | 823 ms: 1.11x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                             |
| chaos                      | 62.8 ms                                                | 69.8 ms: 1.11x slower                                             |
| deltablue                  | 3.45 ms                                                | 3.85 ms: 1.12x slower                                             |
| logging_format             | 7.35 us                                                | 8.22 us: 1.12x slower                                             |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                            |
| tomli_loads                | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                             |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                              |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.13x slower                                              |
| scimark_fft                | 342 ms                                                 | 388 ms: 1.14x slower                                              |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                             |
| thrift                     | 791 us                                                 | 905 us: 1.14x slower                                              |
| html5lib                   | 63.6 ms                                                | 73.0 ms: 1.15x slower                                             |
| crypto_pyaes               | 76.6 ms                                                | 88.0 ms: 1.15x slower                                             |
| mdp                        | 2.42 sec                                               | 2.78 sec: 1.15x slower                                            |
| 2to3                       | 264 ms                                                 | 303 ms: 1.15x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 61.7 ms: 1.16x slower                                             |
| sympy_str                  | 292 ms                                                 | 340 ms: 1.17x slower                                              |
| pickle_pure_python         | 308 us                                                 | 363 us: 1.18x slower                                              |
| json_loads                 | 26.5 us                                                | 31.3 us: 1.18x slower                                             |
| richards                   | 45.9 ms                                                | 54.2 ms: 1.18x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 59.4 ms: 1.18x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 69.8 ms: 1.18x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.3 ms: 1.18x slower                                             |
| sympy_expand               | 468 ms                                                 | 557 ms: 1.19x slower                                              |
| sqlglot_transpile          | 1.67 ms                                                | 1.99 ms: 1.19x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.39 ms: 1.20x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 82.7 ms: 1.21x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                              |
| genshi_text                | 22.8 ms                                                | 27.7 ms: 1.21x slower                                             |
| nqueens                    | 80.1 ms                                                | 97.4 ms: 1.22x slower                                             |
| richards_super             | 51.9 ms                                                | 63.4 ms: 1.22x slower                                             |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                              |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.68 ms: 1.24x slower                                             |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.27x slower                                             |
| django_template            | 34.7 ms                                                | 44.3 ms: 1.28x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.69 ms: 1.30x slower                                             |
| fannkuch                   | 372 ms                                                 | 487 ms: 1.31x slower                                              |
| telco                      | 6.53 ms                                                | 8.78 ms: 1.35x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.72 ms: 1.36x slower                                             |
| coverage                   | 71.4 ms                                                | 98.9 ms: 1.38x slower                                             |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                             |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                              |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.51x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.8 ms: 8.87x slower                                             |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, scimark_sor
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250220-3.14.0a5+-e71a0e9-NOGIL/bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.048x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x