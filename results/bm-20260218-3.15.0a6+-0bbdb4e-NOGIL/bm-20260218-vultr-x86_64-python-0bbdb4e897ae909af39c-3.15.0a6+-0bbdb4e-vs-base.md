# Results vs. base

- fork: python
- ref: 0bbdb4e897ae909af39c
- machine: linux-x86_64
- commit hash: 0bbdb4e
- commit date: 2026-02-18
- overall geometric mean: 1.108x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json | results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                                                                            | 278 ms: 1.13x slower                                                                                                    |
| docutils       | 2.53 sec                                                                                                          | 2.76 sec: 1.09x slower                                                                                                  |
| html5lib       | 59.8 ms                                                                                                           | 66.4 ms: 1.11x slower                                                                                                   |
| sphinx         | 955 ms                                                                                                            | 1.05 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json | results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 544 ms                                                                                                            | 514 ms: 1.06x faster                                                                                                    |
| coroutines                 | 24.0 ms                                                                                                           | 23.4 ms: 1.03x faster                                                                                                   |
| async_tree_none_tg         | 248 ms                                                                                                            | 264 ms: 1.06x slower                                                                                                    |
| async_tree_io_tg           | 568 ms                                                                                                            | 606 ms: 1.07x slower                                                                                                    |
| async_tree_io              | 573 ms                                                                                                            | 629 ms: 1.10x slower                                                                                                    |
| async_generators           | 342 ms                                                                                                            | 377 ms: 1.10x slower                                                                                                    |
| async_tree_memoization_tg  | 295 ms                                                                                                            | 325 ms: 1.10x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                                                            | 553 ms: 1.12x slower                                                                                                    |
| async_tree_none            | 247 ms                                                                                                            | 287 ms: 1.16x slower                                                                                                    |
| async_tree_memoization     | 301 ms                                                                                                            | 355 ms: 1.18x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 485 ms                                                                                                            | 578 ms: 1.19x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json | results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 69.6 ms                                                                                                           | 73.5 ms: 1.06x slower                                                                                                   |
| pidigits       | 194 ms                                                                                                            | 209 ms: 1.08x slower                                                                                                    |
| nbody          | 88.2 ms                                                                                                           | 122 ms: 1.38x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json | results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.3 ms                                                                                                           | 21.5 ms: 1.01x slower                                                                                                   |
| regex_dna      | 165 ms                                                                                                            | 181 ms: 1.09x slower                                                                                                    |
| regex_effbot   | 2.66 ms                                                                                                           | 2.93 ms: 1.10x slower                                                                                                   |
| regex_compile  | 121 ms                                                                                                            | 142 ms: 1.17x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json | results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 83.8 ms                                                                                                           | 88.3 ms: 1.05x slower                                                                                                   |
| tomli_loads          | 1.86 sec                                                                                                          | 1.97 sec: 1.06x slower                                                                                                  |
| pickle_pure_python   | 305 us                                                                                                            | 332 us: 1.09x slower                                                                                                    |
| unpickle_pure_python | 211 us                                                                                                            | 235 us: 1.11x slower                                                                                                    |
| json_dumps           | 9.85 ms                                                                                                           | 11.1 ms: 1.13x slower                                                                                                   |
| xml_etree_generate   | 83.6 ms                                                                                                           | 95.3 ms: 1.14x slower                                                                                                   |
| json_loads           | 28.3 us                                                                                                           | 32.4 us: 1.14x slower                                                                                                   |
| xml_etree_process    | 58.8 ms                                                                                                           | 68.7 ms: 1.17x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json | results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                           | 16.0 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 7.33 ms                                                                                                           | 9.76 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json | results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 48.7 ms                                                                                                           | 54.6 ms: 1.12x slower                                                                                                   |
| django_template | 35.1 ms                                                                                                           | 40.4 ms: 1.15x slower                                                                                                   |
| genshi_text     | 20.8 ms                                                                                                           | 25.9 ms: 1.24x slower                                                                                                   |
| mako            | 11.9 ms                                                                                                           | 15.9 ms: 1.34x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.21x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json | results/bm-20260218-3.15.0a6+-0bbdb4e-NOGIL/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 331 ms                                                                                                            | 7.11 ms: 46.53x faster                                                                                                  |
| gc_traversal               | 4.47 ms                                                                                                           | 1.93 ms: 2.32x faster                                                                                                   |
| create_gc_cycles           | 1.86 ms                                                                                                           | 1.49 ms: 1.25x faster                                                                                                   |
| sqlite_synth               | 2.20 us                                                                                                           | 1.93 us: 1.14x faster                                                                                                   |
| asyncio_websockets         | 544 ms                                                                                                            | 514 ms: 1.06x faster                                                                                                    |
| coroutines                 | 24.0 ms                                                                                                           | 23.4 ms: 1.03x faster                                                                                                   |
| regex_v8                   | 21.3 ms                                                                                                           | 21.5 ms: 1.01x slower                                                                                                   |
| pathlib                    | 17.3 ms                                                                                                           | 17.6 ms: 1.01x slower                                                                                                   |
| logging_silent             | 100 ns                                                                                                            | 102 ns: 1.02x slower                                                                                                    |
| pylint                     | 283 ms                                                                                                            | 292 ms: 1.03x slower                                                                                                    |
| pycparser                  | 1.09 sec                                                                                                          | 1.13 sec: 1.04x slower                                                                                                  |
| bpe_tokeniser              | 4.18 sec                                                                                                          | 4.36 sec: 1.04x slower                                                                                                  |
| xml_etree_iterparse        | 83.8 ms                                                                                                           | 88.3 ms: 1.05x slower                                                                                                   |
| float                      | 69.6 ms                                                                                                           | 73.5 ms: 1.06x slower                                                                                                   |
| json                       | 5.14 ms                                                                                                           | 5.43 ms: 1.06x slower                                                                                                   |
| tomli_loads                | 1.86 sec                                                                                                          | 1.97 sec: 1.06x slower                                                                                                  |
| async_tree_none_tg         | 248 ms                                                                                                            | 264 ms: 1.06x slower                                                                                                    |
| async_tree_io_tg           | 568 ms                                                                                                            | 606 ms: 1.07x slower                                                                                                    |
| dulwich_log                | 66.8 ms                                                                                                           | 71.3 ms: 1.07x slower                                                                                                   |
| pidigits                   | 194 ms                                                                                                            | 209 ms: 1.08x slower                                                                                                    |
| deltablue                  | 3.33 ms                                                                                                           | 3.61 ms: 1.08x slower                                                                                                   |
| many_optionals             | 942 us                                                                                                            | 1.02 ms: 1.09x slower                                                                                                   |
| pickle_pure_python         | 305 us                                                                                                            | 332 us: 1.09x slower                                                                                                    |
| docutils                   | 2.53 sec                                                                                                          | 2.76 sec: 1.09x slower                                                                                                  |
| regex_dna                  | 165 ms                                                                                                            | 181 ms: 1.09x slower                                                                                                    |
| async_tree_io              | 573 ms                                                                                                            | 629 ms: 1.10x slower                                                                                                    |
| telco                      | 157 ms                                                                                                            | 172 ms: 1.10x slower                                                                                                    |
| pyflate                    | 415 ms                                                                                                            | 456 ms: 1.10x slower                                                                                                    |
| async_generators           | 342 ms                                                                                                            | 377 ms: 1.10x slower                                                                                                    |
| regex_effbot               | 2.66 ms                                                                                                           | 2.93 ms: 1.10x slower                                                                                                   |
| async_tree_memoization_tg  | 295 ms                                                                                                            | 325 ms: 1.10x slower                                                                                                    |
| sphinx                     | 955 ms                                                                                                            | 1.05 sec: 1.10x slower                                                                                                  |
| html5lib                   | 59.8 ms                                                                                                           | 66.4 ms: 1.11x slower                                                                                                   |
| unpickle_pure_python       | 211 us                                                                                                            | 235 us: 1.11x slower                                                                                                    |
| sympy_expand               | 470 ms                                                                                                            | 526 ms: 1.12x slower                                                                                                    |
| pprint_safe_repr           | 696 ms                                                                                                            | 779 ms: 1.12x slower                                                                                                    |
| genshi_xml                 | 48.7 ms                                                                                                           | 54.6 ms: 1.12x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                                                            | 553 ms: 1.12x slower                                                                                                    |
| scimark_fft                | 303 ms                                                                                                            | 340 ms: 1.12x slower                                                                                                    |
| go                         | 107 ms                                                                                                            | 121 ms: 1.13x slower                                                                                                    |
| 2to3                       | 246 ms                                                                                                            | 278 ms: 1.13x slower                                                                                                    |
| sqlglot_v2_optimize        | 50.7 ms                                                                                                           | 57.2 ms: 1.13x slower                                                                                                   |
| json_dumps                 | 9.85 ms                                                                                                           | 11.1 ms: 1.13x slower                                                                                                   |
| subparsers                 | 9.15 ms                                                                                                           | 10.3 ms: 1.13x slower                                                                                                   |
| chaos                      | 55.6 ms                                                                                                           | 63.3 ms: 1.14x slower                                                                                                   |
| comprehensions             | 16.0 us                                                                                                           | 18.2 us: 1.14x slower                                                                                                   |
| xml_etree_generate         | 83.6 ms                                                                                                           | 95.3 ms: 1.14x slower                                                                                                   |
| sympy_str                  | 275 ms                                                                                                            | 314 ms: 1.14x slower                                                                                                    |
| json_loads                 | 28.3 us                                                                                                           | 32.4 us: 1.14x slower                                                                                                   |
| logging_simple             | 5.92 us                                                                                                           | 6.77 us: 1.14x slower                                                                                                   |
| mdp                        | 1.15 sec                                                                                                          | 1.31 sec: 1.15x slower                                                                                                  |
| sympy_sum                  | 158 ms                                                                                                            | 181 ms: 1.15x slower                                                                                                    |
| pprint_pformat             | 1.41 sec                                                                                                          | 1.62 sec: 1.15x slower                                                                                                  |
| sympy_integrate            | 19.2 ms                                                                                                           | 22.1 ms: 1.15x slower                                                                                                   |
| sqlglot_v2_normalize       | 100 ms                                                                                                            | 116 ms: 1.15x slower                                                                                                    |
| spectral_norm              | 94.6 ms                                                                                                           | 109 ms: 1.15x slower                                                                                                    |
| django_template            | 35.1 ms                                                                                                           | 40.4 ms: 1.15x slower                                                                                                   |
| logging_format             | 6.60 us                                                                                                           | 7.64 us: 1.16x slower                                                                                                   |
| async_tree_none            | 247 ms                                                                                                            | 287 ms: 1.16x slower                                                                                                    |
| hexiom                     | 5.61 ms                                                                                                           | 6.51 ms: 1.16x slower                                                                                                   |
| deepcopy                   | 231 us                                                                                                            | 268 us: 1.16x slower                                                                                                    |
| nqueens                    | 77.1 ms                                                                                                           | 89.6 ms: 1.16x slower                                                                                                   |
| deepcopy_memo              | 26.3 us                                                                                                           | 30.6 us: 1.16x slower                                                                                                   |
| scimark_sor                | 104 ms                                                                                                            | 121 ms: 1.17x slower                                                                                                    |
| scimark_lu                 | 107 ms                                                                                                            | 125 ms: 1.17x slower                                                                                                    |
| xml_etree_process          | 58.8 ms                                                                                                           | 68.7 ms: 1.17x slower                                                                                                   |
| deepcopy_reduce            | 2.51 us                                                                                                           | 2.93 us: 1.17x slower                                                                                                   |
| raytrace                   | 252 ms                                                                                                            | 295 ms: 1.17x slower                                                                                                    |
| regex_compile              | 121 ms                                                                                                            | 142 ms: 1.17x slower                                                                                                    |
| async_tree_memoization     | 301 ms                                                                                                            | 355 ms: 1.18x slower                                                                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                           | 1.78 ms: 1.18x slower                                                                                                   |
| fannkuch                   | 385 ms                                                                                                            | 456 ms: 1.18x slower                                                                                                    |
| thrift                     | 780 us                                                                                                            | 924 us: 1.18x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 485 ms                                                                                                            | 578 ms: 1.19x slower                                                                                                    |
| k_core                     | 1.87 sec                                                                                                          | 2.23 sec: 1.19x slower                                                                                                  |
| sqlglot_v2_parse           | 1.20 ms                                                                                                           | 1.44 ms: 1.20x slower                                                                                                   |
| generators                 | 27.0 ms                                                                                                           | 32.8 ms: 1.22x slower                                                                                                   |
| richards                   | 42.6 ms                                                                                                           | 51.8 ms: 1.22x slower                                                                                                   |
| richards_super             | 48.4 ms                                                                                                           | 59.3 ms: 1.23x slower                                                                                                   |
| bench_thread_pool          | 1.31 ms                                                                                                           | 1.62 ms: 1.24x slower                                                                                                   |
| genshi_text                | 20.8 ms                                                                                                           | 25.9 ms: 1.24x slower                                                                                                   |
| typing_runtime_protocols   | 160 us                                                                                                            | 199 us: 1.24x slower                                                                                                    |
| connected_components       | 388 ms                                                                                                            | 482 ms: 1.24x slower                                                                                                    |
| shortest_path              | 428 ms                                                                                                            | 535 ms: 1.25x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.34 ms                                                                                                           | 5.43 ms: 1.25x slower                                                                                                   |
| meteor_contest             | 99.6 ms                                                                                                           | 125 ms: 1.25x slower                                                                                                    |
| scimark_monte_carlo        | 61.7 ms                                                                                                           | 78.0 ms: 1.26x slower                                                                                                   |
| python_startup             | 12.6 ms                                                                                                           | 16.0 ms: 1.27x slower                                                                                                   |
| crypto_pyaes               | 68.0 ms                                                                                                           | 87.0 ms: 1.28x slower                                                                                                   |
| python_startup_no_site     | 7.33 ms                                                                                                           | 9.76 ms: 1.33x slower                                                                                                   |
| mako                       | 11.9 ms                                                                                                           | 15.9 ms: 1.34x slower                                                                                                   |
| coverage                   | 82.0 ms                                                                                                           | 111 ms: 1.35x slower                                                                                                    |
| nbody                      | 88.2 ms                                                                                                           | 122 ms: 1.38x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

- Geometric mean (including insignificant results): 1.108x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.22x