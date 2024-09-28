# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: dc12237
- commit date: 2024-09-28
- overall geometric mean: 1.51x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 260 ms                                                       | 408 ms: 1.57x slower                                  |
| docutils       | 2.62 sec                                                     | 3.29 sec: 1.26x slower                                |
| html5lib       | 67.0 ms                                                      | 102 ms: 1.52x slower                                  |
| tornado_http   | 114 ms                                                       | 161 ms: 1.41x slower                                  |
| Geometric mean | (ref)                                                        | 1.43x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io             | 876 ms                                                       | 949 ms: 1.08x slower                                  |
| async_tree_memoization    | 461 ms                                                       | 506 ms: 1.10x slower                                  |
| async_tree_none_tg        | 336 ms                                                       | 376 ms: 1.12x slower                                  |
| asyncio_tcp               | 505 ms                                                       | 574 ms: 1.14x slower                                  |
| async_tree_memoization_tg | 414 ms                                                       | 472 ms: 1.14x slower                                  |
| asyncio_tcp_ssl           | 1.51 sec                                                     | 1.74 sec: 1.15x slower                                |
| async_tree_none           | 354 ms                                                       | 421 ms: 1.19x slower                                  |
| async_generators          | 377 ms                                                       | 497 ms: 1.32x slower                                  |
| coroutines                | 23.6 ms                                                      | 31.4 ms: 1.33x slower                                 |
| Geometric mean            | (ref)                                                        | 1.11x slower                                          |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 217 ms                                                       | 188 ms: 1.15x faster                                  |
| float          | 77.5 ms                                                      | 153 ms: 1.98x slower                                  |
| nbody          | 85.1 ms                                                      | 223 ms: 2.62x slower                                  |
| Geometric mean | (ref)                                                        | 1.65x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.13 ms: 1.01x slower                                 |
| regex_dna      | 180 ms                                                       | 192 ms: 1.06x slower                                  |
| regex_v8       | 22.7 ms                                                      | 26.3 ms: 1.16x slower                                 |
| regex_compile  | 132 ms                                                       | 228 ms: 1.73x slower                                  |
| Geometric mean | (ref)                                                        | 1.21x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle               | 11.3 us                                                      | 10.9 us: 1.04x faster                                 |
| pickle_list          | 4.93 us                                                      | 4.77 us: 1.03x faster                                 |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                  |
| unpickle             | 14.3 us                                                      | 15.3 us: 1.07x slower                                 |
| json_loads           | 27.0 us                                                      | 29.2 us: 1.08x slower                                 |
| unpickle_list        | 4.71 us                                                      | 5.10 us: 1.08x slower                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 109 ms: 1.14x slower                                  |
| json_dumps           | 10.5 ms                                                      | 13.7 ms: 1.30x slower                                 |
| xml_etree_generate   | 85.4 ms                                                      | 112 ms: 1.31x slower                                  |
| xml_etree_process    | 59.3 ms                                                      | 92.0 ms: 1.55x slower                                 |
| tomli_loads          | 2.01 sec                                                     | 3.24 sec: 1.61x slower                                |
| unpickle_pure_python | 210 us                                                       | 408 us: 1.94x slower                                  |
| pickle_pure_python   | 294 us                                                       | 592 us: 2.01x slower                                  |
| Geometric mean       | (ref)                                                        | 1.25x slower                                          |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.1 ms: 1.36x slower                                 |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                 |
| Geometric mean         | (ref)                                                        | 1.38x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 80.7 ms: 1.66x slower                                 |
| mako            | 11.3 ms                                                      | 20.4 ms: 1.79x slower                                 |
| genshi_text     | 21.5 ms                                                      | 39.5 ms: 1.83x slower                                 |
| django_template | 34.1 ms                                                      | 64.1 ms: 1.88x slower                                 |
| Geometric mean  | (ref)                                                        | 1.79x slower                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| gc_traversal              | 3.14 ms                                                      | 2.44 ms: 1.29x faster                                 |
| create_gc_cycles          | 1.34 ms                                                      | 1.11 ms: 1.21x faster                                 |
| pidigits                  | 217 ms                                                       | 188 ms: 1.15x faster                                  |
| pickle                    | 11.3 us                                                      | 10.9 us: 1.04x faster                                 |
| pickle_list               | 4.93 us                                                      | 4.77 us: 1.03x faster                                 |
| xml_etree_parse           | 136 ms                                                       | 134 ms: 1.02x faster                                  |
| regex_effbot              | 3.08 ms                                                      | 3.13 ms: 1.01x slower                                 |
| regex_dna                 | 180 ms                                                       | 192 ms: 1.06x slower                                  |
| unpickle                  | 14.3 us                                                      | 15.3 us: 1.07x slower                                 |
| json_loads                | 27.0 us                                                      | 29.2 us: 1.08x slower                                 |
| json                      | 4.93 ms                                                      | 5.33 ms: 1.08x slower                                 |
| unpickle_list             | 4.71 us                                                      | 5.10 us: 1.08x slower                                 |
| async_tree_io             | 876 ms                                                       | 949 ms: 1.08x slower                                  |
| sqlite_synth              | 2.21 us                                                      | 2.39 us: 1.08x slower                                 |
| async_tree_memoization    | 461 ms                                                       | 506 ms: 1.10x slower                                  |
| async_tree_none_tg        | 336 ms                                                       | 376 ms: 1.12x slower                                  |
| asyncio_tcp               | 505 ms                                                       | 574 ms: 1.14x slower                                  |
| async_tree_memoization_tg | 414 ms                                                       | 472 ms: 1.14x slower                                  |
| xml_etree_iterparse       | 94.9 ms                                                      | 109 ms: 1.14x slower                                  |
| asyncio_tcp_ssl           | 1.51 sec                                                     | 1.74 sec: 1.15x slower                                |
| pathlib                   | 19.2 ms                                                      | 22.0 ms: 1.15x slower                                 |
| regex_v8                  | 22.7 ms                                                      | 26.3 ms: 1.16x slower                                 |
| async_tree_none           | 354 ms                                                       | 421 ms: 1.19x slower                                  |
| telco                     | 7.82 ms                                                      | 9.32 ms: 1.19x slower                                 |
| deepcopy                  | 355 us                                                       | 430 us: 1.21x slower                                  |
| coverage                  | 83.0 ms                                                      | 104 ms: 1.25x slower                                  |
| docutils                  | 2.62 sec                                                     | 3.29 sec: 1.26x slower                                |
| mdp                       | 2.36 sec                                                     | 3.04 sec: 1.29x slower                                |
| json_dumps                | 10.5 ms                                                      | 13.7 ms: 1.30x slower                                 |
| pylint                    | 317 ms                                                       | 415 ms: 1.31x slower                                  |
| xml_etree_generate        | 85.4 ms                                                      | 112 ms: 1.31x slower                                  |
| scimark_fft               | 349 ms                                                       | 458 ms: 1.31x slower                                  |
| async_generators          | 377 ms                                                       | 497 ms: 1.32x slower                                  |
| coroutines                | 23.6 ms                                                      | 31.4 ms: 1.33x slower                                 |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 6.36 ms: 1.35x slower                                 |
| deepcopy_memo             | 39.1 us                                                      | 53.0 us: 1.36x slower                                 |
| python_startup_no_site    | 7.39 ms                                                      | 10.1 ms: 1.36x slower                                 |
| meteor_contest            | 102 ms                                                       | 138 ms: 1.36x slower                                  |
| dulwich_log               | 74.8 ms                                                      | 103 ms: 1.38x slower                                  |
| python_startup            | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                 |
| generators                | 28.8 ms                                                      | 40.6 ms: 1.41x slower                                 |
| tornado_http              | 114 ms                                                       | 161 ms: 1.41x slower                                  |
| bpe_tokeniser             | 4.45 sec                                                     | 6.37 sec: 1.43x slower                                |
| deepcopy_reduce           | 3.11 us                                                      | 4.52 us: 1.45x slower                                 |
| pycparser                 | 1.12 sec                                                     | 1.67 sec: 1.49x slower                                |
| nqueens                   | 78.6 ms                                                      | 119 ms: 1.51x slower                                  |
| html5lib                  | 67.0 ms                                                      | 102 ms: 1.52x slower                                  |
| xml_etree_process         | 59.3 ms                                                      | 92.0 ms: 1.55x slower                                 |
| fannkuch                  | 370 ms                                                       | 577 ms: 1.56x slower                                  |
| 2to3                      | 260 ms                                                       | 408 ms: 1.57x slower                                  |
| typing_runtime_protocols  | 155 us                                                       | 245 us: 1.59x slower                                  |
| spectral_norm             | 111 ms                                                       | 177 ms: 1.59x slower                                  |
| crypto_pyaes              | 67.9 ms                                                      | 109 ms: 1.60x slower                                  |
| tomli_loads               | 2.01 sec                                                     | 3.24 sec: 1.61x slower                                |
| sympy_integrate           | 19.8 ms                                                      | 32.4 ms: 1.63x slower                                 |
| thrift                    | 778 us                                                       | 1.27 ms: 1.64x slower                                 |
| genshi_xml                | 48.8 ms                                                      | 80.7 ms: 1.66x slower                                 |
| sqlglot_normalize         | 106 ms                                                       | 177 ms: 1.67x slower                                  |
| sqlglot_optimize          | 52.7 ms                                                      | 89.6 ms: 1.70x slower                                 |
| regex_compile             | 132 ms                                                       | 228 ms: 1.73x slower                                  |
| pyflate                   | 449 ms                                                       | 775 ms: 1.73x slower                                  |
| pprint_safe_repr          | 738 ms                                                       | 1.31 sec: 1.78x slower                                |
| mako                      | 11.3 ms                                                      | 20.4 ms: 1.79x slower                                 |
| pprint_pformat            | 1.50 sec                                                     | 2.72 sec: 1.82x slower                                |
| comprehensions            | 16.5 us                                                      | 30.1 us: 1.83x slower                                 |
| genshi_text               | 21.5 ms                                                      | 39.5 ms: 1.83x slower                                 |
| django_template           | 34.1 ms                                                      | 64.1 ms: 1.88x slower                                 |
| logging_format            | 6.84 us                                                      | 13.1 us: 1.92x slower                                 |
| logging_simple            | 6.16 us                                                      | 11.9 us: 1.94x slower                                 |
| unpickle_pure_python      | 210 us                                                       | 408 us: 1.94x slower                                  |
| sympy_str                 | 275 ms                                                       | 535 ms: 1.95x slower                                  |
| richards                  | 45.2 ms                                                      | 88.2 ms: 1.95x slower                                 |
| scimark_monte_carlo       | 65.4 ms                                                      | 129 ms: 1.97x slower                                  |
| float                     | 77.5 ms                                                      | 153 ms: 1.98x slower                                  |
| scimark_sor               | 134 ms                                                       | 269 ms: 2.00x slower                                  |
| pickle_pure_python        | 294 us                                                       | 592 us: 2.01x slower                                  |
| logging_silent            | 103 ns                                                       | 210 ns: 2.05x slower                                  |
| hexiom                    | 5.99 ms                                                      | 12.3 ms: 2.05x slower                                 |
| richards_super            | 51.6 ms                                                      | 107 ms: 2.07x slower                                  |
| sqlglot_transpile         | 1.56 ms                                                      | 3.33 ms: 2.13x slower                                 |
| go                        | 141 ms                                                       | 301 ms: 2.14x slower                                  |
| scimark_lu                | 113 ms                                                       | 244 ms: 2.17x slower                                  |
| chaos                     | 57.3 ms                                                      | 127 ms: 2.22x slower                                  |
| sqlglot_parse             | 1.25 ms                                                      | 2.86 ms: 2.29x slower                                 |
| sympy_expand              | 457 ms                                                       | 1.05 sec: 2.30x slower                                |
| sympy_sum                 | 156 ms                                                       | 379 ms: 2.44x slower                                  |
| raytrace                  | 253 ms                                                       | 634 ms: 2.51x slower                                  |
| nbody                     | 85.1 ms                                                      | 223 ms: 2.62x slower                                  |
| deltablue                 | 3.12 ms                                                      | 8.89 ms: 2.85x slower                                 |
| unpack_sequence           | 44.8 ns                                                      | 149 ns: 3.33x slower                                  |
| bench_thread_pool         | 919 us                                                       | 3.14 ms: 3.42x slower                                 |
| bench_mp_pool             | 11.0 ms                                                      | 70.7 ms: 6.43x slower                                 |
| Geometric mean            | (ref)                                                        | 1.51x slower                                          |

Benchmark hidden because not significant (5): async_tree_io_tg, async_tree_cpu_io_mixed_tg, asyncio_websockets, pickle_dict, async_tree_cpu_io_mixed
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.38x
- 95% likely to have a slowdown of 1.36x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.17x