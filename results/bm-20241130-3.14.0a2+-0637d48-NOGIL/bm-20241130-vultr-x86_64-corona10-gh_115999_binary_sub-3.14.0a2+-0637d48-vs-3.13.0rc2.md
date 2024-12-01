# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 0637d48
- commit date: 2024-11-30
- overall geometric mean: 1.280x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 377 ms: 1.45x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.20 sec: 1.22x slower                                                   |
| html5lib       | 67.0 ms                                                      | 101 ms: 1.51x slower                                                     |
| Geometric mean | (ref)                                                        | 1.39x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 865 ms: 1.06x faster                                                     |
| async_tree_memoization    | 461 ms                                                       | 490 ms: 1.06x slower                                                     |
| async_tree_none_tg        | 336 ms                                                       | 368 ms: 1.09x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 463 ms: 1.12x slower                                                     |
| async_tree_none           | 354 ms                                                       | 399 ms: 1.13x slower                                                     |
| coroutines                | 23.6 ms                                                      | 28.1 ms: 1.19x slower                                                    |
| async_generators          | 377 ms                                                       | 471 ms: 1.25x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.07x slower                                                             |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                     |
| nbody          | 85.1 ms                                                      | 134 ms: 1.58x slower                                                     |
| float          | 77.5 ms                                                      | 141 ms: 1.82x slower                                                     |
| Geometric mean | (ref)                                                        | 1.34x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.87 ms: 1.08x faster                                                    |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                    |
| regex_compile  | 132 ms                                                       | 193 ms: 1.46x slower                                                     |
| Geometric mean | (ref)                                                        | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.19x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.72 sec: 1.35x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 82.2 ms: 1.38x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 372 us: 1.77x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 547 us: 1.86x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.29x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.40x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.60x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 66.9 ms: 1.37x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 33.9 ms: 1.57x slower                                                    |
| django_template | 34.1 ms                                                      | 55.7 ms: 1.63x slower                                                    |
| mako            | 11.3 ms                                                      | 19.8 ms: 1.74x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.57x slower                                                             |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 181 ms: 1.20x faster                                                     |
| regex_effbot              | 3.08 ms                                                      | 2.87 ms: 1.08x faster                                                    |
| async_tree_io_tg          | 913 ms                                                       | 865 ms: 1.06x faster                                                     |
| xml_etree_parse           | 136 ms                                                       | 133 ms: 1.03x faster                                                     |
| deepcopy                  | 355 us                                                       | 350 us: 1.01x faster                                                     |
| json                      | 4.93 ms                                                      | 5.05 ms: 1.03x slower                                                    |
| regex_dna                 | 180 ms                                                       | 187 ms: 1.04x slower                                                     |
| json_loads                | 27.0 us                                                      | 28.3 us: 1.05x slower                                                    |
| sqlite_synth              | 2.21 us                                                      | 2.32 us: 1.05x slower                                                    |
| async_tree_memoization    | 461 ms                                                       | 490 ms: 1.06x slower                                                     |
| regex_v8                  | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                    |
| pathlib                   | 19.2 ms                                                      | 20.9 ms: 1.09x slower                                                    |
| async_tree_none_tg        | 336 ms                                                       | 368 ms: 1.09x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 463 ms: 1.12x slower                                                     |
| gc_traversal              | 3.14 ms                                                      | 3.53 ms: 1.12x slower                                                    |
| async_tree_none           | 354 ms                                                       | 399 ms: 1.13x slower                                                     |
| telco                     | 7.82 ms                                                      | 8.84 ms: 1.13x slower                                                    |
| deepcopy_memo             | 39.1 us                                                      | 45.1 us: 1.15x slower                                                    |
| scimark_fft               | 349 ms                                                       | 404 ms: 1.16x slower                                                     |
| spectral_norm             | 111 ms                                                       | 132 ms: 1.19x slower                                                     |
| xml_etree_generate        | 85.4 ms                                                      | 102 ms: 1.19x slower                                                     |
| coroutines                | 23.6 ms                                                      | 28.1 ms: 1.19x slower                                                    |
| deepcopy_reduce           | 3.11 us                                                      | 3.73 us: 1.20x slower                                                    |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.69 ms: 1.21x slower                                                    |
| docutils                  | 2.62 sec                                                     | 3.20 sec: 1.22x slower                                                   |
| bpe_tokeniser             | 4.45 sec                                                     | 5.45 sec: 1.23x slower                                                   |
| coverage                  | 83.0 ms                                                      | 102 ms: 1.23x slower                                                     |
| mdp                       | 2.36 sec                                                     | 2.90 sec: 1.23x slower                                                   |
| pylint                    | 317 ms                                                       | 394 ms: 1.24x slower                                                     |
| async_generators          | 377 ms                                                       | 471 ms: 1.25x slower                                                     |
| nqueens                   | 78.6 ms                                                      | 101 ms: 1.29x slower                                                     |
| meteor_contest            | 102 ms                                                       | 134 ms: 1.32x slower                                                     |
| dulwich_log               | 74.8 ms                                                      | 98.9 ms: 1.32x slower                                                    |
| generators                | 28.8 ms                                                      | 38.4 ms: 1.33x slower                                                    |
| tomli_loads               | 2.01 sec                                                     | 2.72 sec: 1.35x slower                                                   |
| json_dumps                | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                                    |
| fannkuch                  | 370 ms                                                       | 505 ms: 1.37x slower                                                     |
| genshi_xml                | 48.8 ms                                                      | 66.9 ms: 1.37x slower                                                    |
| xml_etree_process         | 59.3 ms                                                      | 82.2 ms: 1.38x slower                                                    |
| typing_runtime_protocols  | 155 us                                                       | 215 us: 1.39x slower                                                     |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.40x slower                                                    |
| create_gc_cycles          | 1.34 ms                                                      | 1.87 ms: 1.40x slower                                                    |
| crypto_pyaes              | 67.9 ms                                                      | 95.2 ms: 1.40x slower                                                    |
| sqlglot_normalize         | 106 ms                                                       | 150 ms: 1.42x slower                                                     |
| sqlglot_optimize          | 52.7 ms                                                      | 74.9 ms: 1.42x slower                                                    |
| pycparser                 | 1.12 sec                                                     | 1.59 sec: 1.42x slower                                                   |
| 2to3                      | 260 ms                                                       | 377 ms: 1.45x slower                                                     |
| pprint_safe_repr          | 738 ms                                                       | 1.07 sec: 1.46x slower                                                   |
| regex_compile             | 132 ms                                                       | 193 ms: 1.46x slower                                                     |
| pprint_pformat            | 1.50 sec                                                     | 2.22 sec: 1.48x slower                                                   |
| html5lib                  | 67.0 ms                                                      | 101 ms: 1.51x slower                                                     |
| thrift                    | 778 us                                                       | 1.20 ms: 1.54x slower                                                    |
| sympy_integrate           | 19.8 ms                                                      | 30.7 ms: 1.55x slower                                                    |
| genshi_text               | 21.5 ms                                                      | 33.9 ms: 1.57x slower                                                    |
| nbody                     | 85.1 ms                                                      | 134 ms: 1.58x slower                                                     |
| pyflate                   | 449 ms                                                       | 713 ms: 1.59x slower                                                     |
| python_startup            | 11.0 ms                                                      | 17.5 ms: 1.60x slower                                                    |
| django_template           | 34.1 ms                                                      | 55.7 ms: 1.63x slower                                                    |
| scimark_lu                | 113 ms                                                       | 194 ms: 1.72x slower                                                     |
| mako                      | 11.3 ms                                                      | 19.8 ms: 1.74x slower                                                    |
| comprehensions            | 16.5 us                                                      | 29.0 us: 1.76x slower                                                    |
| unpickle_pure_python      | 210 us                                                       | 372 us: 1.77x slower                                                     |
| scimark_sor               | 134 ms                                                       | 241 ms: 1.79x slower                                                     |
| sympy_str                 | 275 ms                                                       | 494 ms: 1.80x slower                                                     |
| hexiom                    | 5.99 ms                                                      | 10.8 ms: 1.81x slower                                                    |
| float                     | 77.5 ms                                                      | 141 ms: 1.82x slower                                                     |
| scimark_monte_carlo       | 65.4 ms                                                      | 120 ms: 1.83x slower                                                     |
| logging_format            | 6.84 us                                                      | 12.6 us: 1.84x slower                                                    |
| richards                  | 45.2 ms                                                      | 83.2 ms: 1.84x slower                                                    |
| logging_simple            | 6.16 us                                                      | 11.4 us: 1.84x slower                                                    |
| pickle_pure_python        | 294 us                                                       | 547 us: 1.86x slower                                                     |
| logging_silent            | 103 ns                                                       | 193 ns: 1.88x slower                                                     |
| chaos                     | 57.3 ms                                                      | 109 ms: 1.90x slower                                                     |
| richards_super            | 51.6 ms                                                      | 98.4 ms: 1.91x slower                                                    |
| sqlglot_transpile         | 1.56 ms                                                      | 3.03 ms: 1.94x slower                                                    |
| go                        | 141 ms                                                       | 276 ms: 1.96x slower                                                     |
| sqlglot_parse             | 1.25 ms                                                      | 2.62 ms: 2.10x slower                                                    |
| sympy_expand              | 457 ms                                                       | 985 ms: 2.16x slower                                                     |
| sympy_sum                 | 156 ms                                                       | 358 ms: 2.30x slower                                                     |
| raytrace                  | 253 ms                                                       | 601 ms: 2.38x slower                                                     |
| deltablue                 | 3.12 ms                                                      | 8.66 ms: 2.77x slower                                                    |
| bench_thread_pool         | 919 us                                                       | 3.40 ms: 3.70x slower                                                    |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 10.01x slower                                                    |
| Geometric mean            | (ref)                                                        | 1.44x slower                                                             |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, asyncio_websockets, xml_etree_iterparse, async_tree_io
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241130-3.14.0a2+-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.280x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.31x