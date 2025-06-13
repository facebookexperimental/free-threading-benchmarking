# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_133136_qsbr_defer
- machine: linux-x86_64
- commit hash: 3978e35
- commit date: 2025-06-12
- overall geometric mean: 1.088x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                | 282 ms: 1.13x slower                                                    |
| docutils       | 2.50 sec                                                              | 2.67 sec: 1.07x slower                                                  |
| html5lib       | 61.2 ms                                                               | 65.8 ms: 1.08x slower                                                   |
| sphinx         | 964 ms                                                                | 1.06 sec: 1.10x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                | 522 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg | 515 ms                                                                | 472 ms: 1.09x faster                                                    |
| async_tree_io              | 595 ms                                                                | 550 ms: 1.08x faster                                                    |
| async_tree_memoization_tg  | 307 ms                                                                | 285 ms: 1.08x faster                                                    |
| async_tree_none_tg         | 253 ms                                                                | 237 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed    | 523 ms                                                                | 497 ms: 1.05x faster                                                    |
| async_tree_none            | 270 ms                                                                | 257 ms: 1.05x faster                                                    |
| asyncio_websockets         | 517 ms                                                                | 511 ms: 1.01x faster                                                    |
| coroutines                 | 23.6 ms                                                               | 23.4 ms: 1.01x faster                                                   |
| async_tree_memoization     | 309 ms                                                                | 312 ms: 1.01x slower                                                    |
| async_generators           | 337 ms                                                                | 368 ms: 1.09x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 199 ms                                                                | 184 ms: 1.08x faster                                                    |
| float          | 71.8 ms                                                               | 69.4 ms: 1.04x faster                                                   |
| nbody          | 89.2 ms                                                               | 121 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 172 ms                                                                | 167 ms: 1.03x faster                                                    |
| regex_v8       | 20.4 ms                                                               | 20.6 ms: 1.01x slower                                                   |
| regex_effbot   | 2.63 ms                                                               | 2.73 ms: 1.04x slower                                                   |
| regex_compile  | 123 ms                                                                | 143 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.9 ms                                                               | 86.3 ms: 1.06x faster                                                   |
| xml_etree_parse      | 131 ms                                                                | 130 ms: 1.01x faster                                                    |
| pickle_pure_python   | 305 us                                                                | 335 us: 1.10x slower                                                    |
| json_dumps           | 10.8 ms                                                               | 11.9 ms: 1.10x slower                                                   |
| unpickle_pure_python | 209 us                                                                | 231 us: 1.10x slower                                                    |
| tomli_loads          | 1.93 sec                                                              | 2.16 sec: 1.12x slower                                                  |
| json_loads           | 28.5 us                                                               | 31.8 us: 1.12x slower                                                   |
| xml_etree_generate   | 82.0 ms                                                               | 94.5 ms: 1.15x slower                                                   |
| xml_etree_process    | 57.8 ms                                                               | 68.4 ms: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.09x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                               | 16.0 ms: 1.27x slower                                                   |
| python_startup_no_site | 7.33 ms                                                               | 9.61 ms: 1.31x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.29x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.7 ms                                                               | 39.0 ms: 1.13x slower                                                   |
| genshi_xml      | 48.9 ms                                                               | 55.6 ms: 1.14x slower                                                   |
| genshi_text     | 20.8 ms                                                               | 25.8 ms: 1.24x slower                                                   |
| mako            | 11.8 ms                                                               | 15.9 ms: 1.35x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal               | 4.30 ms                                                               | 1.93 ms: 2.23x faster                                                   |
| create_gc_cycles           | 1.91 ms                                                               | 1.49 ms: 1.28x faster                                                   |
| async_tree_io_tg           | 628 ms                                                                | 522 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg | 515 ms                                                                | 472 ms: 1.09x faster                                                    |
| async_tree_io              | 595 ms                                                                | 550 ms: 1.08x faster                                                    |
| async_tree_memoization_tg  | 307 ms                                                                | 285 ms: 1.08x faster                                                    |
| sqlite_synth               | 2.22 us                                                               | 2.06 us: 1.08x faster                                                   |
| pidigits                   | 199 ms                                                                | 184 ms: 1.08x faster                                                    |
| async_tree_none_tg         | 253 ms                                                                | 237 ms: 1.07x faster                                                    |
| xml_etree_iterparse        | 91.9 ms                                                               | 86.3 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed    | 523 ms                                                                | 497 ms: 1.05x faster                                                    |
| async_tree_none            | 270 ms                                                                | 257 ms: 1.05x faster                                                    |
| float                      | 71.8 ms                                                               | 69.4 ms: 1.04x faster                                                   |
| regex_dna                  | 172 ms                                                                | 167 ms: 1.03x faster                                                    |
| asyncio_websockets         | 517 ms                                                                | 511 ms: 1.01x faster                                                    |
| coroutines                 | 23.6 ms                                                               | 23.4 ms: 1.01x faster                                                   |
| xml_etree_parse            | 131 ms                                                                | 130 ms: 1.01x faster                                                    |
| async_tree_memoization     | 309 ms                                                                | 312 ms: 1.01x slower                                                    |
| regex_v8                   | 20.4 ms                                                               | 20.6 ms: 1.01x slower                                                   |
| pycparser                  | 1.09 sec                                                              | 1.13 sec: 1.03x slower                                                  |
| regex_effbot               | 2.63 ms                                                               | 2.73 ms: 1.04x slower                                                   |
| bpe_tokeniser              | 4.19 sec                                                              | 4.36 sec: 1.04x slower                                                  |
| bench_mp_pool              | 98.8 ms                                                               | 103 ms: 1.05x slower                                                    |
| generators                 | 28.0 ms                                                               | 29.4 ms: 1.05x slower                                                   |
| json                       | 5.13 ms                                                               | 5.42 ms: 1.06x slower                                                   |
| dulwich_log                | 66.6 ms                                                               | 71.0 ms: 1.07x slower                                                   |
| docutils                   | 2.50 sec                                                              | 2.67 sec: 1.07x slower                                                  |
| html5lib                   | 61.2 ms                                                               | 65.8 ms: 1.08x slower                                                   |
| scimark_fft                | 340 ms                                                                | 366 ms: 1.08x slower                                                    |
| many_optionals             | 1.04 ms                                                               | 1.13 ms: 1.08x slower                                                   |
| async_generators           | 337 ms                                                                | 368 ms: 1.09x slower                                                    |
| pickle_pure_python         | 305 us                                                                | 335 us: 1.10x slower                                                    |
| sphinx                     | 964 ms                                                                | 1.06 sec: 1.10x slower                                                  |
| json_dumps                 | 10.8 ms                                                               | 11.9 ms: 1.10x slower                                                   |
| unpickle_pure_python       | 209 us                                                                | 231 us: 1.10x slower                                                    |
| deltablue                  | 3.24 ms                                                               | 3.59 ms: 1.11x slower                                                   |
| k_core                     | 2.02 sec                                                              | 2.23 sec: 1.11x slower                                                  |
| subparsers                 | 25.0 ms                                                               | 27.8 ms: 1.11x slower                                                   |
| pylint                     | 278 ms                                                                | 309 ms: 1.11x slower                                                    |
| logging_silent             | 470 ns                                                                | 524 ns: 1.11x slower                                                    |
| chaos                      | 56.4 ms                                                               | 63.0 ms: 1.12x slower                                                   |
| tomli_loads                | 1.93 sec                                                              | 2.16 sec: 1.12x slower                                                  |
| json_loads                 | 28.5 us                                                               | 31.8 us: 1.12x slower                                                   |
| django_template            | 34.7 ms                                                               | 39.0 ms: 1.13x slower                                                   |
| nqueens                    | 75.5 ms                                                               | 85.1 ms: 1.13x slower                                                   |
| mdp                        | 1.16 sec                                                              | 1.31 sec: 1.13x slower                                                  |
| hexiom                     | 5.62 ms                                                               | 6.34 ms: 1.13x slower                                                   |
| scimark_sparse_mat_mult    | 4.80 ms                                                               | 5.44 ms: 1.13x slower                                                   |
| pprint_safe_repr           | 778 ms                                                                | 883 ms: 1.13x slower                                                    |
| 2to3                       | 248 ms                                                                | 282 ms: 1.13x slower                                                    |
| genshi_xml                 | 48.9 ms                                                               | 55.6 ms: 1.14x slower                                                   |
| scimark_sor                | 110 ms                                                                | 125 ms: 1.14x slower                                                    |
| sqlglot_v2_optimize        | 49.3 ms                                                               | 56.2 ms: 1.14x slower                                                   |
| sqlglot_v2_normalize       | 98.0 ms                                                               | 112 ms: 1.14x slower                                                    |
| comprehensions             | 15.5 us                                                               | 17.6 us: 1.14x slower                                                   |
| deepcopy_reduce            | 2.60 us                                                               | 2.96 us: 1.14x slower                                                   |
| pprint_pformat             | 1.59 sec                                                              | 1.82 sec: 1.14x slower                                                  |
| deepcopy                   | 248 us                                                                | 286 us: 1.15x slower                                                    |
| xml_etree_generate         | 82.0 ms                                                               | 94.5 ms: 1.15x slower                                                   |
| spectral_norm              | 101 ms                                                                | 116 ms: 1.15x slower                                                    |
| regex_compile              | 123 ms                                                                | 143 ms: 1.16x slower                                                    |
| go                         | 105 ms                                                                | 122 ms: 1.16x slower                                                    |
| scimark_lu                 | 110 ms                                                                | 128 ms: 1.16x slower                                                    |
| sympy_expand               | 446 ms                                                                | 519 ms: 1.16x slower                                                    |
| sympy_sum                  | 153 ms                                                                | 178 ms: 1.17x slower                                                    |
| raytrace                   | 253 ms                                                                | 296 ms: 1.17x slower                                                    |
| sympy_str                  | 266 ms                                                                | 312 ms: 1.17x slower                                                    |
| sympy_integrate            | 18.7 ms                                                               | 21.9 ms: 1.17x slower                                                   |
| thrift                     | 736 us                                                                | 866 us: 1.18x slower                                                    |
| logging_simple             | 6.49 us                                                               | 7.64 us: 1.18x slower                                                   |
| xml_etree_process          | 57.8 ms                                                               | 68.4 ms: 1.18x slower                                                   |
| pyflate                    | 399 ms                                                                | 472 ms: 1.19x slower                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                               | 1.80 ms: 1.20x slower                                                   |
| telco                      | 7.25 ms                                                               | 8.68 ms: 1.20x slower                                                   |
| meteor_contest             | 98.7 ms                                                               | 118 ms: 1.20x slower                                                    |
| sqlglot_v2_parse           | 1.21 ms                                                               | 1.46 ms: 1.20x slower                                                   |
| logging_format             | 7.29 us                                                               | 8.76 us: 1.20x slower                                                   |
| deepcopy_memo              | 28.6 us                                                               | 34.7 us: 1.22x slower                                                   |
| fannkuch                   | 381 ms                                                                | 466 ms: 1.22x slower                                                    |
| connected_components       | 394 ms                                                                | 484 ms: 1.23x slower                                                    |
| shortest_path              | 435 ms                                                                | 534 ms: 1.23x slower                                                    |
| richards                   | 41.1 ms                                                               | 50.9 ms: 1.24x slower                                                   |
| genshi_text                | 20.8 ms                                                               | 25.8 ms: 1.24x slower                                                   |
| richards_super             | 46.5 ms                                                               | 58.6 ms: 1.26x slower                                                   |
| scimark_monte_carlo        | 60.8 ms                                                               | 76.7 ms: 1.26x slower                                                   |
| typing_runtime_protocols   | 151 us                                                                | 191 us: 1.27x slower                                                    |
| python_startup             | 12.6 ms                                                               | 16.0 ms: 1.27x slower                                                   |
| crypto_pyaes               | 67.1 ms                                                               | 85.9 ms: 1.28x slower                                                   |
| python_startup_no_site     | 7.33 ms                                                               | 9.61 ms: 1.31x slower                                                   |
| coverage                   | 81.4 ms                                                               | 109 ms: 1.34x slower                                                    |
| nbody                      | 89.2 ms                                                               | 121 ms: 1.35x slower                                                    |
| mako                       | 11.8 ms                                                               | 15.9 ms: 1.35x slower                                                   |
| bench_thread_pool          | 1.04 ms                                                               | 3.43 ms: 3.29x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.11x slower                                                            |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.088x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.21x