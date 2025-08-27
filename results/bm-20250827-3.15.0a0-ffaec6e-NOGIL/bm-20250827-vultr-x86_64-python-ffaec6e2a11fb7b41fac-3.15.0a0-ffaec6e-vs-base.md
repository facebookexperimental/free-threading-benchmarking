# Results vs. base

- fork: python
- ref: ffaec6e2a11fb7b41fac
- machine: linux-x86_64
- commit hash: ffaec6e
- commit date: 2025-08-27
- overall geometric mean: 1.094x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json | results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                          | 282 ms: 1.13x slower                                                                                                  |
| docutils       | 2.56 sec                                                                                                        | 2.68 sec: 1.04x slower                                                                                                |
| html5lib       | 61.5 ms                                                                                                         | 66.4 ms: 1.08x slower                                                                                                 |
| sphinx         | 969 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json | results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 619 ms                                                                                                          | 519 ms: 1.19x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 226 ms: 1.12x faster                                                                                                  |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 285 ms: 1.09x faster                                                                                                  |
| async_tree_io              | 594 ms                                                                                                          | 551 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                                                          | 480 ms: 1.05x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_none            | 256 ms                                                                                                          | 259 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 498 ms                                                                                                          | 508 ms: 1.02x slower                                                                                                  |
| coroutines                 | 23.7 ms                                                                                                         | 24.8 ms: 1.05x slower                                                                                                 |
| async_generators           | 340 ms                                                                                                          | 378 ms: 1.11x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json | results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 218 ms                                                                                                          | 192 ms: 1.14x faster                                                                                                  |
| float          | 72.1 ms                                                                                                         | 69.7 ms: 1.04x faster                                                                                                 |
| nbody          | 91.3 ms                                                                                                         | 124 ms: 1.36x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json | results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                                                         | 20.2 ms: 1.07x faster                                                                                                 |
| regex_effbot   | 2.60 ms                                                                                                         | 2.55 ms: 1.02x faster                                                                                                 |
| regex_dna      | 167 ms                                                                                                          | 164 ms: 1.02x faster                                                                                                  |
| regex_compile  | 123 ms                                                                                                          | 144 ms: 1.18x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.01x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json | results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.6 ms                                                                                                         | 87.7 ms: 1.06x faster                                                                                                 |
| json_dumps           | 9.69 ms                                                                                                         | 10.5 ms: 1.08x slower                                                                                                 |
| json_loads           | 28.3 us                                                                                                         | 31.4 us: 1.11x slower                                                                                                 |
| unpickle_pure_python | 210 us                                                                                                          | 236 us: 1.12x slower                                                                                                  |
| pickle_pure_python   | 304 us                                                                                                          | 347 us: 1.14x slower                                                                                                  |
| tomli_loads          | 1.89 sec                                                                                                        | 2.15 sec: 1.14x slower                                                                                                |
| xml_etree_generate   | 82.4 ms                                                                                                         | 96.9 ms: 1.18x slower                                                                                                 |
| xml_etree_process    | 57.8 ms                                                                                                         | 69.9 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json | results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                         | 15.6 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.21 ms                                                                                                         | 9.48 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json | results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                                                                         | 40.8 ms: 1.18x slower                                                                                                 |
| genshi_xml      | 48.9 ms                                                                                                         | 58.5 ms: 1.20x slower                                                                                                 |
| genshi_text     | 20.7 ms                                                                                                         | 27.2 ms: 1.31x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.6 ms: 1.33x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json | results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.37 ms                                                                                                         | 1.91 ms: 2.28x faster                                                                                                 |
| create_gc_cycles           | 1.93 ms                                                                                                         | 1.50 ms: 1.29x faster                                                                                                 |
| async_tree_io_tg           | 619 ms                                                                                                          | 519 ms: 1.19x faster                                                                                                  |
| pidigits                   | 218 ms                                                                                                          | 192 ms: 1.14x faster                                                                                                  |
| async_tree_none_tg         | 254 ms                                                                                                          | 226 ms: 1.12x faster                                                                                                  |
| sqlite_synth               | 2.29 us                                                                                                         | 2.06 us: 1.11x faster                                                                                                 |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 285 ms: 1.09x faster                                                                                                  |
| async_tree_io              | 594 ms                                                                                                          | 551 ms: 1.08x faster                                                                                                  |
| regex_v8                   | 21.6 ms                                                                                                         | 20.2 ms: 1.07x faster                                                                                                 |
| xml_etree_iterparse        | 92.6 ms                                                                                                         | 87.7 ms: 1.06x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                                                          | 480 ms: 1.05x faster                                                                                                  |
| float                      | 72.1 ms                                                                                                         | 69.7 ms: 1.04x faster                                                                                                 |
| regex_effbot               | 2.60 ms                                                                                                         | 2.55 ms: 1.02x faster                                                                                                 |
| regex_dna                  | 167 ms                                                                                                          | 164 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_none            | 256 ms                                                                                                          | 259 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 498 ms                                                                                                          | 508 ms: 1.02x slower                                                                                                  |
| json                       | 5.21 ms                                                                                                         | 5.37 ms: 1.03x slower                                                                                                 |
| pycparser                  | 1.08 sec                                                                                                        | 1.12 sec: 1.04x slower                                                                                                |
| docutils                   | 2.56 sec                                                                                                        | 2.68 sec: 1.04x slower                                                                                                |
| coroutines                 | 23.7 ms                                                                                                         | 24.8 ms: 1.05x slower                                                                                                 |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.41 sec: 1.05x slower                                                                                                |
| bench_mp_pool              | 103 ms                                                                                                          | 109 ms: 1.05x slower                                                                                                  |
| logging_silent             | 98.5 ns                                                                                                         | 104 ns: 1.06x slower                                                                                                  |
| html5lib                   | 61.5 ms                                                                                                         | 66.4 ms: 1.08x slower                                                                                                 |
| json_dumps                 | 9.69 ms                                                                                                         | 10.5 ms: 1.08x slower                                                                                                 |
| dulwich_log                | 66.1 ms                                                                                                         | 71.9 ms: 1.09x slower                                                                                                 |
| sphinx                     | 969 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| pylint                     | 279 ms                                                                                                          | 307 ms: 1.10x slower                                                                                                  |
| many_optionals             | 1.20 ms                                                                                                         | 1.33 ms: 1.11x slower                                                                                                 |
| json_loads                 | 28.3 us                                                                                                         | 31.4 us: 1.11x slower                                                                                                 |
| k_core                     | 2.02 sec                                                                                                        | 2.24 sec: 1.11x slower                                                                                                |
| async_generators           | 340 ms                                                                                                          | 378 ms: 1.11x slower                                                                                                  |
| telco                      | 158 ms                                                                                                          | 176 ms: 1.11x slower                                                                                                  |
| scimark_fft                | 331 ms                                                                                                          | 369 ms: 1.12x slower                                                                                                  |
| unpickle_pure_python       | 210 us                                                                                                          | 236 us: 1.12x slower                                                                                                  |
| sympy_expand               | 465 ms                                                                                                          | 523 ms: 1.12x slower                                                                                                  |
| 2to3                       | 250 ms                                                                                                          | 282 ms: 1.13x slower                                                                                                  |
| chaos                      | 55.8 ms                                                                                                         | 63.2 ms: 1.13x slower                                                                                                 |
| scimark_sor                | 108 ms                                                                                                          | 123 ms: 1.14x slower                                                                                                  |
| mdp                        | 1.15 sec                                                                                                        | 1.31 sec: 1.14x slower                                                                                                |
| comprehensions             | 15.6 us                                                                                                         | 17.8 us: 1.14x slower                                                                                                 |
| pickle_pure_python         | 304 us                                                                                                          | 347 us: 1.14x slower                                                                                                  |
| tomli_loads                | 1.89 sec                                                                                                        | 2.15 sec: 1.14x slower                                                                                                |
| pyflate                    | 399 ms                                                                                                          | 456 ms: 1.14x slower                                                                                                  |
| subparsers                 | 42.8 ms                                                                                                         | 49.1 ms: 1.15x slower                                                                                                 |
| hexiom                     | 5.63 ms                                                                                                         | 6.48 ms: 1.15x slower                                                                                                 |
| sqlglot_v2_optimize        | 50.0 ms                                                                                                         | 58.0 ms: 1.16x slower                                                                                                 |
| sqlglot_v2_normalize       | 100 ms                                                                                                          | 116 ms: 1.16x slower                                                                                                  |
| pprint_safe_repr           | 680 ms                                                                                                          | 790 ms: 1.16x slower                                                                                                  |
| nqueens                    | 76.4 ms                                                                                                         | 89.2 ms: 1.17x slower                                                                                                 |
| sympy_str                  | 269 ms                                                                                                          | 314 ms: 1.17x slower                                                                                                  |
| pprint_pformat             | 1.39 sec                                                                                                        | 1.63 sec: 1.17x slower                                                                                                |
| go                         | 104 ms                                                                                                          | 122 ms: 1.17x slower                                                                                                  |
| generators                 | 27.6 ms                                                                                                         | 32.4 ms: 1.17x slower                                                                                                 |
| regex_compile              | 123 ms                                                                                                          | 144 ms: 1.18x slower                                                                                                  |
| deepcopy_reduce            | 2.61 us                                                                                                         | 3.07 us: 1.18x slower                                                                                                 |
| spectral_norm              | 94.4 ms                                                                                                         | 111 ms: 1.18x slower                                                                                                  |
| xml_etree_generate         | 82.4 ms                                                                                                         | 96.9 ms: 1.18x slower                                                                                                 |
| scimark_lu                 | 112 ms                                                                                                          | 131 ms: 1.18x slower                                                                                                  |
| django_template            | 34.7 ms                                                                                                         | 40.8 ms: 1.18x slower                                                                                                 |
| deepcopy                   | 252 us                                                                                                          | 297 us: 1.18x slower                                                                                                  |
| sympy_integrate            | 18.8 ms                                                                                                         | 22.2 ms: 1.18x slower                                                                                                 |
| raytrace                   | 251 ms                                                                                                          | 298 ms: 1.18x slower                                                                                                  |
| sympy_sum                  | 152 ms                                                                                                          | 181 ms: 1.19x slower                                                                                                  |
| logging_simple             | 5.74 us                                                                                                         | 6.84 us: 1.19x slower                                                                                                 |
| logging_format             | 6.44 us                                                                                                         | 7.67 us: 1.19x slower                                                                                                 |
| thrift                     | 738 us                                                                                                          | 880 us: 1.19x slower                                                                                                  |
| fannkuch                   | 380 ms                                                                                                          | 454 ms: 1.20x slower                                                                                                  |
| meteor_contest             | 99.9 ms                                                                                                         | 120 ms: 1.20x slower                                                                                                  |
| genshi_xml                 | 48.9 ms                                                                                                         | 58.5 ms: 1.20x slower                                                                                                 |
| deltablue                  | 3.08 ms                                                                                                         | 3.69 ms: 1.20x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.52 ms                                                                                                         | 1.83 ms: 1.20x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.70 ms                                                                                                         | 5.65 ms: 1.20x slower                                                                                                 |
| xml_etree_process          | 57.8 ms                                                                                                         | 69.9 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.22 ms                                                                                                         | 1.48 ms: 1.21x slower                                                                                                 |
| shortest_path              | 441 ms                                                                                                          | 536 ms: 1.22x slower                                                                                                  |
| deepcopy_memo              | 28.8 us                                                                                                         | 35.1 us: 1.22x slower                                                                                                 |
| typing_runtime_protocols   | 154 us                                                                                                          | 188 us: 1.22x slower                                                                                                  |
| connected_components       | 400 ms                                                                                                          | 490 ms: 1.23x slower                                                                                                  |
| scimark_monte_carlo        | 63.0 ms                                                                                                         | 78.5 ms: 1.25x slower                                                                                                 |
| crypto_pyaes               | 69.3 ms                                                                                                         | 86.3 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.4 ms                                                                                                         | 15.6 ms: 1.25x slower                                                                                                 |
| richards                   | 41.3 ms                                                                                                         | 52.3 ms: 1.27x slower                                                                                                 |
| richards_super             | 47.0 ms                                                                                                         | 60.8 ms: 1.29x slower                                                                                                 |
| genshi_text                | 20.7 ms                                                                                                         | 27.2 ms: 1.31x slower                                                                                                 |
| python_startup_no_site     | 7.21 ms                                                                                                         | 9.48 ms: 1.32x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.6 ms: 1.33x slower                                                                                                 |
| nbody                      | 91.3 ms                                                                                                         | 124 ms: 1.36x slower                                                                                                  |
| coverage                   | 81.9 ms                                                                                                         | 111 ms: 1.36x slower                                                                                                  |
| bench_thread_pool          | 1.01 ms                                                                                                         | 3.13 ms: 3.10x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmark hidden because not significant (3): pathlib, xml_etree_parse, async_tree_memoization

- Geometric mean (including insignificant results): 1.094x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x