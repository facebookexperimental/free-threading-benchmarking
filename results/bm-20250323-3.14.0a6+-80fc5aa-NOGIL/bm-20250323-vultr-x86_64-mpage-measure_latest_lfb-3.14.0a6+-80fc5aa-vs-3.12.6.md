# Results vs. 3.12.6

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.023x slower
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 289 ms: 1.10x slower                                                |
| docutils       | 2.64 sec                                               | 2.75 sec: 1.04x slower                                              |
| html5lib       | 63.6 ms                                                | 68.1 ms: 1.07x slower                                               |
| Geometric mean | (ref)                                                  | 1.07x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 541 ms: 2.05x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 294 ms: 1.91x faster                                                |
| async_tree_io              | 1.08 sec                                               | 573 ms: 1.89x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 326 ms: 1.70x faster                                                |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                                |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                               |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.8 ms: 1.12x faster                                               |
| pidigits       | 184 ms                                                 | 198 ms: 1.08x slower                                                |
| nbody          | 89.3 ms                                                | 120 ms: 1.35x slower                                                |
| Geometric mean | (ref)                                                  | 1.09x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                               |
| regex_dna      | 168 ms                                                 | 168 ms: 1.00x slower                                                |
| regex_v8       | 20.6 ms                                                | 21.3 ms: 1.04x slower                                               |
| regex_compile  | 142 ms                                                 | 153 ms: 1.08x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                               |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                                |
| tomli_loads          | 2.11 sec                                               | 2.25 sec: 1.07x slower                                              |
| unpickle_pure_python | 221 us                                                 | 244 us: 1.11x slower                                                |
| pickle_pure_python   | 308 us                                                 | 343 us: 1.12x slower                                                |
| json_loads           | 26.5 us                                                | 29.8 us: 1.12x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.13x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 70.7 ms: 1.20x slower                                               |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                               |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                               |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                               |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.8 ms: 1.15x slower                                               |
| genshi_text     | 22.8 ms                                                | 27.1 ms: 1.19x slower                                               |
| django_template | 34.7 ms                                                | 41.8 ms: 1.20x slower                                               |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                               |
| Geometric mean  | (ref)                                                  | 1.24x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 541 ms: 2.05x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 294 ms: 1.91x faster                                                |
| async_tree_io              | 1.08 sec                                               | 573 ms: 1.89x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 326 ms: 1.70x faster                                                |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                                |
| deepcopy                   | 352 us                                                 | 301 us: 1.17x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                               |
| float                      | 80.8 ms                                                | 71.8 ms: 1.12x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                               |
| sqlite_synth               | 2.20 us                                                | 2.00 us: 1.10x faster                                               |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                               |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 37.3 us: 1.08x faster                                               |
| dulwich_log                | 78.9 ms                                                | 74.2 ms: 1.06x faster                                               |
| go                         | 139 ms                                                 | 135 ms: 1.03x faster                                                |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                               |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.72 sec: 1.00x faster                                              |
| regex_dna                  | 168 ms                                                 | 168 ms: 1.00x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.10 us: 1.01x slower                                               |
| logging_silent             | 109 ns                                                 | 111 ns: 1.02x slower                                                |
| raytrace                   | 299 ms                                                 | 307 ms: 1.03x slower                                                |
| comprehensions             | 19.8 us                                                | 20.4 us: 1.03x slower                                               |
| regex_v8                   | 20.6 ms                                                | 21.3 ms: 1.04x slower                                               |
| docutils                   | 2.64 sec                                               | 2.75 sec: 1.04x slower                                              |
| generators                 | 32.2 ms                                                | 33.7 ms: 1.05x slower                                               |
| chaos                      | 62.8 ms                                                | 66.4 ms: 1.06x slower                                               |
| scimark_fft                | 342 ms                                                 | 364 ms: 1.07x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.25 sec: 1.07x slower                                              |
| html5lib                   | 63.6 ms                                                | 68.1 ms: 1.07x slower                                               |
| deltablue                  | 3.45 ms                                                | 3.70 ms: 1.07x slower                                               |
| pidigits                   | 184 ms                                                 | 198 ms: 1.08x slower                                                |
| regex_compile              | 142 ms                                                 | 153 ms: 1.08x slower                                                |
| pyflate                    | 448 ms                                                 | 489 ms: 1.09x slower                                                |
| 2to3                       | 264 ms                                                 | 289 ms: 1.10x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 816 ms: 1.10x slower                                                |
| thrift                     | 791 us                                                 | 872 us: 1.10x slower                                                |
| logging_simple             | 6.63 us                                                | 7.32 us: 1.10x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.11x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.11x slower                                               |
| unpickle_pure_python       | 221 us                                                 | 244 us: 1.11x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                                |
| logging_format             | 7.35 us                                                | 8.16 us: 1.11x slower                                               |
| pickle_pure_python         | 308 us                                                 | 343 us: 1.12x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 85.9 ms: 1.12x slower                                               |
| json_loads                 | 26.5 us                                                | 29.8 us: 1.12x slower                                               |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                                |
| mdp                        | 2.42 sec                                               | 2.74 sec: 1.13x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.13x slower                                               |
| sympy_str                  | 292 ms                                                 | 332 ms: 1.14x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 23.4 ms: 1.14x slower                                               |
| genshi_xml                 | 50.2 ms                                                | 57.8 ms: 1.15x slower                                               |
| scimark_monte_carlo        | 68.4 ms                                                | 78.9 ms: 1.15x slower                                               |
| richards                   | 45.9 ms                                                | 53.8 ms: 1.17x slower                                               |
| typing_runtime_protocols   | 163 us                                                 | 194 us: 1.18x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.21 ms: 1.19x slower                                               |
| genshi_text                | 22.8 ms                                                | 27.1 ms: 1.19x slower                                               |
| sympy_expand               | 468 ms                                                 | 558 ms: 1.19x slower                                                |
| richards_super             | 51.9 ms                                                | 62.1 ms: 1.20x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 70.7 ms: 1.20x slower                                               |
| hexiom                     | 6.17 ms                                                | 7.42 ms: 1.20x slower                                               |
| django_template            | 34.7 ms                                                | 41.8 ms: 1.20x slower                                               |
| nqueens                    | 80.1 ms                                                | 96.6 ms: 1.21x slower                                               |
| scimark_lu                 | 114 ms                                                 | 138 ms: 1.21x slower                                                |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                               |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                               |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.23x slower                                                |
| fannkuch                   | 372 ms                                                 | 466 ms: 1.25x slower                                                |
| nbody                      | 89.3 ms                                                | 120 ms: 1.35x slower                                                |
| telco                      | 6.53 ms                                                | 8.94 ms: 1.37x slower                                               |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                               |
| coverage                   | 71.4 ms                                                | 107 ms: 1.50x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                               |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                               |
| bench_thread_pool          | 941 us                                                 | 3.14 ms: 3.34x slower                                               |
| bench_mp_pool              | 10.8 ms                                                | 97.1 ms: 9.00x slower                                               |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                        |

Benchmark hidden because not significant (4): pylint, scimark_sor, asyncio_websockets, json
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250323-3.14.0a6+-80fc5aa-NOGIL/bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.023x slower

# HPT report

- Reliability score: 99.79% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x