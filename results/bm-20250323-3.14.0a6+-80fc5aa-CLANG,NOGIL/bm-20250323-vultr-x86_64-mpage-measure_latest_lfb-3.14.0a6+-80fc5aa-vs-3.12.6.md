# Results vs. 3.12.6

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.070x faster
- HPT reliability: 93.90%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 269 ms: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 61.7 ms: 1.03x faster                                               |
| Geometric mean | (ref)                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 486 ms: 2.28x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 211 ms: 2.11x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 267 ms: 2.10x faster                                                |
| async_tree_io              | 1.08 sec                                               | 519 ms: 2.09x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 299 ms: 1.86x faster                                                |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 430 ms: 1.68x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 464 ms: 1.54x faster                                                |
| coroutines                 | 23.9 ms                                                | 19.7 ms: 1.22x faster                                               |
| async_generators           | 384 ms                                                 | 332 ms: 1.16x faster                                                |
| Geometric mean             | (ref)                                                  | 1.66x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 64.2 ms: 1.26x faster                                               |
| pidigits       | 184 ms                                                 | 187 ms: 1.01x slower                                                |
| nbody          | 89.3 ms                                                | 108 ms: 1.21x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.99 ms: 1.06x faster                                               |
| regex_compile  | 142 ms                                                 | 135 ms: 1.06x faster                                                |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                               |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.3 ms: 1.15x faster                                               |
| tomli_loads          | 2.11 sec                                               | 2.00 sec: 1.05x faster                                              |
| xml_etree_generate   | 85.2 ms                                                | 84.1 ms: 1.01x faster                                               |
| unpickle_pure_python | 221 us                                                 | 218 us: 1.01x faster                                                |
| xml_etree_process    | 59.0 ms                                                | 59.7 ms: 1.01x slower                                               |
| pickle_pure_python   | 308 us                                                 | 311 us: 1.01x slower                                                |
| xml_etree_parse      | 139 ms                                                 | 141 ms: 1.01x slower                                                |
| json_loads           | 26.5 us                                                | 29.3 us: 1.11x slower                                               |
| json_dumps           | 10.4 ms                                                | 12.6 ms: 1.22x slower                                               |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.0 ms: 1.53x slower                                               |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                               |
| Geometric mean         | (ref)                                                  | 1.55x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 50.6 ms: 1.01x slower                                               |
| genshi_text     | 22.8 ms                                                | 23.4 ms: 1.02x slower                                               |
| django_template | 34.7 ms                                                | 36.5 ms: 1.05x slower                                               |
| mako            | 11.0 ms                                                | 14.4 ms: 1.31x slower                                               |
| Geometric mean  | (ref)                                                  | 1.09x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 486 ms: 2.28x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 211 ms: 2.11x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 267 ms: 2.10x faster                                                |
| async_tree_io              | 1.08 sec                                               | 519 ms: 2.09x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 299 ms: 1.86x faster                                                |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 430 ms: 1.68x faster                                                |
| gc_traversal               | 3.46 ms                                                | 2.08 ms: 1.66x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 464 ms: 1.54x faster                                                |
| deepcopy                   | 352 us                                                 | 260 us: 1.35x faster                                                |
| logging_silent             | 109 ns                                                 | 85.3 ns: 1.28x faster                                               |
| float                      | 80.8 ms                                                | 64.2 ms: 1.26x faster                                               |
| deepcopy_memo              | 40.3 us                                                | 32.1 us: 1.26x faster                                               |
| coroutines                 | 23.9 ms                                                | 19.7 ms: 1.22x faster                                               |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                |
| spectral_norm              | 110 ms                                                 | 92.2 ms: 1.20x faster                                               |
| go                         | 139 ms                                                 | 118 ms: 1.18x faster                                                |
| comprehensions             | 19.8 us                                                | 17.0 us: 1.16x faster                                               |
| scimark_fft                | 342 ms                                                 | 294 ms: 1.16x faster                                                |
| async_generators           | 384 ms                                                 | 332 ms: 1.16x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.68 us: 1.15x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 84.3 ms: 1.15x faster                                               |
| generators                 | 32.2 ms                                                | 28.3 ms: 1.14x faster                                               |
| pathlib                    | 21.5 ms                                                | 18.9 ms: 1.14x faster                                               |
| sqlite_synth               | 2.20 us                                                | 1.96 us: 1.12x faster                                               |
| raytrace                   | 299 ms                                                 | 267 ms: 1.12x faster                                                |
| dulwich_log                | 78.9 ms                                                | 70.8 ms: 1.11x faster                                               |
| chaos                      | 62.8 ms                                                | 56.7 ms: 1.11x faster                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.29 sec: 1.10x faster                                              |
| pylint                     | 319 ms                                                 | 293 ms: 1.09x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.99 ms: 1.06x faster                                               |
| regex_compile              | 142 ms                                                 | 135 ms: 1.06x faster                                                |
| deltablue                  | 3.45 ms                                                | 3.27 ms: 1.05x faster                                               |
| scimark_monte_carlo        | 68.4 ms                                                | 65.0 ms: 1.05x faster                                               |
| tomli_loads                | 2.11 sec                                               | 2.00 sec: 1.05x faster                                              |
| html5lib                   | 63.6 ms                                                | 61.7 ms: 1.03x faster                                               |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                              |
| pyflate                    | 448 ms                                                 | 438 ms: 1.02x faster                                                |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                |
| richards                   | 45.9 ms                                                | 45.2 ms: 1.02x faster                                               |
| xml_etree_generate         | 85.2 ms                                                | 84.1 ms: 1.01x faster                                               |
| logging_simple             | 6.63 us                                                | 6.55 us: 1.01x faster                                               |
| unpickle_pure_python       | 221 us                                                 | 218 us: 1.01x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 50.6 ms: 1.01x slower                                               |
| pprint_safe_repr           | 743 ms                                                 | 751 ms: 1.01x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 59.7 ms: 1.01x slower                                               |
| pidigits                   | 184 ms                                                 | 187 ms: 1.01x slower                                                |
| pickle_pure_python         | 308 us                                                 | 311 us: 1.01x slower                                                |
| logging_format             | 7.35 us                                                | 7.44 us: 1.01x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 1.54 sec: 1.01x slower                                              |
| xml_etree_parse            | 139 ms                                                 | 141 ms: 1.01x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.46 ms: 1.01x slower                                               |
| 2to3                       | 264 ms                                                 | 269 ms: 1.02x slower                                                |
| genshi_text                | 22.8 ms                                                | 23.4 ms: 1.02x slower                                               |
| sympy_sum                  | 166 ms                                                 | 170 ms: 1.03x slower                                                |
| json                       | 5.02 ms                                                | 5.15 ms: 1.03x slower                                               |
| thrift                     | 791 us                                                 | 813 us: 1.03x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 79.0 ms: 1.03x slower                                               |
| sympy_integrate            | 20.5 ms                                                | 21.2 ms: 1.03x slower                                               |
| nqueens                    | 80.1 ms                                                | 82.7 ms: 1.03x slower                                               |
| richards_super             | 51.9 ms                                                | 53.7 ms: 1.04x slower                                               |
| sympy_str                  | 292 ms                                                 | 302 ms: 1.04x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.41 ms: 1.04x slower                                               |
| sqlalchemy_imperative      | 21.8 ms                                                | 22.7 ms: 1.04x slower                                               |
| sqlalchemy_declarative     | 143 ms                                                 | 150 ms: 1.05x slower                                                |
| django_template            | 34.7 ms                                                | 36.5 ms: 1.05x slower                                               |
| typing_runtime_protocols   | 163 us                                                 | 173 us: 1.06x slower                                                |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                               |
| sympy_expand               | 468 ms                                                 | 498 ms: 1.06x slower                                                |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                |
| fannkuch                   | 372 ms                                                 | 412 ms: 1.11x slower                                                |
| json_loads                 | 26.5 us                                                | 29.3 us: 1.11x slower                                               |
| meteor_contest             | 104 ms                                                 | 118 ms: 1.14x slower                                                |
| mdp                        | 2.42 sec                                               | 2.83 sec: 1.17x slower                                              |
| nbody                      | 89.3 ms                                                | 108 ms: 1.21x slower                                                |
| json_dumps                 | 10.4 ms                                                | 12.6 ms: 1.22x slower                                               |
| telco                      | 6.53 ms                                                | 7.98 ms: 1.22x slower                                               |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                               |
| mako                       | 11.0 ms                                                | 14.4 ms: 1.31x slower                                               |
| coverage                   | 71.4 ms                                                | 94.1 ms: 1.32x slower                                               |
| python_startup_no_site     | 7.16 ms                                                | 11.0 ms: 1.53x slower                                               |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                               |
| bench_thread_pool          | 941 us                                                 | 3.07 ms: 3.27x slower                                               |
| bench_mp_pool              | 10.8 ms                                                | 95.0 ms: 8.80x slower                                               |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                        |

Benchmark hidden because not significant (2): docutils, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250323-3.14.0a6+-80fc5aa-CLANG,NOGIL/bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 93.90% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.41x