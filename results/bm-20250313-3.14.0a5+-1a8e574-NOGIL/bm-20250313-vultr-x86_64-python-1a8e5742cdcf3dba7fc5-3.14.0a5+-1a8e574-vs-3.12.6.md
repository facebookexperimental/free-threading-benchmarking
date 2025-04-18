# Results vs. 3.12.6

- fork: python
- ref: 1a8e5742cdcf3dba7fc5
- machine: linux-x86_64
- commit hash: 1a8e574
- commit date: 2025-03-13
- overall geometric mean: 1.050x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 299 ms: 1.13x slower                                                   |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| html5lib       | 63.6 ms                                                | 72.0 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 546 ms: 2.03x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 236 ms: 1.89x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                   |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 530 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 561 ms: 1.28x faster                                                   |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.9 ms: 1.04x faster                                                  |
| pidigits       | 184 ms                                                 | 202 ms: 1.10x slower                                                   |
| nbody          | 89.3 ms                                                | 134 ms: 1.50x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                  |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| regex_compile  | 142 ms                                                 | 158 ms: 1.11x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| json_loads           | 26.5 us                                                | 29.2 us: 1.10x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.38 sec: 1.13x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 257 us: 1.16x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 360 us: 1.17x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 70.4 ms: 1.19x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.6 ms: 1.19x slower                                                  |
| genshi_text     | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                  |
| django_template | 34.7 ms                                                | 43.1 ms: 1.24x slower                                                  |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 546 ms: 2.03x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.74 ms: 1.99x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 236 ms: 1.89x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                   |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 530 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 561 ms: 1.28x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                  |
| deepcopy                   | 352 us                                                 | 312 us: 1.13x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 73.0 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 38.8 us: 1.04x faster                                                  |
| float                      | 80.8 ms                                                | 77.9 ms: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| generators                 | 32.2 ms                                                | 31.6 ms: 1.02x faster                                                  |
| json                       | 5.02 ms                                                | 5.10 ms: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                 |
| logging_silent             | 109 ns                                                 | 111 ns: 1.02x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.84 sec: 1.02x slower                                                 |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.04x slower                                                   |
| go                         | 139 ms                                                 | 145 ms: 1.04x slower                                                   |
| scimark_sor                | 130 ms                                                 | 136 ms: 1.05x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.26 us: 1.06x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| comprehensions             | 19.8 us                                                | 21.1 us: 1.07x slower                                                  |
| raytrace                   | 299 ms                                                 | 323 ms: 1.08x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.21 us: 1.09x slower                                                  |
| pidigits                   | 184 ms                                                 | 202 ms: 1.10x slower                                                   |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| json_loads                 | 26.5 us                                                | 29.2 us: 1.10x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                   |
| regex_compile              | 142 ms                                                 | 158 ms: 1.11x slower                                                   |
| chaos                      | 62.8 ms                                                | 70.1 ms: 1.12x slower                                                  |
| thrift                     | 791 us                                                 | 889 us: 1.12x slower                                                   |
| logging_format             | 7.35 us                                                | 8.26 us: 1.12x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.38 sec: 1.13x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.90 ms: 1.13x slower                                                  |
| html5lib                   | 63.6 ms                                                | 72.0 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                  |
| 2to3                       | 264 ms                                                 | 299 ms: 1.13x slower                                                   |
| pyflate                    | 448 ms                                                 | 509 ms: 1.14x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.14x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 848 ms: 1.14x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.74 sec: 1.14x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 87.8 ms: 1.15x slower                                                  |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.79 sec: 1.15x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 61.4 ms: 1.15x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.93 ms: 1.16x slower                                                  |
| scimark_fft                | 342 ms                                                 | 395 ms: 1.16x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 257 us: 1.16x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 360 us: 1.17x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                  |
| sympy_expand               | 468 ms                                                 | 551 ms: 1.18x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 59.6 ms: 1.19x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.61 ms: 1.19x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 70.4 ms: 1.19x slower                                                  |
| richards                   | 45.9 ms                                                | 55.1 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 197 us: 1.21x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 139 ms: 1.22x slower                                                   |
| nqueens                    | 80.1 ms                                                | 97.8 ms: 1.22x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 84.1 ms: 1.23x slower                                                  |
| richards_super             | 51.9 ms                                                | 63.7 ms: 1.23x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.65 ms: 1.24x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| django_template            | 34.7 ms                                                | 43.1 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.68 ms: 1.29x slower                                                  |
| fannkuch                   | 372 ms                                                 | 499 ms: 1.34x slower                                                   |
| telco                      | 6.53 ms                                                | 9.05 ms: 1.39x slower                                                  |
| coverage                   | 71.4 ms                                                | 99.6 ms: 1.39x slower                                                  |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| nbody                      | 89.3 ms                                                | 134 ms: 1.50x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.35x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.9 ms: 8.88x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, coroutines
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250313-3.14.0a5+-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.050x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.36x