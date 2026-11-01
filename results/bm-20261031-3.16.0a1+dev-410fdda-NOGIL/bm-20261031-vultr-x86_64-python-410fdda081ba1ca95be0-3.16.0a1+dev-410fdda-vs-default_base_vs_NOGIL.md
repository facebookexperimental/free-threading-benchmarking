# Results vs. default_base_vs_NOGIL

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: linux-x86_64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.116x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                    | 291 ms: 1.14x slower                                                      |
| docutils       | 2.31 sec                                                                  | 2.89 sec: 1.25x slower                                                    |
| html5lib       | 56.5 ms                                                                   | 64.9 ms: 1.15x slower                                                     |
| sphinx         | 979 ms                                                                    | 1.11 sec: 1.14x slower                                                    |
| Geometric mean | (ref)                                                                     | 1.17x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| asyncio_websockets         | 543 ms                                                                    | 510 ms: 1.07x faster                                                      |
| async_tree_io              | 653 ms                                                                    | 712 ms: 1.09x slower                                                      |
| async_tree_cpu_io_mixed_tg | 520 ms                                                                    | 589 ms: 1.13x slower                                                      |
| coroutines                 | 23.0 ms                                                                   | 26.2 ms: 1.14x slower                                                     |
| async_tree_memoization_tg  | 341 ms                                                                    | 403 ms: 1.18x slower                                                      |
| async_tree_cpu_io_mixed    | 506 ms                                                                    | 606 ms: 1.20x slower                                                      |
| async_tree_memoization     | 346 ms                                                                    | 417 ms: 1.21x slower                                                      |
| async_tree_none_tg         | 275 ms                                                                    | 334 ms: 1.21x slower                                                      |
| async_tree_none            | 273 ms                                                                    | 341 ms: 1.25x slower                                                      |
| async_generators           | 227 ms                                                                    | 292 ms: 1.28x slower                                                      |
| Geometric mean             | (ref)                                                                     | 1.14x slower                                                              |

