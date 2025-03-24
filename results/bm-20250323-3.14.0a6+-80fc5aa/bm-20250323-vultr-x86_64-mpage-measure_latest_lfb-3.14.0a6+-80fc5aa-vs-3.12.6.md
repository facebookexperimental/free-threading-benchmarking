# Results vs. 3.12.6

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.096x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.06x faster                                                |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                              |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 632 ms: 1.76x faster                                                |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 490 ms: 1.47x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                               |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.9 ms: 1.14x faster                                               |
| nbody          | 89.3 ms                                                | 90.8 ms: 1.02x slower                                               |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.58 ms: 1.23x faster                                               |
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                  | 1.06x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.87 sec: 1.13x faster                                              |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 91.2 ms: 1.06x faster                                               |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                                |
| xml_etree_generate   | 85.2 ms                                                | 83.0 ms: 1.03x faster                                               |
| pickle_pure_python   | 308 us                                                 | 302 us: 1.02x faster                                                |
| xml_etree_process    | 59.0 ms                                                | 58.4 ms: 1.01x faster                                               |
| json_loads           | 26.5 us                                                | 27.2 us: 1.02x slower                                               |
| json_dumps           | 10.4 ms                                                | 11.0 ms: 1.07x slower                                               |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.64 ms: 1.21x slower                                               |
| python_startup         | 9.93 ms                                                | 15.0 ms: 1.51x slower                                               |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.5 ms: 1.11x faster                                               |
| genshi_xml      | 50.2 ms                                                | 47.9 ms: 1.05x faster                                               |
| django_template | 34.7 ms                                                | 34.5 ms: 1.01x faster                                               |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                               |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 632 ms: 1.76x faster                                                |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 490 ms: 1.47x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 28.6 us: 1.41x faster                                               |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                |
| go                         | 139 ms                                                 | 109 ms: 1.27x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.58 ms: 1.23x faster                                               |
| raytrace                   | 299 ms                                                 | 249 ms: 1.20x faster                                                |
| comprehensions             | 19.8 us                                                | 16.5 us: 1.20x faster                                               |
| generators                 | 32.2 ms                                                | 27.1 ms: 1.19x faster                                               |
| spectral_norm              | 110 ms                                                 | 92.9 ms: 1.19x faster                                               |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                                |
| dulwich_log                | 78.9 ms                                                | 67.4 ms: 1.17x faster                                               |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.17x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.64 us: 1.16x faster                                               |
| logging_silent             | 109 ns                                                 | 93.9 ns: 1.16x faster                                               |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                |
| float                      | 80.8 ms                                                | 70.9 ms: 1.14x faster                                               |
| chaos                      | 62.8 ms                                                | 55.2 ms: 1.14x faster                                               |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.87 sec: 1.13x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                               |
| genshi_text                | 22.8 ms                                                | 20.5 ms: 1.11x faster                                               |
| richards                   | 45.9 ms                                                | 41.3 ms: 1.11x faster                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.29 sec: 1.10x faster                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 130 ms: 1.10x faster                                                |
| richards_super             | 51.9 ms                                                | 47.2 ms: 1.10x faster                                               |
| crypto_pyaes               | 76.6 ms                                                | 69.8 ms: 1.10x faster                                               |
| pyflate                    | 448 ms                                                 | 408 ms: 1.10x faster                                                |
| sqlalchemy_imperative      | 21.8 ms                                                | 20.1 ms: 1.09x faster                                               |
| logging_simple             | 6.63 us                                                | 6.14 us: 1.08x faster                                               |
| scimark_monte_carlo        | 68.4 ms                                                | 63.5 ms: 1.08x faster                                               |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                |
| logging_format             | 7.35 us                                                | 6.84 us: 1.07x faster                                               |
| scimark_fft                | 342 ms                                                 | 318 ms: 1.07x faster                                                |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                                |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                              |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 697 ms: 1.07x faster                                                |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                              |
| deltablue                  | 3.45 ms                                                | 3.24 ms: 1.06x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 91.2 ms: 1.06x faster                                               |
| mdp                        | 2.42 sec                                               | 2.29 sec: 1.06x faster                                              |
| sympy_integrate            | 20.5 ms                                                | 19.5 ms: 1.06x faster                                               |
| 2to3                       | 264 ms                                                 | 250 ms: 1.06x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 47.9 ms: 1.05x faster                                               |
| meteor_contest             | 104 ms                                                 | 99.1 ms: 1.04x faster                                               |
| json                       | 5.02 ms                                                | 4.84 ms: 1.04x faster                                               |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.98 ms: 1.03x faster                                               |
| thrift                     | 791 us                                                 | 769 us: 1.03x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 83.0 ms: 1.03x faster                                               |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                              |
| sympy_expand               | 468 ms                                                 | 458 ms: 1.02x faster                                                |
| nqueens                    | 80.1 ms                                                | 78.5 ms: 1.02x faster                                               |
| pickle_pure_python         | 308 us                                                 | 302 us: 1.02x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                               |
| xml_etree_process          | 59.0 ms                                                | 58.4 ms: 1.01x faster                                               |
| django_template            | 34.7 ms                                                | 34.5 ms: 1.01x faster                                               |
| nbody                      | 89.3 ms                                                | 90.8 ms: 1.02x slower                                               |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                               |
| json_loads                 | 26.5 us                                                | 27.2 us: 1.02x slower                                               |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                |
| fannkuch                   | 372 ms                                                 | 390 ms: 1.05x slower                                                |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                               |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.68 ms: 1.07x slower                                               |
| json_dumps                 | 10.4 ms                                                | 11.0 ms: 1.07x slower                                               |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                               |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.11x slower                                               |
| coverage                   | 71.4 ms                                                | 80.4 ms: 1.13x slower                                               |
| telco                      | 6.53 ms                                                | 7.35 ms: 1.13x slower                                               |
| gc_traversal               | 3.46 ms                                                | 4.08 ms: 1.18x slower                                               |
| python_startup_no_site     | 7.16 ms                                                | 8.64 ms: 1.21x slower                                               |
| python_startup             | 9.93 ms                                                | 15.0 ms: 1.51x slower                                               |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                               |
| bench_mp_pool              | 10.8 ms                                                | 90.0 ms: 8.33x slower                                               |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                        |

Benchmark hidden because not significant (2): scimark_lu, asyncio_websockets
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250323-3.14.0a6+-80fc5aa/bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.13x