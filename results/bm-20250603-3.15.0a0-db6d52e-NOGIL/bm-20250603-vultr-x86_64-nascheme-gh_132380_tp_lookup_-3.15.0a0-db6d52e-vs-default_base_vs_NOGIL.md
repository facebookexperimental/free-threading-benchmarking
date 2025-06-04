# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_132380_tp_lookup_
- machine: linux-x86_64
- commit hash: db6d52e
- commit date: 2025-06-03
- overall geometric mean: 1.088x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                | 281 ms: 1.13x slower                                                    |
| docutils       | 2.50 sec                                                              | 2.68 sec: 1.07x slower                                                  |
| html5lib       | 61.2 ms                                                               | 65.3 ms: 1.07x slower                                                   |
| sphinx         | 964 ms                                                                | 1.05 sec: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                | 524 ms: 1.20x faster                                                    |
| async_tree_none_tg         | 253 ms                                                                | 227 ms: 1.11x faster                                                    |
| async_tree_io              | 595 ms                                                                | 549 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed_tg | 515 ms                                                                | 475 ms: 1.08x faster                                                    |
| async_tree_memoization_tg  | 307 ms                                                                | 284 ms: 1.08x faster                                                    |
| async_tree_none            | 270 ms                                                                | 255 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed    | 523 ms                                                                | 503 ms: 1.04x faster                                                    |
| coroutines                 | 23.6 ms                                                               | 23.5 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                                | 515 ms: 1.00x faster                                                    |
| async_generators           | 337 ms                                                                | 373 ms: 1.11x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.8 ms                                                               | 69.6 ms: 1.03x faster                                                   |
| pidigits       | 199 ms                                                                | 215 ms: 1.08x slower                                                    |
| nbody          | 89.2 ms                                                               | 121 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 172 ms                                                                | 164 ms: 1.05x faster                                                    |
| regex_v8       | 20.4 ms                                                               | 20.5 ms: 1.01x slower                                                   |
| regex_compile  | 123 ms                                                                | 143 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.9 ms                                                               | 87.9 ms: 1.05x faster                                                   |
| xml_etree_parse      | 131 ms                                                                | 130 ms: 1.01x faster                                                    |
| json_loads           | 28.5 us                                                               | 30.7 us: 1.08x slower                                                   |
| unpickle_pure_python | 209 us                                                                | 230 us: 1.10x slower                                                    |
| pickle_pure_python   | 305 us                                                                | 337 us: 1.10x slower                                                    |
| tomli_loads          | 1.93 sec                                                              | 2.13 sec: 1.11x slower                                                  |
| json_dumps           | 10.8 ms                                                               | 12.0 ms: 1.11x slower                                                   |
| xml_etree_generate   | 82.0 ms                                                               | 94.6 ms: 1.15x slower                                                   |
| xml_etree_process    | 57.8 ms                                                               | 68.3 ms: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.09x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                               | 16.1 ms: 1.27x slower                                                   |
| python_startup_no_site | 7.33 ms                                                               | 9.61 ms: 1.31x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.29x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.7 ms                                                               | 39.2 ms: 1.13x slower                                                   |
| genshi_xml      | 48.9 ms                                                               | 57.4 ms: 1.17x slower                                                   |
| genshi_text     | 20.8 ms                                                               | 26.2 ms: 1.26x slower                                                   |
| mako            | 11.8 ms                                                               | 15.7 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal               | 4.30 ms                                                               | 1.92 ms: 2.24x faster                                                   |
| create_gc_cycles           | 1.91 ms                                                               | 1.49 ms: 1.29x faster                                                   |
| async_tree_io_tg           | 628 ms                                                                | 524 ms: 1.20x faster                                                    |
| async_tree_none_tg         | 253 ms                                                                | 227 ms: 1.11x faster                                                    |
| sqlite_synth               | 2.22 us                                                               | 2.03 us: 1.10x faster                                                   |
| async_tree_io              | 595 ms                                                                | 549 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed_tg | 515 ms                                                                | 475 ms: 1.08x faster                                                    |
| async_tree_memoization_tg  | 307 ms                                                                | 284 ms: 1.08x faster                                                    |
| async_tree_none            | 270 ms                                                                | 255 ms: 1.06x faster                                                    |
| regex_dna                  | 172 ms                                                                | 164 ms: 1.05x faster                                                    |
| xml_etree_iterparse        | 91.9 ms                                                               | 87.9 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed    | 523 ms                                                                | 503 ms: 1.04x faster                                                    |
| float                      | 71.8 ms                                                               | 69.6 ms: 1.03x faster                                                   |
| xml_etree_parse            | 131 ms                                                                | 130 ms: 1.01x faster                                                    |
| coroutines                 | 23.6 ms                                                               | 23.5 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                                | 515 ms: 1.00x faster                                                    |
| regex_v8                   | 20.4 ms                                                               | 20.5 ms: 1.01x slower                                                   |
| pathlib                    | 19.3 ms                                                               | 19.6 ms: 1.02x slower                                                   |
| pycparser                  | 1.09 sec                                                              | 1.13 sec: 1.03x slower                                                  |
| json                       | 5.13 ms                                                               | 5.33 ms: 1.04x slower                                                   |
| bpe_tokeniser              | 4.19 sec                                                              | 4.38 sec: 1.04x slower                                                  |
| bench_mp_pool              | 98.8 ms                                                               | 103 ms: 1.04x slower                                                    |
| scimark_fft                | 340 ms                                                                | 360 ms: 1.06x slower                                                    |
| html5lib                   | 61.2 ms                                                               | 65.3 ms: 1.07x slower                                                   |
| dulwich_log                | 66.6 ms                                                               | 71.1 ms: 1.07x slower                                                   |
| generators                 | 28.0 ms                                                               | 29.9 ms: 1.07x slower                                                   |
| docutils                   | 2.50 sec                                                              | 2.68 sec: 1.07x slower                                                  |
| json_loads                 | 28.5 us                                                               | 30.7 us: 1.08x slower                                                   |
| pidigits                   | 199 ms                                                                | 215 ms: 1.08x slower                                                    |
| many_optionals             | 1.04 ms                                                               | 1.13 ms: 1.09x slower                                                   |
| sphinx                     | 964 ms                                                                | 1.05 sec: 1.09x slower                                                  |
| scimark_sparse_mat_mult    | 4.80 ms                                                               | 5.26 ms: 1.09x slower                                                   |
| deltablue                  | 3.24 ms                                                               | 3.56 ms: 1.10x slower                                                   |
| unpickle_pure_python       | 209 us                                                                | 230 us: 1.10x slower                                                    |
| pylint                     | 278 ms                                                                | 306 ms: 1.10x slower                                                    |
| k_core                     | 2.02 sec                                                              | 2.23 sec: 1.10x slower                                                  |
| pickle_pure_python         | 305 us                                                                | 337 us: 1.10x slower                                                    |
| tomli_loads                | 1.93 sec                                                              | 2.13 sec: 1.11x slower                                                  |
| async_generators           | 337 ms                                                                | 373 ms: 1.11x slower                                                    |
| json_dumps                 | 10.8 ms                                                               | 12.0 ms: 1.11x slower                                                   |
| chaos                      | 56.4 ms                                                               | 62.9 ms: 1.12x slower                                                   |
| subparsers                 | 25.0 ms                                                               | 27.9 ms: 1.12x slower                                                   |
| logging_silent             | 470 ns                                                                | 526 ns: 1.12x slower                                                    |
| hexiom                     | 5.62 ms                                                               | 6.30 ms: 1.12x slower                                                   |
| spectral_norm              | 101 ms                                                                | 113 ms: 1.12x slower                                                    |
| mdp                        | 1.16 sec                                                              | 1.31 sec: 1.13x slower                                                  |
| scimark_sor                | 110 ms                                                                | 124 ms: 1.13x slower                                                    |
| pprint_safe_repr           | 778 ms                                                                | 880 ms: 1.13x slower                                                    |
| 2to3                       | 248 ms                                                                | 281 ms: 1.13x slower                                                    |
| django_template            | 34.7 ms                                                               | 39.2 ms: 1.13x slower                                                   |
| comprehensions             | 15.5 us                                                               | 17.6 us: 1.14x slower                                                   |
| pprint_pformat             | 1.59 sec                                                              | 1.81 sec: 1.14x slower                                                  |
| sqlglot_v2_optimize        | 49.3 ms                                                               | 56.4 ms: 1.14x slower                                                   |
| deepcopy_reduce            | 2.60 us                                                               | 2.97 us: 1.14x slower                                                   |
| nqueens                    | 75.5 ms                                                               | 86.7 ms: 1.15x slower                                                   |
| xml_etree_generate         | 82.0 ms                                                               | 94.6 ms: 1.15x slower                                                   |
| go                         | 105 ms                                                                | 121 ms: 1.16x slower                                                    |
| sqlglot_v2_normalize       | 98.0 ms                                                               | 113 ms: 1.16x slower                                                    |
| regex_compile              | 123 ms                                                                | 143 ms: 1.16x slower                                                    |
| sympy_expand               | 446 ms                                                                | 518 ms: 1.16x slower                                                    |
| sympy_sum                  | 153 ms                                                                | 177 ms: 1.16x slower                                                    |
| scimark_lu                 | 110 ms                                                                | 128 ms: 1.17x slower                                                    |
| deepcopy                   | 248 us                                                                | 289 us: 1.17x slower                                                    |
| raytrace                   | 253 ms                                                                | 296 ms: 1.17x slower                                                    |
| sympy_integrate            | 18.7 ms                                                               | 21.8 ms: 1.17x slower                                                   |
| sympy_str                  | 266 ms                                                                | 312 ms: 1.17x slower                                                    |
| genshi_xml                 | 48.9 ms                                                               | 57.4 ms: 1.17x slower                                                   |
| logging_simple             | 6.49 us                                                               | 7.64 us: 1.18x slower                                                   |
| sqlglot_v2_transpile       | 1.51 ms                                                               | 1.78 ms: 1.18x slower                                                   |
| thrift                     | 736 us                                                                | 869 us: 1.18x slower                                                    |
| xml_etree_process          | 57.8 ms                                                               | 68.3 ms: 1.18x slower                                                   |
| logging_format             | 7.29 us                                                               | 8.68 us: 1.19x slower                                                   |
| telco                      | 7.25 ms                                                               | 8.63 ms: 1.19x slower                                                   |
| pyflate                    | 399 ms                                                                | 477 ms: 1.20x slower                                                    |
| sqlglot_v2_parse           | 1.21 ms                                                               | 1.46 ms: 1.20x slower                                                   |
| meteor_contest             | 98.7 ms                                                               | 120 ms: 1.22x slower                                                    |
| connected_components       | 394 ms                                                                | 480 ms: 1.22x slower                                                    |
| fannkuch                   | 381 ms                                                                | 466 ms: 1.22x slower                                                    |
| deepcopy_memo              | 28.6 us                                                               | 35.0 us: 1.22x slower                                                   |
| shortest_path              | 435 ms                                                                | 535 ms: 1.23x slower                                                    |
| typing_runtime_protocols   | 151 us                                                                | 188 us: 1.24x slower                                                    |
| richards                   | 41.1 ms                                                               | 51.2 ms: 1.25x slower                                                   |
| genshi_text                | 20.8 ms                                                               | 26.2 ms: 1.26x slower                                                   |
| richards_super             | 46.5 ms                                                               | 58.7 ms: 1.26x slower                                                   |
| scimark_monte_carlo        | 60.8 ms                                                               | 77.3 ms: 1.27x slower                                                   |
| python_startup             | 12.6 ms                                                               | 16.1 ms: 1.27x slower                                                   |
| crypto_pyaes               | 67.1 ms                                                               | 85.8 ms: 1.28x slower                                                   |
| python_startup_no_site     | 7.33 ms                                                               | 9.61 ms: 1.31x slower                                                   |
| mako                       | 11.8 ms                                                               | 15.7 ms: 1.33x slower                                                   |
| nbody                      | 89.2 ms                                                               | 121 ms: 1.35x slower                                                    |
| coverage                   | 81.4 ms                                                               | 112 ms: 1.38x slower                                                    |
| bench_thread_pool          | 1.04 ms                                                               | 3.11 ms: 2.98x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.11x slower                                                            |

Benchmark hidden because not significant (2): async_tree_memoization, regex_effbot

- Geometric mean (including insignificant results): 1.088x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.22x