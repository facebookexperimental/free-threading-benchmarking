# Results vs. 3.12.6

- fork: python
- ref: bbe589f93ccaf32eb95f
- machine: linux-x86_64
- commit hash: bbe589f
- commit date: 2025-07-22
- overall geometric mean: 1.073x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| html5lib       | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 585 ms: 1.85x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 264 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.8 ms: 1.13x faster                                                 |
| pidigits       | 184 ms                                                 | 217 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 164 ms: 1.02x faster                                                  |
| regex_v8       | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                |
| unpickle_pure_python | 221 us                                                 | 207 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.6 ms: 1.04x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.4 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.0 ms: 1.03x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 306 us: 1.01x faster                                                  |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 47.9 ms: 1.05x faster                                                 |
| django_template | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                 |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_io              | 1.08 sec                                               | 585 ms: 1.85x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 264 ms: 1.76x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.3 us: 1.42x faster                                                 |
| deepcopy                   | 352 us                                                 | 250 us: 1.41x faster                                                  |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.4 us: 1.29x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                  |
| raytrace                   | 299 ms                                                 | 249 ms: 1.20x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.3 ms: 1.19x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.64 us: 1.17x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| generators                 | 32.2 ms                                                | 28.1 ms: 1.15x faster                                                 |
| spectral_norm              | 110 ms                                                 | 96.6 ms: 1.14x faster                                                 |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| pylint                     | 319 ms                                                 | 281 ms: 1.14x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.84 us: 1.13x faster                                                 |
| logging_silent             | 109 ns                                                 | 96.2 ns: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                |
| crypto_pyaes               | 76.6 ms                                                | 68.0 ms: 1.13x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.8 ms: 1.13x faster                                                 |
| float                      | 80.8 ms                                                | 71.8 ms: 1.13x faster                                                 |
| pyflate                    | 448 ms                                                 | 398 ms: 1.13x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.07 ms: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 41.0 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.1 ms: 1.12x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.11x faster                                                 |
| logging_format             | 7.35 us                                                | 6.60 us: 1.11x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.2 ms: 1.10x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.66 ms: 1.09x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.08x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 686 ms: 1.08x faster                                                  |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| unpickle_pure_python       | 221 us                                                 | 207 us: 1.06x faster                                                  |
| thrift                     | 791 us                                                 | 747 us: 1.06x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| scimark_fft                | 342 ms                                                 | 326 ms: 1.05x faster                                                  |
| nqueens                    | 80.1 ms                                                | 76.5 ms: 1.05x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 47.9 ms: 1.05x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 92.6 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.1 ms: 1.04x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| xml_etree_process          | 59.0 ms                                                | 57.4 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.0 ms: 1.03x faster                                                 |
| regex_dna                  | 168 ms                                                 | 164 ms: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 306 us: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                 |
| fannkuch                   | 372 ms                                                 | 379 ms: 1.02x slower                                                  |
| json                       | 5.02 ms                                                | 5.14 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.53 ms: 1.03x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.5 ms: 1.14x slower                                                 |
| pidigits                   | 184 ms                                                 | 217 ms: 1.18x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.78 ms: 1.38x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 102 ms: 9.49x slower                                                  |
| telco                      | 6.53 ms                                                | 157 ms: 24.09x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): sympy_expand, nbody, asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250722-3.15.0a0-bbe589f/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x