# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_132380_tp_getattr
- machine: linux-x86_64
- commit hash: 04ccde3
- commit date: 2025-06-05
- overall geometric mean: 1.087x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                | 281 ms: 1.13x slower                                                    |
| docutils       | 2.53 sec                                                              | 2.65 sec: 1.05x slower                                                  |
| html5lib       | 60.9 ms                                                               | 66.4 ms: 1.09x slower                                                   |
| sphinx         | 976 ms                                                                | 1.06 sec: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 618 ms                                                                | 519 ms: 1.19x faster                                                    |
| async_tree_none_tg         | 249 ms                                                                | 227 ms: 1.09x faster                                                    |
| async_tree_io              | 593 ms                                                                | 549 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                | 471 ms: 1.08x faster                                                    |
| async_tree_memoization_tg  | 307 ms                                                                | 285 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed    | 518 ms                                                                | 499 ms: 1.04x faster                                                    |
| async_tree_none            | 265 ms                                                                | 260 ms: 1.02x faster                                                    |
| coroutines                 | 23.8 ms                                                               | 24.0 ms: 1.01x slower                                                   |
| async_tree_memoization     | 310 ms                                                                | 315 ms: 1.02x slower                                                    |
| async_generators           | 332 ms                                                                | 365 ms: 1.10x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.04x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 195 ms                                                                | 189 ms: 1.03x faster                                                    |
| float          | 70.8 ms                                                               | 69.7 ms: 1.01x faster                                                   |
| nbody          | 86.4 ms                                                               | 121 ms: 1.40x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.10x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 2.92 ms                                                               | 2.63 ms: 1.11x faster                                                   |
| regex_v8       | 22.7 ms                                                               | 20.7 ms: 1.09x faster                                                   |
| regex_dna      | 176 ms                                                                | 170 ms: 1.04x faster                                                    |
| regex_compile  | 124 ms                                                                | 143 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.8 ms                                                               | 87.5 ms: 1.05x faster                                                   |
| pickle_pure_python   | 306 us                                                                | 334 us: 1.09x slower                                                    |
| unpickle_pure_python | 210 us                                                                | 231 us: 1.10x slower                                                    |
| json_loads           | 28.2 us                                                               | 31.2 us: 1.11x slower                                                   |
| json_dumps           | 10.8 ms                                                               | 12.1 ms: 1.12x slower                                                   |
| tomli_loads          | 1.90 sec                                                              | 2.16 sec: 1.14x slower                                                  |
| xml_etree_generate   | 82.7 ms                                                               | 95.5 ms: 1.16x slower                                                   |
| xml_etree_process    | 58.2 ms                                                               | 68.8 ms: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.09x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                               | 15.9 ms: 1.27x slower                                                   |
| python_startup_no_site | 7.28 ms                                                               | 9.54 ms: 1.31x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.29x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.6 ms                                                               | 40.6 ms: 1.17x slower                                                   |
| genshi_xml      | 48.1 ms                                                               | 58.4 ms: 1.21x slower                                                   |
| genshi_text     | 20.3 ms                                                               | 26.5 ms: 1.30x slower                                                   |
| mako            | 11.8 ms                                                               | 15.6 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.25x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal               | 4.37 ms                                                               | 1.89 ms: 2.31x faster                                                   |
| create_gc_cycles           | 1.91 ms                                                               | 1.46 ms: 1.31x faster                                                   |
| async_tree_io_tg           | 618 ms                                                                | 519 ms: 1.19x faster                                                    |
| regex_effbot               | 2.92 ms                                                               | 2.63 ms: 1.11x faster                                                   |
| async_tree_none_tg         | 249 ms                                                                | 227 ms: 1.09x faster                                                    |
| regex_v8                   | 22.7 ms                                                               | 20.7 ms: 1.09x faster                                                   |
| sqlite_synth               | 2.23 us                                                               | 2.04 us: 1.09x faster                                                   |
| async_tree_io              | 593 ms                                                                | 549 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                | 471 ms: 1.08x faster                                                    |
| async_tree_memoization_tg  | 307 ms                                                                | 285 ms: 1.08x faster                                                    |
| xml_etree_iterparse        | 91.8 ms                                                               | 87.5 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed    | 518 ms                                                                | 499 ms: 1.04x faster                                                    |
| regex_dna                  | 176 ms                                                                | 170 ms: 1.04x faster                                                    |
| pidigits                   | 195 ms                                                                | 189 ms: 1.03x faster                                                    |
| async_tree_none            | 265 ms                                                                | 260 ms: 1.02x faster                                                    |
| float                      | 70.8 ms                                                               | 69.7 ms: 1.01x faster                                                   |
| pathlib                    | 19.3 ms                                                               | 19.4 ms: 1.01x slower                                                   |
| coroutines                 | 23.8 ms                                                               | 24.0 ms: 1.01x slower                                                   |
| async_tree_memoization     | 310 ms                                                                | 315 ms: 1.02x slower                                                    |
| json                       | 5.09 ms                                                               | 5.29 ms: 1.04x slower                                                   |
| bench_mp_pool              | 98.0 ms                                                               | 102 ms: 1.04x slower                                                    |
| docutils                   | 2.53 sec                                                              | 2.65 sec: 1.05x slower                                                  |
| bpe_tokeniser              | 4.15 sec                                                              | 4.36 sec: 1.05x slower                                                  |
| dulwich_log                | 66.2 ms                                                               | 70.9 ms: 1.07x slower                                                   |
| deltablue                  | 3.31 ms                                                               | 3.59 ms: 1.08x slower                                                   |
| many_optionals             | 1.03 ms                                                               | 1.12 ms: 1.08x slower                                                   |
| sphinx                     | 976 ms                                                                | 1.06 sec: 1.08x slower                                                  |
| html5lib                   | 60.9 ms                                                               | 66.4 ms: 1.09x slower                                                   |
| pickle_pure_python         | 306 us                                                                | 334 us: 1.09x slower                                                    |
| pylint                     | 277 ms                                                                | 304 ms: 1.09x slower                                                    |
| scimark_sor                | 112 ms                                                                | 123 ms: 1.10x slower                                                    |
| k_core                     | 2.04 sec                                                              | 2.24 sec: 1.10x slower                                                  |
| comprehensions             | 15.8 us                                                               | 17.4 us: 1.10x slower                                                   |
| subparsers                 | 25.1 ms                                                               | 27.6 ms: 1.10x slower                                                   |
| async_generators           | 332 ms                                                                | 365 ms: 1.10x slower                                                    |
| unpickle_pure_python       | 210 us                                                                | 231 us: 1.10x slower                                                    |
| hexiom                     | 5.74 ms                                                               | 6.35 ms: 1.11x slower                                                   |
| json_loads                 | 28.2 us                                                               | 31.2 us: 1.11x slower                                                   |
| pprint_safe_repr           | 777 ms                                                                | 866 ms: 1.11x slower                                                    |
| json_dumps                 | 10.8 ms                                                               | 12.1 ms: 1.12x slower                                                   |
| chaos                      | 56.1 ms                                                               | 62.9 ms: 1.12x slower                                                   |
| logging_silent             | 469 ns                                                                | 528 ns: 1.12x slower                                                    |
| pprint_pformat             | 1.59 sec                                                              | 1.79 sec: 1.13x slower                                                  |
| 2to3                       | 249 ms                                                                | 281 ms: 1.13x slower                                                    |
| nqueens                    | 75.8 ms                                                               | 85.4 ms: 1.13x slower                                                   |
| scimark_fft                | 327 ms                                                                | 370 ms: 1.13x slower                                                    |
| deepcopy_reduce            | 2.65 us                                                               | 3.00 us: 1.13x slower                                                   |
| tomli_loads                | 1.90 sec                                                              | 2.16 sec: 1.14x slower                                                  |
| generators                 | 27.7 ms                                                               | 31.6 ms: 1.14x slower                                                   |
| go                         | 106 ms                                                                | 121 ms: 1.14x slower                                                    |
| spectral_norm              | 99.3 ms                                                               | 114 ms: 1.14x slower                                                    |
| pyflate                    | 407 ms                                                                | 466 ms: 1.14x slower                                                    |
| mdp                        | 1.14 sec                                                              | 1.32 sec: 1.15x slower                                                  |
| deepcopy                   | 253 us                                                                | 291 us: 1.15x slower                                                    |
| regex_compile              | 124 ms                                                                | 143 ms: 1.15x slower                                                    |
| thrift                     | 752 us                                                                | 868 us: 1.15x slower                                                    |
| xml_etree_generate         | 82.7 ms                                                               | 95.5 ms: 1.16x slower                                                   |
| sqlglot_v2_optimize        | 49.6 ms                                                               | 57.3 ms: 1.16x slower                                                   |
| sqlglot_v2_normalize       | 98.1 ms                                                               | 114 ms: 1.16x slower                                                    |
| sympy_integrate            | 18.7 ms                                                               | 21.9 ms: 1.17x slower                                                   |
| django_template            | 34.6 ms                                                               | 40.6 ms: 1.17x slower                                                   |
| raytrace                   | 251 ms                                                                | 294 ms: 1.17x slower                                                    |
| logging_simple             | 6.48 us                                                               | 7.63 us: 1.18x slower                                                   |
| telco                      | 7.27 ms                                                               | 8.56 ms: 1.18x slower                                                   |
| sympy_sum                  | 152 ms                                                                | 180 ms: 1.18x slower                                                    |
| fannkuch                   | 387 ms                                                                | 457 ms: 1.18x slower                                                    |
| xml_etree_process          | 58.2 ms                                                               | 68.8 ms: 1.18x slower                                                   |
| sqlglot_v2_transpile       | 1.49 ms                                                               | 1.77 ms: 1.18x slower                                                   |
| scimark_lu                 | 111 ms                                                                | 131 ms: 1.18x slower                                                    |
| sympy_str                  | 266 ms                                                                | 316 ms: 1.19x slower                                                    |
| sympy_expand               | 447 ms                                                                | 531 ms: 1.19x slower                                                    |
| deepcopy_memo              | 29.1 us                                                               | 34.7 us: 1.19x slower                                                   |
| logging_format             | 7.28 us                                                               | 8.69 us: 1.19x slower                                                   |
| meteor_contest             | 100 ms                                                                | 120 ms: 1.19x slower                                                    |
| scimark_sparse_mat_mult    | 4.64 ms                                                               | 5.56 ms: 1.20x slower                                                   |
| genshi_xml                 | 48.1 ms                                                               | 58.4 ms: 1.21x slower                                                   |
| sqlglot_v2_parse           | 1.20 ms                                                               | 1.46 ms: 1.22x slower                                                   |
| shortest_path              | 438 ms                                                                | 537 ms: 1.23x slower                                                    |
| richards                   | 41.6 ms                                                               | 51.0 ms: 1.23x slower                                                   |
| typing_runtime_protocols   | 151 us                                                                | 187 us: 1.24x slower                                                    |
| connected_components       | 395 ms                                                                | 489 ms: 1.24x slower                                                    |
| scimark_monte_carlo        | 61.6 ms                                                               | 76.9 ms: 1.25x slower                                                   |
| richards_super             | 46.8 ms                                                               | 58.7 ms: 1.25x slower                                                   |
| python_startup             | 12.5 ms                                                               | 15.9 ms: 1.27x slower                                                   |
| crypto_pyaes               | 67.0 ms                                                               | 85.8 ms: 1.28x slower                                                   |
| genshi_text                | 20.3 ms                                                               | 26.5 ms: 1.30x slower                                                   |
| python_startup_no_site     | 7.28 ms                                                               | 9.54 ms: 1.31x slower                                                   |
| mako                       | 11.8 ms                                                               | 15.6 ms: 1.32x slower                                                   |
| coverage                   | 81.5 ms                                                               | 112 ms: 1.37x slower                                                    |
| nbody                      | 86.4 ms                                                               | 121 ms: 1.40x slower                                                    |
| bench_thread_pool          | 1.04 ms                                                               | 3.10 ms: 2.98x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.11x slower                                                            |

Benchmark hidden because not significant (3): pycparser, xml_etree_parse, asyncio_websockets

- Geometric mean (including insignificant results): 1.087x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.22x