Benchmark hidden because not significant (1): async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 188 ms                                                                    | 188 ms: 1.00x faster                                                      |
| float          | 72.8 ms                                                                   | 84.7 ms: 1.16x slower                                                     |
| nbody          | 90.7 ms                                                                   | 116 ms: 1.28x slower                                                      |
| Geometric mean | (ref)                                                                     | 1.14x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                   | 21.1 ms: 1.03x faster                                                     |
| regex_effbot   | 2.81 ms                                                                   | 2.99 ms: 1.06x slower                                                     |
| regex_compile  | 148 ms                                                                    | 169 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                                     | 1.04x slower                                                              |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 142 ms                                                                    | 143 ms: 1.00x slower                                                      |
| xml_etree_iterparse  | 91.5 ms                                                                   | 96.8 ms: 1.06x slower                                                     |
| tomli_loads          | 1.82 sec                                                                  | 1.99 sec: 1.09x slower                                                    |
| pickle_pure_python   | 313 us                                                                    | 347 us: 1.11x slower                                                      |
| json_loads           | 27.2 us                                                                   | 30.5 us: 1.12x slower                                                     |
| json_dumps           | 8.98 ms                                                                   | 10.2 ms: 1.14x slower                                                     |
| unpickle_pure_python | 209 us                                                                    | 239 us: 1.15x slower                                                      |
| xml_etree_generate   | 86.9 ms                                                                   | 101 ms: 1.17x slower                                                      |
| xml_etree_process    | 61.4 ms                                                                   | 75.8 ms: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                                     | 1.12x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                                   | 13.8 ms: 1.21x slower                                                     |
| python_startup_no_site | 7.51 ms                                                                   | 9.09 ms: 1.21x slower                                                     |
| Geometric mean         | (ref)                                                                     | 1.21x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 35.7 ms                                                                   | 41.3 ms: 1.16x slower                                                     |
| mako            | 11.6 ms                                                                   | 15.6 ms: 1.35x slower                                                     |
| Geometric mean  | (ref)                                                                     | 1.25x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| bench_mp_pool              | 292 ms                                                                    | 6.55 ms: 44.63x faster                                                    |
| gc_traversal               | 3.41 ms                                                                   | 1.80 ms: 1.90x faster                                                     |
| sqlite_synth               | 2.23 us                                                                   | 2.03 us: 1.10x faster                                                     |
| asyncio_websockets         | 543 ms                                                                    | 510 ms: 1.07x faster                                                      |
| regex_v8                   | 21.6 ms                                                                   | 21.1 ms: 1.03x faster                                                     |
| create_gc_cycles           | 1.34 ms                                                                   | 1.32 ms: 1.02x faster                                                     |
| pidigits                   | 188 ms                                                                    | 188 ms: 1.00x faster                                                      |
| xml_etree_parse            | 142 ms                                                                    | 143 ms: 1.00x slower                                                      |
| pycparser                  | 1.10 sec                                                                  | 1.12 sec: 1.02x slower                                                    |
| scimark_sparse_mat_mult    | 4.73 ms                                                                   | 4.85 ms: 1.02x slower                                                     |
| pathlib                    | 17.6 ms                                                                   | 18.1 ms: 1.03x slower                                                     |
| bpe_tokeniser              | 4.21 sec                                                                  | 4.38 sec: 1.04x slower                                                    |
| bench_thread_pool          | 1.34 ms                                                                   | 1.41 ms: 1.05x slower                                                     |
| scimark_fft                | 311 ms                                                                    | 328 ms: 1.05x slower                                                      |
| dulwich_log                | 67.4 ms                                                                   | 71.0 ms: 1.05x slower                                                     |
| scimark_lu                 | 120 ms                                                                    | 127 ms: 1.05x slower                                                      |
| xml_etree_iterparse        | 91.5 ms                                                                   | 96.8 ms: 1.06x slower                                                     |
| regex_effbot               | 2.81 ms                                                                   | 2.99 ms: 1.06x slower                                                     |
| scimark_sor                | 110 ms                                                                    | 119 ms: 1.08x slower                                                      |
| async_tree_io              | 653 ms                                                                    | 712 ms: 1.09x slower                                                      |
| tomli_loads                | 1.82 sec                                                                  | 1.99 sec: 1.09x slower                                                    |
| json                       | 4.93 ms                                                                   | 5.44 ms: 1.10x slower                                                     |
| telco                      | 159 ms                                                                    | 175 ms: 1.10x slower                                                      |
| k_core                     | 2.02 sec                                                                  | 2.23 sec: 1.11x slower                                                    |
| pickle_pure_python         | 313 us                                                                    | 347 us: 1.11x slower                                                      |
| chaos                      | 54.7 ms                                                                   | 60.6 ms: 1.11x slower                                                     |
| many_optionals             | 872 us                                                                    | 972 us: 1.12x slower                                                      |
| json_loads                 | 27.2 us                                                                   | 30.5 us: 1.12x slower                                                     |
| comprehensions             | 15.7 us                                                                   | 17.7 us: 1.13x slower                                                     |
| pprint_safe_repr           | 718 ms                                                                    | 812 ms: 1.13x slower                                                      |
| async_tree_cpu_io_mixed_tg | 520 ms                                                                    | 589 ms: 1.13x slower                                                      |
| deltablue                  | 3.30 ms                                                                   | 3.74 ms: 1.13x slower                                                     |
| json_dumps                 | 8.98 ms                                                                   | 10.2 ms: 1.14x slower                                                     |
| sphinx                     | 979 ms                                                                    | 1.11 sec: 1.14x slower                                                    |
| sympy_expand               | 476 ms                                                                    | 542 ms: 1.14x slower                                                      |
| coroutines                 | 23.0 ms                                                                   | 26.2 ms: 1.14x slower                                                     |
| regex_compile              | 148 ms                                                                    | 169 ms: 1.14x slower                                                      |
| subparsers                 | 8.83 ms                                                                   | 10.1 ms: 1.14x slower                                                     |
| nqueens                    | 76.1 ms                                                                   | 87.1 ms: 1.14x slower                                                     |
| mdp                        | 1.14 sec                                                                  | 1.30 sec: 1.14x slower                                                    |
| logging_simple             | 6.05 us                                                                   | 6.93 us: 1.14x slower                                                     |
| 2to3                       | 254 ms                                                                    | 291 ms: 1.14x slower                                                      |
| unpickle_pure_python       | 209 us                                                                    | 239 us: 1.15x slower                                                      |
| deepcopy_reduce            | 2.57 us                                                                   | 2.94 us: 1.15x slower                                                     |
| html5lib                   | 56.5 ms                                                                   | 64.9 ms: 1.15x slower                                                     |
| logging_format             | 6.91 us                                                                   | 7.93 us: 1.15x slower                                                     |
| spectral_norm              | 90.0 ms                                                                   | 104 ms: 1.15x slower                                                      |
| sqlglot_v2_optimize        | 50.5 ms                                                                   | 58.1 ms: 1.15x slower                                                     |
| logging_silent             | 95.5 ns                                                                   | 110 ns: 1.15x slower                                                      |
| sqlglot_v2_normalize       | 100 ms                                                                    | 116 ms: 1.15x slower                                                      |
| sympy_str                  | 279 ms                                                                    | 323 ms: 1.15x slower                                                      |
| django_template            | 35.7 ms                                                                   | 41.3 ms: 1.16x slower                                                     |
| thrift                     | 794 us                                                                    | 918 us: 1.16x slower                                                      |
| raytrace                   | 254 ms                                                                    | 294 ms: 1.16x slower                                                      |
| generators                 | 28.8 ms                                                                   | 33.3 ms: 1.16x slower                                                     |
| pyflate                    | 384 ms                                                                    | 445 ms: 1.16x slower                                                      |
| sympy_integrate            | 19.1 ms                                                                   | 22.2 ms: 1.16x slower                                                     |
| pprint_pformat             | 1.46 sec                                                                  | 1.69 sec: 1.16x slower                                                    |
| hexiom                     | 5.59 ms                                                                   | 6.49 ms: 1.16x slower                                                     |
| float                      | 72.8 ms                                                                   | 84.7 ms: 1.16x slower                                                     |
| xml_etree_generate         | 86.9 ms                                                                   | 101 ms: 1.17x slower                                                      |
| sympy_sum                  | 157 ms                                                                    | 183 ms: 1.17x slower                                                      |
| go                         | 104 ms                                                                    | 122 ms: 1.17x slower                                                      |
| deepcopy                   | 230 us                                                                    | 270 us: 1.17x slower                                                      |
| pylint                     | 108 ms                                                                    | 127 ms: 1.18x slower                                                      |
| async_tree_memoization_tg  | 341 ms                                                                    | 403 ms: 1.18x slower                                                      |
| richards                   | 44.8 ms                                                                   | 53.2 ms: 1.19x slower                                                     |
| sqlglot_v2_transpile       | 1.45 ms                                                                   | 1.73 ms: 1.19x slower                                                     |
| richards_super             | 51.0 ms                                                                   | 60.9 ms: 1.19x slower                                                     |
| async_tree_cpu_io_mixed    | 506 ms                                                                    | 606 ms: 1.20x slower                                                      |
| async_tree_memoization     | 346 ms                                                                    | 417 ms: 1.21x slower                                                      |
| python_startup             | 11.5 ms                                                                   | 13.8 ms: 1.21x slower                                                     |
| shortest_path              | 439 ms                                                                    | 531 ms: 1.21x slower                                                      |
| python_startup_no_site     | 7.51 ms                                                                   | 9.09 ms: 1.21x slower                                                     |
| deepcopy_memo              | 27.5 us                                                                   | 33.3 us: 1.21x slower                                                     |
| async_tree_none_tg         | 275 ms                                                                    | 334 ms: 1.21x slower                                                      |
| sqlglot_v2_parse           | 1.15 ms                                                                   | 1.40 ms: 1.21x slower                                                     |
| meteor_contest             | 103 ms                                                                    | 125 ms: 1.22x slower                                                      |
| xml_etree_process          | 61.4 ms                                                                   | 75.8 ms: 1.23x slower                                                     |
| connected_components       | 396 ms                                                                    | 489 ms: 1.23x slower                                                      |
| scimark_monte_carlo        | 62.3 ms                                                                   | 77.5 ms: 1.24x slower                                                     |
| typing_runtime_protocols   | 114 us                                                                    | 142 us: 1.25x slower                                                      |
| async_tree_none            | 273 ms                                                                    | 341 ms: 1.25x slower                                                      |
| docutils                   | 2.31 sec                                                                  | 2.89 sec: 1.25x slower                                                    |
| fannkuch                   | 369 ms                                                                    | 465 ms: 1.26x slower                                                      |
| nbody                      | 90.7 ms                                                                   | 116 ms: 1.28x slower                                                      |
| async_generators           | 227 ms                                                                    | 292 ms: 1.28x slower                                                      |
| crypto_pyaes               | 66.6 ms                                                                   | 87.7 ms: 1.32x slower                                                     |
| mako                       | 11.6 ms                                                                   | 15.6 ms: 1.35x slower                                                     |
| coverage                   | 82.5 ms                                                                   | 117 ms: 1.42x slower                                                      |
| Geometric mean             | (ref)                                                                     | 1.08x slower                                                              |

Benchmark hidden because not significant (2): regex_dna, async_tree_io_tg
Ignored benchmarks (8) of results/bm-20261031-3.16.0a1+dev-47c249a/bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.116x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.17x