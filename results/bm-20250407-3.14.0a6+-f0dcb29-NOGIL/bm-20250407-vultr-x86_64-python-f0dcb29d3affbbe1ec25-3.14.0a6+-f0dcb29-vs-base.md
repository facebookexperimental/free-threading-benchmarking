# Results vs. base

- fork: python
- ref: f0dcb29d3affbbe1ec25
- machine: linux-x86_64
- commit hash: f0dcb29
- commit date: 2025-04-07
- overall geometric mean: 1.145x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                                                            | 310 ms: 1.22x slower                                                                                                    |
| docutils       | 2.58 sec                                                                                                          | 2.91 sec: 1.12x slower                                                                                                  |
| sphinx         | 1000 ms                                                                                                           | 1.15 sec: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg          | 631 ms                                                                                                            | 567 ms: 1.11x faster                                                                                                    |
| async_tree_none_tg        | 265 ms                                                                                                            | 246 ms: 1.08x faster                                                                                                    |
| async_tree_io             | 632 ms                                                                                                            | 597 ms: 1.06x faster                                                                                                    |
| async_tree_memoization_tg | 324 ms                                                                                                            | 312 ms: 1.04x faster                                                                                                    |
| asyncio_websockets        | 517 ms                                                                                                            | 516 ms: 1.00x faster                                                                                                    |
| async_tree_cpu_io_mixed   | 503 ms                                                                                                            | 525 ms: 1.05x slower                                                                                                    |
| async_tree_memoization    | 321 ms                                                                                                            | 339 ms: 1.06x slower                                                                                                    |
| coroutines                | 24.5 ms                                                                                                           | 27.0 ms: 1.10x slower                                                                                                   |
| async_generators          | 337 ms                                                                                                            | 387 ms: 1.15x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.00x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_none, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 190 ms                                                                                                            | 191 ms: 1.01x slower                                                                                                    |
| float          | 71.4 ms                                                                                                           | 77.6 ms: 1.09x slower                                                                                                   |
| nbody          | 92.6 ms                                                                                                           | 140 ms: 1.51x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.1 ms                                                                                                           | 21.7 ms: 1.02x faster                                                                                                   |
| regex_dna      | 181 ms                                                                                                            | 180 ms: 1.00x faster                                                                                                    |
| regex_effbot   | 2.84 ms                                                                                                           | 2.96 ms: 1.04x slower                                                                                                   |
| regex_compile  | 130 ms                                                                                                            | 169 ms: 1.30x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.7 ms                                                                                                           | 93.1 ms: 1.01x faster                                                                                                   |
| json_loads           | 27.7 us                                                                                                           | 30.3 us: 1.09x slower                                                                                                   |
| json_dumps           | 11.2 ms                                                                                                           | 13.2 ms: 1.17x slower                                                                                                   |
| pickle_pure_python   | 322 us                                                                                                            | 381 us: 1.18x slower                                                                                                    |
| xml_etree_generate   | 85.1 ms                                                                                                           | 101 ms: 1.19x slower                                                                                                    |
| unpickle_pure_python | 222 us                                                                                                            | 270 us: 1.22x slower                                                                                                    |
| xml_etree_process    | 60.6 ms                                                                                                           | 74.2 ms: 1.22x slower                                                                                                   |
| tomli_loads          | 1.99 sec                                                                                                          | 2.51 sec: 1.26x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                                                           | 16.0 ms: 1.06x slower                                                                                                   |
| python_startup_no_site | 8.64 ms                                                                                                           | 11.2 ms: 1.30x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.6 ms                                                                                                           | 45.1 ms: 1.23x slower                                                                                                   |
| mako            | 12.2 ms                                                                                                           | 16.5 ms: 1.35x slower                                                                                                   |
| genshi_xml      | 50.5 ms                                                                                                           | 68.4 ms: 1.36x slower                                                                                                   |
| genshi_text     | 22.0 ms                                                                                                           | 31.4 ms: 1.43x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.34x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal              | 4.26 ms                                                                                                           | 1.78 ms: 2.40x faster                                                                                                   |
| create_gc_cycles          | 1.84 ms                                                                                                           | 1.33 ms: 1.38x faster                                                                                                   |
| async_tree_io_tg          | 631 ms                                                                                                            | 567 ms: 1.11x faster                                                                                                    |
| async_tree_none_tg        | 265 ms                                                                                                            | 246 ms: 1.08x faster                                                                                                    |
| sqlite_synth              | 2.18 us                                                                                                           | 2.06 us: 1.06x faster                                                                                                   |
| async_tree_io             | 632 ms                                                                                                            | 597 ms: 1.06x faster                                                                                                    |
| async_tree_memoization_tg | 324 ms                                                                                                            | 312 ms: 1.04x faster                                                                                                    |
| regex_v8                  | 22.1 ms                                                                                                           | 21.7 ms: 1.02x faster                                                                                                   |
| xml_etree_iterparse       | 93.7 ms                                                                                                           | 93.1 ms: 1.01x faster                                                                                                   |
| regex_dna                 | 181 ms                                                                                                            | 180 ms: 1.00x faster                                                                                                    |
| asyncio_websockets        | 517 ms                                                                                                            | 516 ms: 1.00x faster                                                                                                    |
| pidigits                  | 190 ms                                                                                                            | 191 ms: 1.01x slower                                                                                                    |
| pathlib                   | 19.7 ms                                                                                                           | 19.9 ms: 1.01x slower                                                                                                   |
| json                      | 4.96 ms                                                                                                           | 5.11 ms: 1.03x slower                                                                                                   |
| regex_effbot              | 2.84 ms                                                                                                           | 2.96 ms: 1.04x slower                                                                                                   |
| async_tree_cpu_io_mixed   | 503 ms                                                                                                            | 525 ms: 1.05x slower                                                                                                    |
| async_tree_memoization    | 321 ms                                                                                                            | 339 ms: 1.06x slower                                                                                                    |
| python_startup            | 15.1 ms                                                                                                           | 16.0 ms: 1.06x slower                                                                                                   |
| pycparser                 | 1.17 sec                                                                                                          | 1.25 sec: 1.07x slower                                                                                                  |
| float                     | 71.4 ms                                                                                                           | 77.6 ms: 1.09x slower                                                                                                   |
| json_loads                | 27.7 us                                                                                                           | 30.3 us: 1.09x slower                                                                                                   |
| bench_mp_pool             | 88.9 ms                                                                                                           | 97.4 ms: 1.09x slower                                                                                                   |
| coroutines                | 24.5 ms                                                                                                           | 27.0 ms: 1.10x slower                                                                                                   |
| k_core                    | 2.06 sec                                                                                                          | 2.29 sec: 1.11x slower                                                                                                  |
| docutils                  | 2.58 sec                                                                                                          | 2.91 sec: 1.12x slower                                                                                                  |
| bpe_tokeniser             | 4.35 sec                                                                                                          | 4.94 sec: 1.14x slower                                                                                                  |
| dulwich_log               | 68.9 ms                                                                                                           | 78.3 ms: 1.14x slower                                                                                                   |
| async_generators          | 337 ms                                                                                                            | 387 ms: 1.15x slower                                                                                                    |
| pylint                    | 287 ms                                                                                                            | 331 ms: 1.15x slower                                                                                                    |
| sphinx                    | 1000 ms                                                                                                           | 1.15 sec: 1.15x slower                                                                                                  |
| many_optionals            | 1.04 ms                                                                                                           | 1.21 ms: 1.16x slower                                                                                                   |
| json_dumps                | 11.2 ms                                                                                                           | 13.2 ms: 1.17x slower                                                                                                   |
| scimark_fft               | 321 ms                                                                                                            | 379 ms: 1.18x slower                                                                                                    |
| pickle_pure_python        | 322 us                                                                                                            | 381 us: 1.18x slower                                                                                                    |
| telco                     | 7.29 ms                                                                                                           | 8.64 ms: 1.19x slower                                                                                                   |
| xml_etree_generate        | 85.1 ms                                                                                                           | 101 ms: 1.19x slower                                                                                                    |
| subparsers                | 22.5 ms                                                                                                           | 26.9 ms: 1.20x slower                                                                                                   |
| spectral_norm             | 98.0 ms                                                                                                           | 118 ms: 1.21x slower                                                                                                    |
| sqlglot_v2_normalize      | 106 ms                                                                                                            | 128 ms: 1.21x slower                                                                                                    |
| scimark_lu                | 117 ms                                                                                                            | 142 ms: 1.21x slower                                                                                                    |
| deepcopy_reduce           | 2.69 us                                                                                                           | 3.27 us: 1.21x slower                                                                                                   |
| 2to3                      | 255 ms                                                                                                            | 310 ms: 1.22x slower                                                                                                    |
| pprint_safe_repr          | 732 ms                                                                                                            | 890 ms: 1.22x slower                                                                                                    |
| unpickle_pure_python      | 222 us                                                                                                            | 270 us: 1.22x slower                                                                                                    |
| sqlglot_v2_optimize       | 52.5 ms                                                                                                           | 64.1 ms: 1.22x slower                                                                                                   |
| xml_etree_process         | 60.6 ms                                                                                                           | 74.2 ms: 1.22x slower                                                                                                   |
| sympy_sum                 | 159 ms                                                                                                            | 195 ms: 1.23x slower                                                                                                    |
| sqlalchemy_imperative     | 20.6 ms                                                                                                           | 25.3 ms: 1.23x slower                                                                                                   |
| django_template           | 36.6 ms                                                                                                           | 45.1 ms: 1.23x slower                                                                                                   |
| logging_silent            | 101 ns                                                                                                            | 124 ns: 1.24x slower                                                                                                    |
| nqueens                   | 80.8 ms                                                                                                           | 100 ms: 1.24x slower                                                                                                    |
| sympy_integrate           | 19.6 ms                                                                                                           | 24.2 ms: 1.24x slower                                                                                                   |
| sympy_expand              | 471 ms                                                                                                            | 584 ms: 1.24x slower                                                                                                    |
| pprint_pformat            | 1.49 sec                                                                                                          | 1.85 sec: 1.24x slower                                                                                                  |
| mdp                       | 1.18 sec                                                                                                          | 1.47 sec: 1.24x slower                                                                                                  |
| deepcopy                  | 262 us                                                                                                            | 327 us: 1.24x slower                                                                                                    |
| sqlalchemy_declarative    | 132 ms                                                                                                            | 165 ms: 1.25x slower                                                                                                    |
| sqlglot_v2_transpile      | 1.59 ms                                                                                                           | 2.00 ms: 1.25x slower                                                                                                   |
| sympy_str                 | 281 ms                                                                                                            | 352 ms: 1.25x slower                                                                                                    |
| pyflate                   | 420 ms                                                                                                            | 529 ms: 1.26x slower                                                                                                    |
| shortest_path             | 441 ms                                                                                                            | 556 ms: 1.26x slower                                                                                                    |
| tomli_loads               | 1.99 sec                                                                                                          | 2.51 sec: 1.26x slower                                                                                                  |
| typing_runtime_protocols  | 162 us                                                                                                            | 206 us: 1.27x slower                                                                                                    |
| scimark_sparse_mat_mult   | 4.40 ms                                                                                                           | 5.59 ms: 1.27x slower                                                                                                   |
| comprehensions            | 17.3 us                                                                                                           | 22.0 us: 1.27x slower                                                                                                   |
| chaos                     | 55.9 ms                                                                                                           | 71.8 ms: 1.28x slower                                                                                                   |
| sqlglot_v2_parse          | 1.28 ms                                                                                                           | 1.65 ms: 1.29x slower                                                                                                   |
| connected_components      | 399 ms                                                                                                            | 512 ms: 1.29x slower                                                                                                    |
| python_startup_no_site    | 8.64 ms                                                                                                           | 11.2 ms: 1.30x slower                                                                                                   |
| fannkuch                  | 396 ms                                                                                                            | 514 ms: 1.30x slower                                                                                                    |
| regex_compile             | 130 ms                                                                                                            | 169 ms: 1.30x slower                                                                                                    |
| crypto_pyaes              | 69.7 ms                                                                                                           | 90.9 ms: 1.30x slower                                                                                                   |
| raytrace                  | 260 ms                                                                                                            | 341 ms: 1.31x slower                                                                                                    |
| scimark_sor               | 115 ms                                                                                                            | 151 ms: 1.31x slower                                                                                                    |
| hexiom                    | 6.12 ms                                                                                                           | 8.08 ms: 1.32x slower                                                                                                   |
| deltablue                 | 3.36 ms                                                                                                           | 4.45 ms: 1.33x slower                                                                                                   |
| go                        | 114 ms                                                                                                            | 153 ms: 1.34x slower                                                                                                    |
| richards                  | 44.5 ms                                                                                                           | 59.8 ms: 1.34x slower                                                                                                   |
| mako                      | 12.2 ms                                                                                                           | 16.5 ms: 1.35x slower                                                                                                   |
| logging_simple            | 6.24 us                                                                                                           | 8.42 us: 1.35x slower                                                                                                   |
| meteor_contest            | 101 ms                                                                                                            | 136 ms: 1.35x slower                                                                                                    |
| deepcopy_memo             | 29.7 us                                                                                                           | 40.2 us: 1.35x slower                                                                                                   |
| scimark_monte_carlo       | 63.8 ms                                                                                                           | 86.4 ms: 1.35x slower                                                                                                   |
| genshi_xml                | 50.5 ms                                                                                                           | 68.4 ms: 1.36x slower                                                                                                   |
| richards_super            | 50.3 ms                                                                                                           | 68.3 ms: 1.36x slower                                                                                                   |
| logging_format            | 6.92 us                                                                                                           | 9.56 us: 1.38x slower                                                                                                   |
| coverage                  | 79.9 ms                                                                                                           | 111 ms: 1.38x slower                                                                                                    |
| genshi_text               | 22.0 ms                                                                                                           | 31.4 ms: 1.43x slower                                                                                                   |
| nbody                     | 92.6 ms                                                                                                           | 140 ms: 1.51x slower                                                                                                    |
| generators                | 29.2 ms                                                                                                           | 44.5 ms: 1.52x slower                                                                                                   |
| bench_thread_pool         | 1.06 ms                                                                                                           | 3.18 ms: 3.02x slower                                                                                                   |
| Geometric mean            | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_none, async_tree_cpu_io_mixed_tg, xml_etree_parse
Ignored benchmarks (1) of results/bm-20250407-3.14.0a6+-f0dcb29-NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json: html5lib

- Geometric mean (including insignificant results): 1.145x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.20x