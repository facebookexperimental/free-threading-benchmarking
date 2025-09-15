# Results vs. 3.12.6

- fork: python
- ref: 3e06cfcaeee31c2a6e9b
- machine: linux-x86_64
- commit hash: 3e06cfc
- commit date: 2025-09-14
- overall geometric mean: 1.077x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                  |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                |
| html5lib       | 63.6 ms                                                | 61.3 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 621 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                  |
| async_generators           | 384 ms                                                 | 347 ms: 1.11x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.5 ms: 1.13x faster                                                 |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.56 ms: 1.24x faster                                                 |
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_dna      | 168 ms                                                 | 166 ms: 1.01x faster                                                  |
| regex_v8       | 20.6 ms                                                | 20.7 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                |
| json_dumps           | 10.4 ms                                                | 9.57 ms: 1.08x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.8 ms: 1.04x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 301 us: 1.02x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.7 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                 |
| json_loads           | 26.5 us                                                | 28.0 us: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                 |
| django_template | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                 |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                                |
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 621 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.1 us: 1.54x faster                                                 |
| deepcopy                   | 352 us                                                 | 240 us: 1.47x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                  |
| go                         | 139 ms                                                 | 105 ms: 1.33x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.5 us: 1.28x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.56 ms: 1.24x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.20x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                 |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.5 ms: 1.19x faster                                                 |
| raytrace                   | 299 ms                                                 | 255 ms: 1.18x faster                                                  |
| spectral_norm              | 110 ms                                                 | 94.5 ms: 1.17x faster                                                 |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.17x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| logging_silent             | 109 ns                                                 | 96.1 ns: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                |
| float                      | 80.8 ms                                                | 71.5 ms: 1.13x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.88 us: 1.13x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 68.1 ms: 1.13x faster                                                 |
| logging_format             | 7.35 us                                                | 6.54 us: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 41.1 ms: 1.12x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.54 ms: 1.11x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                |
| pyflate                    | 448 ms                                                 | 404 ms: 1.11x faster                                                  |
| async_generators           | 384 ms                                                 | 347 ms: 1.11x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.9 ms: 1.11x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.2 ms: 1.10x faster                                                 |
| sympy_str                  | 292 ms                                                 | 265 ms: 1.10x faster                                                  |
| chaos                      | 62.8 ms                                                | 57.4 ms: 1.10x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 149 us: 1.09x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.09x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 684 ms: 1.09x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.57 ms: 1.08x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.24 ms: 1.06x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.5 ms: 1.05x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 756 us: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 92.8 ms: 1.04x faster                                                 |
| sympy_expand               | 468 ms                                                 | 450 ms: 1.04x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.3 ms: 1.04x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 77.7 ms: 1.03x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 301 us: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.7 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                 |
| django_template            | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                 |
| scimark_fft                | 342 ms                                                 | 339 ms: 1.01x faster                                                  |
| regex_dna                  | 168 ms                                                 | 166 ms: 1.01x faster                                                  |
| regex_v8                   | 20.6 ms                                                | 20.7 ms: 1.01x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                 |
| fannkuch                   | 372 ms                                                 | 384 ms: 1.03x slower                                                  |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.31 us: 1.05x slower                                                 |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.06x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.00 ms: 1.07x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.70 ms: 1.07x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 12.3 ms: 1.14x slower                                                 |
| coverage                   | 71.4 ms                                                | 82.8 ms: 1.16x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.68 ms: 1.35x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                 |
| telco                      | 6.53 ms                                                | 157 ms: 24.10x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (2): nbody, json
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x