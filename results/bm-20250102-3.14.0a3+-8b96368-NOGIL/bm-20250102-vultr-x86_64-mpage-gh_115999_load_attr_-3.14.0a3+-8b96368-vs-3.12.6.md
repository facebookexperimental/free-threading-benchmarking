# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 8b96368
- commit date: 2025-01-02
- overall geometric mean: 1.060x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 312 ms: 1.18x slower                                                  |
| docutils       | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                |
| html5lib       | 63.6 ms                                                | 73.6 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 343 ms: 1.62x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 471 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                  |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                 |
| async_generators           | 384 ms                                                 | 416 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.7 ms: 1.04x faster                                                 |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                  |
| nbody          | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                  |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| json_loads           | 26.5 us                                                | 27.7 us: 1.04x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 248 us: 1.12x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.5 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.9 ms: 1.17x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.51 sec: 1.19x slower                                                |
| pickle_pure_python   | 308 us                                                 | 375 us: 1.22x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.25x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.71 ms: 1.36x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.56x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.5 ms: 1.19x slower                                                 |
| genshi_text     | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                 |
| django_template | 34.7 ms                                                | 42.8 ms: 1.24x slower                                                 |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 343 ms: 1.62x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 471 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                  |
| deepcopy                   | 352 us                                                 | 311 us: 1.13x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                                 |
| generators                 | 32.2 ms                                                | 30.6 ms: 1.05x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.30 ms: 1.05x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 38.7 us: 1.04x faster                                                 |
| float                      | 80.8 ms                                                | 77.7 ms: 1.04x faster                                                 |
| json                       | 5.02 ms                                                | 4.85 ms: 1.04x faster                                                 |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.79 sec: 1.01x slower                                                |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                                |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                  |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.04x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 82.6 ms: 1.05x slower                                                 |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                 |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                  |
| logging_silent             | 109 ns                                                 | 115 ns: 1.05x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.25 us: 1.06x slower                                                 |
| comprehensions             | 19.8 us                                                | 21.1 us: 1.07x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                |
| raytrace                   | 299 ms                                                 | 322 ms: 1.08x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.61 sec: 1.08x slower                                                |
| async_generators           | 384 ms                                                 | 416 ms: 1.08x slower                                                  |
| scimark_fft                | 342 ms                                                 | 371 ms: 1.09x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.29 us: 1.10x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.11x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 827 ms: 1.11x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 248 us: 1.12x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.71 sec: 1.13x slower                                                |
| logging_format             | 7.35 us                                                | 8.30 us: 1.13x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.6 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.5 ms: 1.13x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 162 ms: 1.13x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.13x slower                                                  |
| chaos                      | 62.8 ms                                                | 71.3 ms: 1.13x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.93 ms: 1.16x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                 |
| pyflate                    | 448 ms                                                 | 518 ms: 1.16x slower                                                  |
| html5lib                   | 63.6 ms                                                | 73.6 ms: 1.16x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 62.0 ms: 1.16x slower                                                 |
| sympy_str                  | 292 ms                                                 | 340 ms: 1.17x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.9 ms: 1.17x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                 |
| sympy_expand               | 468 ms                                                 | 553 ms: 1.18x slower                                                  |
| 2to3                       | 264 ms                                                 | 312 ms: 1.18x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.5 ms: 1.19x slower                                                 |
| thrift                     | 791 us                                                 | 940 us: 1.19x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.51 sec: 1.19x slower                                                |
| richards                   | 45.9 ms                                                | 54.9 ms: 1.19x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 138 ms: 1.21x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 375 us: 1.22x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.23x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.59 ms: 1.23x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.41 ms: 1.23x slower                                                 |
| django_template            | 34.7 ms                                                | 42.8 ms: 1.24x slower                                                 |
| richards_super             | 51.9 ms                                                | 64.1 ms: 1.24x slower                                                 |
| scimark_sor                | 130 ms                                                 | 161 ms: 1.24x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 85.0 ms: 1.24x slower                                                 |
| nqueens                    | 80.1 ms                                                | 99.4 ms: 1.24x slower                                                 |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.25x slower                                                 |
| telco                      | 6.53 ms                                                | 8.40 ms: 1.29x slower                                                 |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.71 ms: 1.36x slower                                                 |
| deltablue                  | 3.45 ms                                                | 4.81 ms: 1.40x slower                                                 |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                  |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| nbody                      | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.56x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.80 ms: 1.65x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.35 ms: 3.56x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 97.7 ms: 9.04x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250102-3.14.0a3+-8b96368-NOGIL/bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.060x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x