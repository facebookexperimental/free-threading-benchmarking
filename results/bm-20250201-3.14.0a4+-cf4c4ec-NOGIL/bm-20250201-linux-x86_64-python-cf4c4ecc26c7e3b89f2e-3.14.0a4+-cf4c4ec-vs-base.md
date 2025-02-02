# Results vs. base

- fork: python
- ref: cf4c4ecc26c7e3b89f2e
- machine: linux-x86_64
- commit hash: cf4c4ec
- commit date: 2025-02-01
- overall geometric mean: 1.133x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 461 ms                                                                                                            | 562 ms: 1.22x slower                                                                                                    |
| docutils       | 3.54 sec                                                                                                          | 4.07 sec: 1.15x slower                                                                                                  |
| html5lib       | 84.0 ms                                                                                                           | 98.6 ms: 1.17x slower                                                                                                   |
| sphinx         | 1.54 sec                                                                                                          | 1.70 sec: 1.11x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 909 ms                                                                                                            | 801 ms: 1.13x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 732 ms                                                                                                            | 648 ms: 1.13x faster                                                                                                    |
| async_tree_io              | 890 ms                                                                                                            | 838 ms: 1.06x faster                                                                                                    |
| async_tree_none            | 386 ms                                                                                                            | 406 ms: 1.05x slower                                                                                                    |
| async_generators           | 535 ms                                                                                                            | 564 ms: 1.05x slower                                                                                                    |
| async_tree_memoization_tg  | 467 ms                                                                                                            | 506 ms: 1.08x slower                                                                                                    |
| coroutines                 | 31.0 ms                                                                                                           | 34.3 ms: 1.11x slower                                                                                                   |
| asyncio_websockets         | 724 ms                                                                                                            | 817 ms: 1.13x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 682 ms                                                                                                            | 795 ms: 1.17x slower                                                                                                    |
| asyncio_tcp                | 966 ms                                                                                                            | 1.21 sec: 1.25x slower                                                                                                  |
| asyncio_tcp_ssl            | 2.77 sec                                                                                                          | 3.50 sec: 1.26x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_none_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                                                                            | 194 ms: 1.54x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.29 ms                                                                                                           | 4.48 ms: 1.04x slower                                                                                                   |
| regex_dna      | 268 ms                                                                                                            | 310 ms: 1.15x slower                                                                                                    |
| regex_compile  | 164 ms                                                                                                            | 211 ms: 1.29x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle_list          | 7.83 us                                                                                                           | 7.27 us: 1.08x faster                                                                                                   |
| pickle_dict          | 48.1 us                                                                                                           | 45.5 us: 1.06x faster                                                                                                   |
| json_dumps           | 16.0 ms                                                                                                           | 16.8 ms: 1.05x slower                                                                                                   |
| unpickle             | 19.4 us                                                                                                           | 21.2 us: 1.09x slower                                                                                                   |
| xml_etree_parse      | 195 ms                                                                                                            | 230 ms: 1.18x slower                                                                                                    |
| tomli_loads          | 2.61 sec                                                                                                          | 3.13 sec: 1.20x slower                                                                                                  |
| unpickle_pure_python | 297 us                                                                                                            | 357 us: 1.20x slower                                                                                                    |
| json_loads           | 37.4 us                                                                                                           | 47.2 us: 1.26x slower                                                                                                   |
| xml_etree_process    | 79.4 ms                                                                                                           | 101 ms: 1.27x slower                                                                                                    |
| xml_etree_generate   | 112 ms                                                                                                            | 147 ms: 1.31x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle_list, pickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 28.0 ms                                                                                                           | 31.6 ms: 1.13x slower                                                                                                   |
| python_startup_no_site | 16.0 ms                                                                                                           | 19.6 ms: 1.23x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 51.1 ms                                                                                                           | 56.1 ms: 1.10x slower                                                                                                   |
| genshi_xml      | 71.9 ms                                                                                                           | 87.5 ms: 1.22x slower                                                                                                   |
| genshi_text     | 29.1 ms                                                                                                           | 38.3 ms: 1.32x slower                                                                                                   |
| mako            | 16.6 ms                                                                                                           | 23.5 ms: 1.42x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.26x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 8.19 ms                                                                                                           | 3.76 ms: 2.18x faster                                                                                                   |
| create_gc_cycles           | 3.68 ms                                                                                                           | 3.04 ms: 1.21x faster                                                                                                   |
| async_tree_io_tg           | 909 ms                                                                                                            | 801 ms: 1.13x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 732 ms                                                                                                            | 648 ms: 1.13x faster                                                                                                    |
| bench_mp_pool              | 96.1 ms                                                                                                           | 85.5 ms: 1.12x faster                                                                                                   |
| pickle_list                | 7.83 us                                                                                                           | 7.27 us: 1.08x faster                                                                                                   |
| async_tree_io              | 890 ms                                                                                                            | 838 ms: 1.06x faster                                                                                                    |
| pickle_dict                | 48.1 us                                                                                                           | 45.5 us: 1.06x faster                                                                                                   |
| regex_effbot               | 4.29 ms                                                                                                           | 4.48 ms: 1.04x slower                                                                                                   |
| async_tree_none            | 386 ms                                                                                                            | 406 ms: 1.05x slower                                                                                                    |
| json_dumps                 | 16.0 ms                                                                                                           | 16.8 ms: 1.05x slower                                                                                                   |
| async_generators           | 535 ms                                                                                                            | 564 ms: 1.05x slower                                                                                                    |
| json                       | 7.47 ms                                                                                                           | 8.00 ms: 1.07x slower                                                                                                   |
| pyflate                    | 698 ms                                                                                                            | 750 ms: 1.07x slower                                                                                                    |
| deepcopy_reduce            | 4.07 us                                                                                                           | 4.38 us: 1.08x slower                                                                                                   |
| coverage                   | 132 ms                                                                                                            | 143 ms: 1.08x slower                                                                                                    |
| deepcopy                   | 373 us                                                                                                            | 403 us: 1.08x slower                                                                                                    |
| pathlib                    | 30.2 ms                                                                                                           | 32.6 ms: 1.08x slower                                                                                                   |
| async_tree_memoization_tg  | 467 ms                                                                                                            | 506 ms: 1.08x slower                                                                                                    |
| unpickle                   | 19.4 us                                                                                                           | 21.2 us: 1.09x slower                                                                                                   |
| django_template            | 51.1 ms                                                                                                           | 56.1 ms: 1.10x slower                                                                                                   |
| k_core                     | 4.07 sec                                                                                                          | 4.47 sec: 1.10x slower                                                                                                  |
| connected_components       | 841 ms                                                                                                            | 927 ms: 1.10x slower                                                                                                    |
| coroutines                 | 31.0 ms                                                                                                           | 34.3 ms: 1.11x slower                                                                                                   |
| generators                 | 39.7 ms                                                                                                           | 44.0 ms: 1.11x slower                                                                                                   |
| sphinx                     | 1.54 sec                                                                                                          | 1.70 sec: 1.11x slower                                                                                                  |
| scimark_lu                 | 160 ms                                                                                                            | 180 ms: 1.12x slower                                                                                                    |
| python_startup             | 28.0 ms                                                                                                           | 31.6 ms: 1.13x slower                                                                                                   |
| asyncio_websockets         | 724 ms                                                                                                            | 817 ms: 1.13x slower                                                                                                    |
| telco                      | 10.5 ms                                                                                                           | 12.0 ms: 1.14x slower                                                                                                   |
| docutils                   | 3.54 sec                                                                                                          | 4.07 sec: 1.15x slower                                                                                                  |
| many_optionals             | 1.11 ms                                                                                                           | 1.27 ms: 1.15x slower                                                                                                   |
| mdp                        | 3.66 sec                                                                                                          | 4.21 sec: 1.15x slower                                                                                                  |
| shortest_path              | 896 ms                                                                                                            | 1.03 sec: 1.15x slower                                                                                                  |
| sqlite_synth               | 3.53 us                                                                                                           | 4.06 us: 1.15x slower                                                                                                   |
| regex_dna                  | 268 ms                                                                                                            | 310 ms: 1.15x slower                                                                                                    |
| pprint_safe_repr           | 930 ms                                                                                                            | 1.08 sec: 1.16x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 682 ms                                                                                                            | 795 ms: 1.17x slower                                                                                                    |
| go                         | 160 ms                                                                                                            | 187 ms: 1.17x slower                                                                                                    |
| logging_silent             | 135 ns                                                                                                            | 158 ns: 1.17x slower                                                                                                    |
| html5lib                   | 84.0 ms                                                                                                           | 98.6 ms: 1.17x slower                                                                                                   |
| scimark_fft                | 455 ms                                                                                                            | 536 ms: 1.18x slower                                                                                                    |
| xml_etree_parse            | 195 ms                                                                                                            | 230 ms: 1.18x slower                                                                                                    |
| pylint                     | 411 ms                                                                                                            | 490 ms: 1.19x slower                                                                                                    |
| tomli_loads                | 2.61 sec                                                                                                          | 3.13 sec: 1.20x slower                                                                                                  |
| unpickle_pure_python       | 297 us                                                                                                            | 357 us: 1.20x slower                                                                                                    |
| meteor_contest             | 152 ms                                                                                                            | 183 ms: 1.20x slower                                                                                                    |
| logging_simple             | 7.68 us                                                                                                           | 9.29 us: 1.21x slower                                                                                                   |
| richards                   | 63.2 ms                                                                                                           | 76.4 ms: 1.21x slower                                                                                                   |
| genshi_xml                 | 71.9 ms                                                                                                           | 87.5 ms: 1.22x slower                                                                                                   |
| richards_super             | 71.2 ms                                                                                                           | 86.8 ms: 1.22x slower                                                                                                   |
| 2to3                       | 461 ms                                                                                                            | 562 ms: 1.22x slower                                                                                                    |
| python_startup_no_site     | 16.0 ms                                                                                                           | 19.6 ms: 1.23x slower                                                                                                   |
| sqlglot_transpile          | 2.36 ms                                                                                                           | 2.90 ms: 1.23x slower                                                                                                   |
| spectral_norm              | 128 ms                                                                                                            | 158 ms: 1.23x slower                                                                                                    |
| hexiom                     | 8.73 ms                                                                                                           | 10.8 ms: 1.23x slower                                                                                                   |
| sqlglot_normalize          | 140 ms                                                                                                            | 173 ms: 1.24x slower                                                                                                    |
| nqueens                    | 110 ms                                                                                                            | 136 ms: 1.24x slower                                                                                                    |
| pprint_pformat             | 1.86 sec                                                                                                          | 2.32 sec: 1.24x slower                                                                                                  |
| asyncio_tcp                | 966 ms                                                                                                            | 1.21 sec: 1.25x slower                                                                                                  |
| sqlalchemy_imperative      | 24.6 ms                                                                                                           | 30.8 ms: 1.25x slower                                                                                                   |
| sympy_expand               | 587 ms                                                                                                            | 741 ms: 1.26x slower                                                                                                    |
| json_loads                 | 37.4 us                                                                                                           | 47.2 us: 1.26x slower                                                                                                   |
| asyncio_tcp_ssl            | 2.77 sec                                                                                                          | 3.50 sec: 1.26x slower                                                                                                  |
| fannkuch                   | 521 ms                                                                                                            | 660 ms: 1.27x slower                                                                                                    |
| xml_etree_process          | 79.4 ms                                                                                                           | 101 ms: 1.27x slower                                                                                                    |
| thrift                     | 1.13 ms                                                                                                           | 1.45 ms: 1.28x slower                                                                                                   |
| subparsers                 | 33.0 ms                                                                                                           | 42.3 ms: 1.28x slower                                                                                                   |
| regex_compile              | 164 ms                                                                                                            | 211 ms: 1.29x slower                                                                                                    |
| sympy_integrate            | 27.9 ms                                                                                                           | 36.2 ms: 1.30x slower                                                                                                   |
| scimark_monte_carlo        | 84.6 ms                                                                                                           | 110 ms: 1.30x slower                                                                                                    |
| scimark_sor                | 151 ms                                                                                                            | 198 ms: 1.31x slower                                                                                                    |
| bpe_tokeniser              | 5.78 sec                                                                                                          | 7.57 sec: 1.31x slower                                                                                                  |
| xml_etree_generate         | 112 ms                                                                                                            | 147 ms: 1.31x slower                                                                                                    |
| genshi_text                | 29.1 ms                                                                                                           | 38.3 ms: 1.32x slower                                                                                                   |
| sqlalchemy_declarative     | 178 ms                                                                                                            | 235 ms: 1.32x slower                                                                                                    |
| typing_runtime_protocols   | 211 us                                                                                                            | 280 us: 1.32x slower                                                                                                    |
| sympy_str                  | 364 ms                                                                                                            | 483 ms: 1.33x slower                                                                                                    |
| comprehensions             | 21.4 us                                                                                                           | 28.6 us: 1.34x slower                                                                                                   |
| scimark_sparse_mat_mult    | 6.10 ms                                                                                                           | 8.26 ms: 1.35x slower                                                                                                   |
| chaos                      | 79.5 ms                                                                                                           | 108 ms: 1.36x slower                                                                                                    |
| sqlglot_optimize           | 71.4 ms                                                                                                           | 97.0 ms: 1.36x slower                                                                                                   |
| crypto_pyaes               | 92.8 ms                                                                                                           | 128 ms: 1.38x slower                                                                                                    |
| mako                       | 16.6 ms                                                                                                           | 23.5 ms: 1.42x slower                                                                                                   |
| logging_format             | 8.87 us                                                                                                           | 12.6 us: 1.42x slower                                                                                                   |
| raytrace                   | 339 ms                                                                                                            | 480 ms: 1.42x slower                                                                                                    |
| bench_thread_pool          | 3.14 ms                                                                                                           | 4.49 ms: 1.43x slower                                                                                                   |
| sqlglot_parse              | 1.72 ms                                                                                                           | 2.55 ms: 1.48x slower                                                                                                   |
| deepcopy_memo              | 38.8 us                                                                                                           | 58.3 us: 1.50x slower                                                                                                   |
| deltablue                  | 4.62 ms                                                                                                           | 7.02 ms: 1.52x slower                                                                                                   |
| nbody                      | 126 ms                                                                                                            | 194 ms: 1.54x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (13): unpack_sequence, xml_etree_iterparse, async_tree_none_tg, async_tree_memoization, regex_v8, pidigits, float, unpickle_list, pickle, sympy_sum, pickle_pure_python, pycparser, dulwich_log

- Geometric mean (including insignificant results): 1.133x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.19x