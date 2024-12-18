# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 47b80b4
- commit date: 2024-12-19
- overall geometric mean: 1.246x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 366 ms: 1.41x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.10 sec: 1.18x slower                                                   |
| html5lib       | 67.0 ms                                                      | 98.8 ms: 1.47x slower                                                    |
| Geometric mean | (ref)                                                        | 1.35x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 823 ms: 1.11x faster                                                     |
| async_tree_io             | 876 ms                                                       | 852 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 652 ms: 1.02x faster                                                     |
| asyncio_websockets        | 520 ms                                                       | 517 ms: 1.01x faster                                                     |
| coroutines                | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                    |
| async_tree_none_tg        | 336 ms                                                       | 358 ms: 1.06x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 443 ms: 1.07x slower                                                     |
| async_tree_none           | 354 ms                                                       | 387 ms: 1.09x slower                                                     |
| async_generators          | 377 ms                                                       | 452 ms: 1.20x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.03x slower                                                             |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 182 ms: 1.19x faster                                                     |
| nbody          | 85.1 ms                                                      | 134 ms: 1.57x slower                                                     |
| float          | 77.5 ms                                                      | 140 ms: 1.81x slower                                                     |
| Geometric mean | (ref)                                                        | 1.34x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.90 ms: 1.06x faster                                                    |
| regex_dna      | 180 ms                                                       | 184 ms: 1.02x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                    |
| regex_compile  | 132 ms                                                       | 179 ms: 1.35x slower                                                     |
| Geometric mean | (ref)                                                        | 1.09x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 97.3 ms: 1.14x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 77.4 ms: 1.30x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.66 sec: 1.33x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.5 ms: 1.37x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 335 us: 1.60x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 511 us: 1.73x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.3 ms: 1.30x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 31.7 ms: 1.47x slower                                                    |
| django_template | 34.1 ms                                                      | 51.4 ms: 1.51x slower                                                    |
| mako            | 11.3 ms                                                      | 17.7 ms: 1.56x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.46x slower                                                             |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 182 ms: 1.19x faster                                                     |
| async_tree_io_tg          | 913 ms                                                       | 823 ms: 1.11x faster                                                     |
| deepcopy                  | 355 us                                                       | 327 us: 1.09x faster                                                     |
| regex_effbot              | 3.08 ms                                                      | 2.90 ms: 1.06x faster                                                    |
| xml_etree_iterparse       | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                    |
| xml_etree_parse           | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| async_tree_io             | 876 ms                                                       | 852 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 652 ms: 1.02x faster                                                     |
| asyncio_websockets        | 520 ms                                                       | 517 ms: 1.01x faster                                                     |
| gc_traversal              | 3.14 ms                                                      | 3.17 ms: 1.01x slower                                                    |
| deepcopy_memo             | 39.1 us                                                      | 39.5 us: 1.01x slower                                                    |
| regex_dna                 | 180 ms                                                       | 184 ms: 1.02x slower                                                     |
| json                      | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                                    |
| sqlite_synth              | 2.21 us                                                      | 2.29 us: 1.04x slower                                                    |
| json_loads                | 27.0 us                                                      | 28.2 us: 1.04x slower                                                    |
| coroutines                | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                    |
| async_tree_none_tg        | 336 ms                                                       | 358 ms: 1.06x slower                                                     |
| pathlib                   | 19.2 ms                                                      | 20.4 ms: 1.07x slower                                                    |
| async_tree_memoization_tg | 414 ms                                                       | 443 ms: 1.07x slower                                                     |
| spectral_norm             | 111 ms                                                       | 120 ms: 1.08x slower                                                     |
| async_tree_none           | 354 ms                                                       | 387 ms: 1.09x slower                                                     |
| regex_v8                  | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                    |
| telco                     | 7.82 ms                                                      | 8.66 ms: 1.11x slower                                                    |
| deepcopy_reduce           | 3.11 us                                                      | 3.48 us: 1.12x slower                                                    |
| bpe_tokeniser             | 4.45 sec                                                     | 5.00 sec: 1.13x slower                                                   |
| xml_etree_generate        | 85.4 ms                                                      | 97.3 ms: 1.14x slower                                                    |
| scimark_fft               | 349 ms                                                       | 402 ms: 1.15x slower                                                     |
| docutils                  | 2.62 sec                                                     | 3.10 sec: 1.18x slower                                                   |
| coverage                  | 83.0 ms                                                      | 99.1 ms: 1.19x slower                                                    |
| async_generators          | 377 ms                                                       | 452 ms: 1.20x slower                                                     |
| pylint                    | 317 ms                                                       | 381 ms: 1.20x slower                                                     |
| mdp                       | 2.36 sec                                                     | 2.84 sec: 1.21x slower                                                   |
| nqueens                   | 78.6 ms                                                      | 96.0 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.93 ms: 1.26x slower                                                    |
| meteor_contest            | 102 ms                                                       | 128 ms: 1.26x slower                                                     |
| dulwich_log               | 74.8 ms                                                      | 95.5 ms: 1.28x slower                                                    |
| sqlglot_normalize         | 106 ms                                                       | 135 ms: 1.28x slower                                                     |
| genshi_xml                | 48.8 ms                                                      | 63.3 ms: 1.30x slower                                                    |
| xml_etree_process         | 59.3 ms                                                      | 77.4 ms: 1.30x slower                                                    |
| sqlglot_optimize          | 52.7 ms                                                      | 68.8 ms: 1.31x slower                                                    |
| pprint_safe_repr          | 738 ms                                                       | 970 ms: 1.32x slower                                                     |
| typing_runtime_protocols  | 155 us                                                       | 204 us: 1.32x slower                                                     |
| generators                | 28.8 ms                                                      | 38.1 ms: 1.32x slower                                                    |
| tomli_loads               | 2.01 sec                                                     | 2.66 sec: 1.33x slower                                                   |
| fannkuch                  | 370 ms                                                       | 492 ms: 1.33x slower                                                     |
| create_gc_cycles          | 1.34 ms                                                      | 1.80 ms: 1.35x slower                                                    |
| pprint_pformat            | 1.50 sec                                                     | 2.02 sec: 1.35x slower                                                   |
| regex_compile             | 132 ms                                                       | 179 ms: 1.35x slower                                                     |
| crypto_pyaes              | 67.9 ms                                                      | 92.1 ms: 1.36x slower                                                    |
| pycparser                 | 1.12 sec                                                     | 1.52 sec: 1.37x slower                                                   |
| json_dumps                | 10.5 ms                                                      | 14.5 ms: 1.37x slower                                                    |
| python_startup_no_site    | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| scimark_lu                | 113 ms                                                       | 156 ms: 1.39x slower                                                     |
| 2to3                      | 260 ms                                                       | 366 ms: 1.41x slower                                                     |
| genshi_text               | 21.5 ms                                                      | 31.7 ms: 1.47x slower                                                    |
| thrift                    | 778 us                                                       | 1.15 ms: 1.47x slower                                                    |
| html5lib                  | 67.0 ms                                                      | 98.8 ms: 1.47x slower                                                    |
| sympy_integrate           | 19.8 ms                                                      | 29.4 ms: 1.48x slower                                                    |
| django_template           | 34.1 ms                                                      | 51.4 ms: 1.51x slower                                                    |
| pyflate                   | 449 ms                                                       | 691 ms: 1.54x slower                                                     |
| mako                      | 11.3 ms                                                      | 17.7 ms: 1.56x slower                                                    |
| nbody                     | 85.1 ms                                                      | 134 ms: 1.57x slower                                                     |
| python_startup            | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                    |
| unpickle_pure_python      | 210 us                                                       | 335 us: 1.60x slower                                                     |
| hexiom                    | 5.99 ms                                                      | 9.72 ms: 1.62x slower                                                    |
| scimark_sor               | 134 ms                                                       | 221 ms: 1.64x slower                                                     |
| comprehensions            | 16.5 us                                                      | 27.5 us: 1.67x slower                                                    |
| richards_super            | 51.6 ms                                                      | 86.9 ms: 1.68x slower                                                    |
| richards                  | 45.2 ms                                                      | 76.9 ms: 1.70x slower                                                    |
| logging_format            | 6.84 us                                                      | 11.8 us: 1.72x slower                                                    |
| logging_simple            | 6.16 us                                                      | 10.6 us: 1.72x slower                                                    |
| sympy_str                 | 275 ms                                                       | 476 ms: 1.73x slower                                                     |
| pickle_pure_python        | 294 us                                                       | 511 us: 1.73x slower                                                     |
| logging_silent            | 103 ns                                                       | 184 ns: 1.79x slower                                                     |
| float                     | 77.5 ms                                                      | 140 ms: 1.81x slower                                                     |
| chaos                     | 57.3 ms                                                      | 105 ms: 1.83x slower                                                     |
| scimark_monte_carlo       | 65.4 ms                                                      | 120 ms: 1.84x slower                                                     |
| sqlglot_transpile         | 1.56 ms                                                      | 2.97 ms: 1.91x slower                                                    |
| go                        | 141 ms                                                       | 271 ms: 1.92x slower                                                     |
| sqlglot_parse             | 1.25 ms                                                      | 2.57 ms: 2.06x slower                                                    |
| sympy_expand              | 457 ms                                                       | 953 ms: 2.08x slower                                                     |
| raytrace                  | 253 ms                                                       | 547 ms: 2.17x slower                                                     |
| sympy_sum                 | 156 ms                                                       | 350 ms: 2.25x slower                                                     |
| deltablue                 | 3.12 ms                                                      | 7.98 ms: 2.55x slower                                                    |
| bench_thread_pool         | 919 us                                                       | 3.43 ms: 3.73x slower                                                    |
| bench_mp_pool             | 11.0 ms                                                      | 109 ms: 9.87x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.37x slower                                                             |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241219-3.14.0a2+-47b80b4-NOGIL/bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.246x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.31x