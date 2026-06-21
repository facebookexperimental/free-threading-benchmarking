# Results vs. base

- fork: python
- ref: a9db5cb52fefffc8fcdd
- machine: linux-x86_64
- commit hash: a9db5cb
- commit date: 2026-06-19
- overall geometric mean: 1.110x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json | results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                                                          | 293 ms: 1.14x slower                                                                                                  |
| docutils       | 2.40 sec                                                                                                        | 2.97 sec: 1.24x slower                                                                                                |
| html5lib       | 60.0 ms                                                                                                         | 69.0 ms: 1.15x slower                                                                                                 |
| sphinx         | 980 ms                                                                                                          | 1.12 sec: 1.14x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json | results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 755 ms                                                                                                          | 677 ms: 1.12x faster                                                                                                  |
| asyncio_websockets         | 543 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 716 ms                                                                                                          | 699 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 557 ms                                                                                                          | 578 ms: 1.04x slower                                                                                                  |
| coroutines                 | 23.5 ms                                                                                                         | 24.6 ms: 1.05x slower                                                                                                 |
| async_tree_memoization_tg  | 361 ms                                                                                                          | 391 ms: 1.08x slower                                                                                                  |
| async_tree_none_tg         | 295 ms                                                                                                          | 322 ms: 1.09x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 416 ms: 1.10x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 601 ms: 1.11x slower                                                                                                  |
| async_generators           | 336 ms                                                                                                          | 386 ms: 1.15x slower                                                                                                  |
| async_tree_none            | 291 ms                                                                                                          | 337 ms: 1.16x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json | results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 188 ms                                                                                                          | 181 ms: 1.03x faster                                                                                                  |
| float          | 73.4 ms                                                                                                         | 86.2 ms: 1.18x slower                                                                                                 |
| nbody          | 89.9 ms                                                                                                         | 127 ms: 1.42x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json | results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.1 ms                                                                                                         | 21.5 ms: 1.02x slower                                                                                                 |
| regex_dna      | 175 ms                                                                                                          | 188 ms: 1.07x slower                                                                                                  |
| regex_compile  | 122 ms                                                                                                          | 141 ms: 1.15x slower                                                                                                  |
| regex_effbot   | 2.69 ms                                                                                                         | 3.19 ms: 1.19x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json | results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 144 ms                                                                                                          | 142 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 89.6 ms                                                                                                         | 95.2 ms: 1.06x slower                                                                                                 |
| tomli_loads          | 1.83 sec                                                                                                        | 1.95 sec: 1.06x slower                                                                                                |
| json_dumps           | 9.76 ms                                                                                                         | 10.6 ms: 1.09x slower                                                                                                 |
| pickle_pure_python   | 307 us                                                                                                          | 338 us: 1.10x slower                                                                                                  |
| json_loads           | 27.2 us                                                                                                         | 30.3 us: 1.11x slower                                                                                                 |
| unpickle_pure_python | 209 us                                                                                                          | 237 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 85.9 ms                                                                                                         | 101 ms: 1.18x slower                                                                                                  |
| xml_etree_process    | 60.6 ms                                                                                                         | 74.6 ms: 1.23x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json | results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 6.94 ms                                                                                                         | 9.18 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json | results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.1 ms                                                                                                         | 41.1 ms: 1.17x slower                                                                                                 |
| mako            | 12.4 ms                                                                                                         | 16.3 ms: 1.32x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json | results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 248 ms                                                                                                          | 6.86 ms: 36.11x faster                                                                                                |
| gc_traversal               | 3.77 ms                                                                                                         | 1.76 ms: 2.15x faster                                                                                                 |
| create_gc_cycles           | 1.68 ms                                                                                                         | 1.34 ms: 1.25x faster                                                                                                 |
| sqlite_synth               | 2.22 us                                                                                                         | 1.96 us: 1.13x faster                                                                                                 |
| async_tree_io_tg           | 755 ms                                                                                                          | 677 ms: 1.12x faster                                                                                                  |
| asyncio_websockets         | 543 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| pidigits                   | 188 ms                                                                                                          | 181 ms: 1.03x faster                                                                                                  |
| async_tree_io              | 716 ms                                                                                                          | 699 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 144 ms                                                                                                          | 142 ms: 1.02x faster                                                                                                  |
| regex_v8                   | 21.1 ms                                                                                                         | 21.5 ms: 1.02x slower                                                                                                 |
| dulwich_log                | 67.6 ms                                                                                                         | 69.9 ms: 1.03x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 557 ms                                                                                                          | 578 ms: 1.04x slower                                                                                                  |
| bpe_tokeniser              | 4.22 sec                                                                                                        | 4.39 sec: 1.04x slower                                                                                                |
| json                       | 5.09 ms                                                                                                         | 5.30 ms: 1.04x slower                                                                                                 |
| coroutines                 | 23.5 ms                                                                                                         | 24.6 ms: 1.05x slower                                                                                                 |
| pycparser                  | 1.11 sec                                                                                                        | 1.17 sec: 1.06x slower                                                                                                |
| xml_etree_iterparse        | 89.6 ms                                                                                                         | 95.2 ms: 1.06x slower                                                                                                 |
| tomli_loads                | 1.83 sec                                                                                                        | 1.95 sec: 1.06x slower                                                                                                |
| logging_silent             | 98.0 ns                                                                                                         | 104 ns: 1.06x slower                                                                                                  |
| regex_dna                  | 175 ms                                                                                                          | 188 ms: 1.07x slower                                                                                                  |
| async_tree_memoization_tg  | 361 ms                                                                                                          | 391 ms: 1.08x slower                                                                                                  |
| json_dumps                 | 9.76 ms                                                                                                         | 10.6 ms: 1.09x slower                                                                                                 |
| async_tree_none_tg         | 295 ms                                                                                                          | 322 ms: 1.09x slower                                                                                                  |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.47 ms: 1.09x slower                                                                                                 |
| many_optionals             | 911 us                                                                                                          | 997 us: 1.09x slower                                                                                                  |
| comprehensions             | 15.8 us                                                                                                         | 17.3 us: 1.10x slower                                                                                                 |
| pickle_pure_python         | 307 us                                                                                                          | 338 us: 1.10x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 416 ms: 1.10x slower                                                                                                  |
| telco                      | 158 ms                                                                                                          | 175 ms: 1.11x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 601 ms: 1.11x slower                                                                                                  |
| generators                 | 28.6 ms                                                                                                         | 31.8 ms: 1.11x slower                                                                                                 |
| json_loads                 | 27.2 us                                                                                                         | 30.3 us: 1.11x slower                                                                                                 |
| scimark_fft                | 316 ms                                                                                                          | 353 ms: 1.11x slower                                                                                                  |
| pprint_safe_repr           | 714 ms                                                                                                          | 797 ms: 1.12x slower                                                                                                  |
| deepcopy_reduce            | 2.57 us                                                                                                         | 2.87 us: 1.12x slower                                                                                                 |
| scimark_sor                | 107 ms                                                                                                          | 120 ms: 1.12x slower                                                                                                  |
| pyflate                    | 404 ms                                                                                                          | 454 ms: 1.12x slower                                                                                                  |
| k_core                     | 2.01 sec                                                                                                        | 2.26 sec: 1.12x slower                                                                                                |
| pprint_pformat             | 1.46 sec                                                                                                        | 1.65 sec: 1.13x slower                                                                                                |
| unpickle_pure_python       | 209 us                                                                                                          | 237 us: 1.13x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.8 ms                                                                                                         | 57.5 ms: 1.13x slower                                                                                                 |
| sphinx                     | 980 ms                                                                                                          | 1.12 sec: 1.14x slower                                                                                                |
| deepcopy                   | 232 us                                                                                                          | 265 us: 1.14x slower                                                                                                  |
| subparsers                 | 9.22 ms                                                                                                         | 10.5 ms: 1.14x slower                                                                                                 |
| sqlglot_v2_normalize       | 100 ms                                                                                                          | 114 ms: 1.14x slower                                                                                                  |
| 2to3                       | 256 ms                                                                                                          | 293 ms: 1.14x slower                                                                                                  |
| sympy_expand               | 460 ms                                                                                                          | 527 ms: 1.14x slower                                                                                                  |
| scimark_lu                 | 114 ms                                                                                                          | 131 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.13 sec                                                                                                        | 1.30 sec: 1.15x slower                                                                                                |
| async_generators           | 336 ms                                                                                                          | 386 ms: 1.15x slower                                                                                                  |
| html5lib                   | 60.0 ms                                                                                                         | 69.0 ms: 1.15x slower                                                                                                 |
| deltablue                  | 3.18 ms                                                                                                         | 3.66 ms: 1.15x slower                                                                                                 |
| regex_compile              | 122 ms                                                                                                          | 141 ms: 1.15x slower                                                                                                  |
| sympy_sum                  | 157 ms                                                                                                          | 182 ms: 1.16x slower                                                                                                  |
| async_tree_none            | 291 ms                                                                                                          | 337 ms: 1.16x slower                                                                                                  |
| sympy_str                  | 273 ms                                                                                                          | 316 ms: 1.16x slower                                                                                                  |
| sympy_integrate            | 19.0 ms                                                                                                         | 22.0 ms: 1.16x slower                                                                                                 |
| pylint                     | 115 ms                                                                                                          | 133 ms: 1.16x slower                                                                                                  |
| django_template            | 35.1 ms                                                                                                         | 41.1 ms: 1.17x slower                                                                                                 |
| float                      | 73.4 ms                                                                                                         | 86.2 ms: 1.18x slower                                                                                                 |
| go                         | 102 ms                                                                                                          | 120 ms: 1.18x slower                                                                                                  |
| logging_format             | 6.62 us                                                                                                         | 7.79 us: 1.18x slower                                                                                                 |
| xml_etree_generate         | 85.9 ms                                                                                                         | 101 ms: 1.18x slower                                                                                                  |
| chaos                      | 53.7 ms                                                                                                         | 63.3 ms: 1.18x slower                                                                                                 |
| logging_simple             | 5.88 us                                                                                                         | 6.94 us: 1.18x slower                                                                                                 |
| deepcopy_memo              | 26.3 us                                                                                                         | 31.1 us: 1.18x slower                                                                                                 |
| hexiom                     | 5.61 ms                                                                                                         | 6.63 ms: 1.18x slower                                                                                                 |
| spectral_norm              | 92.1 ms                                                                                                         | 109 ms: 1.18x slower                                                                                                  |
| regex_effbot               | 2.69 ms                                                                                                         | 3.19 ms: 1.19x slower                                                                                                 |
| nqueens                    | 73.1 ms                                                                                                         | 87.3 ms: 1.19x slower                                                                                                 |
| thrift                     | 772 us                                                                                                          | 926 us: 1.20x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.44 ms                                                                                                         | 1.73 ms: 1.21x slower                                                                                                 |
| raytrace                   | 251 ms                                                                                                          | 306 ms: 1.22x slower                                                                                                  |
| shortest_path              | 440 ms                                                                                                          | 537 ms: 1.22x slower                                                                                                  |
| typing_runtime_protocols   | 118 us                                                                                                          | 145 us: 1.23x slower                                                                                                  |
| xml_etree_process          | 60.6 ms                                                                                                         | 74.6 ms: 1.23x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.49 ms                                                                                                         | 5.54 ms: 1.23x slower                                                                                                 |
| docutils                   | 2.40 sec                                                                                                        | 2.97 sec: 1.24x slower                                                                                                |
| richards                   | 42.6 ms                                                                                                         | 52.7 ms: 1.24x slower                                                                                                 |
| connected_components       | 395 ms                                                                                                          | 491 ms: 1.24x slower                                                                                                  |
| fannkuch                   | 373 ms                                                                                                          | 464 ms: 1.24x slower                                                                                                  |
| sqlglot_v2_parse           | 1.13 ms                                                                                                         | 1.41 ms: 1.24x slower                                                                                                 |
| scimark_monte_carlo        | 63.4 ms                                                                                                         | 79.0 ms: 1.25x slower                                                                                                 |
| richards_super             | 48.4 ms                                                                                                         | 60.7 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 100 ms                                                                                                          | 127 ms: 1.26x slower                                                                                                  |
| crypto_pyaes               | 69.4 ms                                                                                                         | 90.6 ms: 1.31x slower                                                                                                 |
| mako                       | 12.4 ms                                                                                                         | 16.3 ms: 1.32x slower                                                                                                 |
| python_startup_no_site     | 6.94 ms                                                                                                         | 9.18 ms: 1.32x slower                                                                                                 |
| coverage                   | 83.4 ms                                                                                                         | 114 ms: 1.37x slower                                                                                                  |
| nbody                      | 89.9 ms                                                                                                         | 127 ms: 1.42x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.110x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x