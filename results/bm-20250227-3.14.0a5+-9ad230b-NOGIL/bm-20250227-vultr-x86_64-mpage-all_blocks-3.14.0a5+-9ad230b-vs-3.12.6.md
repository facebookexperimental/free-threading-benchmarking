# Results vs. 3.12.6

- fork: mpage
- ref: all_blocks
- machine: linux-x86_64
- commit hash: 9ad230b
- commit date: 2025-02-27
- overall geometric mean: 1.029x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 296 ms: 1.12x slower                                        |
| docutils       | 2.64 sec                                               | 2.77 sec: 1.05x slower                                      |
| html5lib       | 63.6 ms                                                | 68.9 ms: 1.08x slower                                       |
| Geometric mean | (ref)                                                  | 1.08x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 532 ms: 2.08x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 231 ms: 1.93x faster                                        |
| async_tree_io              | 1.08 sec                                               | 563 ms: 1.92x faster                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 297 ms: 1.88x faster                                        |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 530 ms: 1.36x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 562 ms: 1.27x faster                                        |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                        |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                       |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.7 ms: 1.14x faster                                       |
| pidigits       | 184 ms                                                 | 216 ms: 1.17x slower                                        |
| nbody          | 89.3 ms                                                | 120 ms: 1.35x slower                                        |
| Geometric mean | (ref)                                                  | 1.11x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.15x faster                                       |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                        |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                        |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                       |
| Geometric mean | (ref)                                                  | 1.04x slower                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                       |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                        |
| tomli_loads          | 2.11 sec                                               | 2.20 sec: 1.04x slower                                      |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                        |
| pickle_pure_python   | 308 us                                                 | 342 us: 1.11x slower                                        |
| json_loads           | 26.5 us                                                | 29.6 us: 1.12x slower                                       |
| xml_etree_generate   | 85.2 ms                                                | 95.7 ms: 1.12x slower                                       |
| xml_etree_process    | 59.0 ms                                                | 69.5 ms: 1.18x slower                                       |
| json_dumps           | 10.4 ms                                                | 12.6 ms: 1.22x slower                                       |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.64 ms: 1.35x slower                                       |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                       |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.8 ms: 1.15x slower                                       |
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                       |
| django_template | 34.7 ms                                                | 42.1 ms: 1.21x slower                                       |
| mako            | 11.0 ms                                                | 15.6 ms: 1.41x slower                                       |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 532 ms: 2.08x faster                                        |
| gc_traversal               | 3.46 ms                                                | 1.71 ms: 2.02x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 231 ms: 1.93x faster                                        |
| async_tree_io              | 1.08 sec                                               | 563 ms: 1.92x faster                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 297 ms: 1.88x faster                                        |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 530 ms: 1.36x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 562 ms: 1.27x faster                                        |
| deepcopy                   | 352 us                                                 | 294 us: 1.20x faster                                        |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.15x faster                                       |
| float                      | 80.8 ms                                                | 70.7 ms: 1.14x faster                                       |
| deepcopy_memo              | 40.3 us                                                | 35.3 us: 1.14x faster                                       |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.11x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                       |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                        |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                       |
| go                         | 139 ms                                                 | 129 ms: 1.08x faster                                        |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                        |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                        |
| comprehensions             | 19.8 us                                                | 19.4 us: 1.02x faster                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.62 sec: 1.02x faster                                      |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                        |
| deepcopy_reduce            | 3.08 us                                                | 3.03 us: 1.01x faster                                       |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                       |
| generators                 | 32.2 ms                                                | 33.0 ms: 1.02x slower                                       |
| dulwich_log                | 78.9 ms                                                | 82.1 ms: 1.04x slower                                       |
| tomli_loads                | 2.11 sec                                               | 2.20 sec: 1.04x slower                                      |
| docutils                   | 2.64 sec                                               | 2.77 sec: 1.05x slower                                      |
| scimark_sor                | 130 ms                                                 | 136 ms: 1.05x slower                                        |
| deltablue                  | 3.45 ms                                                | 3.62 ms: 1.05x slower                                       |
| chaos                      | 62.8 ms                                                | 66.1 ms: 1.05x slower                                       |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                        |
| mdp                        | 2.42 sec                                               | 2.57 sec: 1.06x slower                                      |
| pprint_safe_repr           | 743 ms                                                 | 793 ms: 1.07x slower                                        |
| pyflate                    | 448 ms                                                 | 478 ms: 1.07x slower                                        |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                        |
| pprint_pformat             | 1.52 sec                                               | 1.63 sec: 1.07x slower                                      |
| logging_simple             | 6.63 us                                                | 7.16 us: 1.08x slower                                       |
| html5lib                   | 63.6 ms                                                | 68.9 ms: 1.08x slower                                       |
| sqlglot_transpile          | 1.67 ms                                                | 1.81 ms: 1.08x slower                                       |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                        |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.8 ms: 1.09x slower                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                        |
| sqlglot_parse              | 1.36 ms                                                | 1.49 ms: 1.10x slower                                       |
| thrift                     | 791 us                                                 | 872 us: 1.10x slower                                        |
| crypto_pyaes               | 76.6 ms                                                | 84.9 ms: 1.11x slower                                       |
| pickle_pure_python         | 308 us                                                 | 342 us: 1.11x slower                                        |
| logging_format             | 7.35 us                                                | 8.19 us: 1.11x slower                                       |
| json_loads                 | 26.5 us                                                | 29.6 us: 1.12x slower                                       |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.12x slower                                        |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                        |
| xml_etree_generate         | 85.2 ms                                                | 95.7 ms: 1.12x slower                                       |
| 2to3                       | 264 ms                                                 | 296 ms: 1.12x slower                                        |
| sqlglot_optimize           | 53.3 ms                                                | 60.3 ms: 1.13x slower                                       |
| sympy_str                  | 292 ms                                                 | 331 ms: 1.13x slower                                        |
| richards                   | 45.9 ms                                                | 52.6 ms: 1.14x slower                                       |
| sympy_integrate            | 20.5 ms                                                | 23.6 ms: 1.15x slower                                       |
| genshi_xml                 | 50.2 ms                                                | 57.8 ms: 1.15x slower                                       |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                       |
| hexiom                     | 6.17 ms                                                | 7.15 ms: 1.16x slower                                       |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                       |
| sympy_expand               | 468 ms                                                 | 545 ms: 1.16x slower                                        |
| pidigits                   | 184 ms                                                 | 216 ms: 1.17x slower                                        |
| xml_etree_process          | 59.0 ms                                                | 69.5 ms: 1.18x slower                                       |
| richards_super             | 51.9 ms                                                | 61.1 ms: 1.18x slower                                       |
| nqueens                    | 80.1 ms                                                | 94.7 ms: 1.18x slower                                       |
| create_gc_cycles           | 1.09 ms                                                | 1.30 ms: 1.19x slower                                       |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                        |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                        |
| django_template            | 34.7 ms                                                | 42.1 ms: 1.21x slower                                       |
| json_dumps                 | 10.4 ms                                                | 12.6 ms: 1.22x slower                                       |
| fannkuch                   | 372 ms                                                 | 471 ms: 1.27x slower                                        |
| scimark_monte_carlo        | 68.4 ms                                                | 89.1 ms: 1.30x slower                                       |
| telco                      | 6.53 ms                                                | 8.60 ms: 1.32x slower                                       |
| scimark_fft                | 342 ms                                                 | 454 ms: 1.33x slower                                        |
| scimark_lu                 | 114 ms                                                 | 153 ms: 1.34x slower                                        |
| python_startup_no_site     | 7.16 ms                                                | 9.64 ms: 1.35x slower                                       |
| nbody                      | 89.3 ms                                                | 120 ms: 1.35x slower                                        |
| coverage                   | 71.4 ms                                                | 96.5 ms: 1.35x slower                                       |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.41x slower                                       |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 7.38 ms: 1.68x slower                                       |
| bench_thread_pool          | 941 us                                                 | 3.27 ms: 3.47x slower                                       |
| bench_mp_pool              | 10.8 ms                                                | 95.3 ms: 8.82x slower                                       |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                |

Benchmark hidden because not significant (5): pylint, asyncio_websockets, raytrace, pycparser, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250227-3.14.0a5+-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.029x slower

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x