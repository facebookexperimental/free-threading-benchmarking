# Results vs. base

- fork: Fidget-Spinner
- ref: jit_ft
- machine: linux-x86_64
- commit hash: 2f39aa8
- commit date: 2025-12-17
- overall geometric mean: 1.024x faster
- HPT reliability: 63.16%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 276 ms                                                                 | 278 ms: 1.01x slower                                               |
| docutils       | 2.77 sec                                                               | 2.94 sec: 1.06x slower                                             |
| html5lib       | 66.0 ms                                                                | 70.3 ms: 1.07x slower                                              |
| sphinx         | 1.07 sec                                                               | 1.10 sec: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| asyncio_websockets         | 510 ms                                                                 | 511 ms: 1.00x slower                                               |
| coroutines                 | 24.0 ms                                                                | 24.2 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed    | 548 ms                                                                 | 556 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed_tg | 523 ms                                                                 | 533 ms: 1.02x slower                                               |
| async_tree_io              | 618 ms                                                                 | 633 ms: 1.02x slower                                               |
| async_tree_io_tg           | 590 ms                                                                 | 607 ms: 1.03x slower                                               |
| async_generators           | 371 ms                                                                 | 391 ms: 1.05x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                       |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_none_tg, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| nbody          | 121 ms                                                                 | 105 ms: 1.16x faster                                               |
| float          | 72.2 ms                                                                | 64.2 ms: 1.12x faster                                              |
| pidigits       | 211 ms                                                                 | 192 ms: 1.10x faster                                               |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 2.90 ms                                                                | 2.92 ms: 1.01x slower                                              |
| regex_v8       | 21.5 ms                                                                | 21.9 ms: 1.02x slower                                              |
| regex_dna      | 177 ms                                                                 | 180 ms: 1.02x slower                                               |
| regex_compile  | 143 ms                                                                 | 146 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| unpickle_pure_python | 239 us                                                                 | 204 us: 1.17x faster                                               |
| xml_etree_process    | 70.1 ms                                                                | 63.6 ms: 1.10x faster                                              |
| xml_etree_generate   | 97.9 ms                                                                | 91.0 ms: 1.08x faster                                              |
| tomli_loads          | 2.31 sec                                                               | 2.15 sec: 1.07x faster                                             |
| pickle_pure_python   | 334 us                                                                 | 312 us: 1.07x faster                                               |
| json_dumps           | 11.3 ms                                                                | 10.7 ms: 1.05x faster                                              |
| json_loads           | 32.8 us                                                                | 32.2 us: 1.02x faster                                              |
| xml_etree_parse      | 132 ms                                                                 | 129 ms: 1.02x faster                                               |
| Geometric mean       | (ref)                                                                  | 1.06x faster                                                       |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 9.54 ms                                                                | 9.56 ms: 1.00x slower                                              |
| python_startup         | 15.9 ms                                                                | 15.9 ms: 1.00x slower                                              |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| mako           | 15.9 ms                                                                | 14.9 ms: 1.07x faster                                              |
| genshi_text    | 27.3 ms                                                                | 28.0 ms: 1.03x slower                                              |
| genshi_xml     | 57.7 ms                                                                | 67.7 ms: 1.17x slower                                              |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                       |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| richards                   | 52.4 ms                                                                | 22.7 ms: 2.31x faster                                              |
| richards_super             | 59.9 ms                                                                | 27.8 ms: 2.15x faster                                              |
| logging_silent             | 106 ns                                                                 | 83.3 ns: 1.27x faster                                              |
| scimark_fft                | 347 ms                                                                 | 292 ms: 1.19x faster                                               |
| unpickle_pure_python       | 239 us                                                                 | 204 us: 1.17x faster                                               |
| nbody                      | 121 ms                                                                 | 105 ms: 1.16x faster                                               |
| deltablue                  | 3.65 ms                                                                | 3.17 ms: 1.15x faster                                              |
| scimark_monte_carlo        | 78.0 ms                                                                | 68.7 ms: 1.14x faster                                              |
| float                      | 72.2 ms                                                                | 64.2 ms: 1.12x faster                                              |
| pyflate                    | 474 ms                                                                 | 425 ms: 1.11x faster                                               |
| spectral_norm              | 111 ms                                                                 | 99.9 ms: 1.11x faster                                              |
| xml_etree_process          | 70.1 ms                                                                | 63.6 ms: 1.10x faster                                              |
| pidigits                   | 211 ms                                                                 | 192 ms: 1.10x faster                                               |
| fannkuch                   | 465 ms                                                                 | 429 ms: 1.08x faster                                               |
| xml_etree_generate         | 97.9 ms                                                                | 91.0 ms: 1.08x faster                                              |
| pprint_safe_repr           | 774 ms                                                                 | 721 ms: 1.07x faster                                               |
| scimark_sor                | 122 ms                                                                 | 114 ms: 1.07x faster                                               |
| tomli_loads                | 2.31 sec                                                               | 2.15 sec: 1.07x faster                                             |
| pickle_pure_python         | 334 us                                                                 | 312 us: 1.07x faster                                               |
| mako                       | 15.9 ms                                                                | 14.9 ms: 1.07x faster                                              |
| go                         | 120 ms                                                                 | 112 ms: 1.07x faster                                               |
| json_dumps                 | 11.3 ms                                                                | 10.7 ms: 1.05x faster                                              |
| bpe_tokeniser              | 4.36 sec                                                               | 4.15 sec: 1.05x faster                                             |
| deepcopy_memo              | 30.6 us                                                                | 29.3 us: 1.04x faster                                              |
| pprint_pformat             | 1.61 sec                                                               | 1.55 sec: 1.04x faster                                             |
| scimark_lu                 | 131 ms                                                                 | 126 ms: 1.04x faster                                               |
| sqlite_synth               | 2.09 us                                                                | 2.02 us: 1.03x faster                                              |
| json                       | 5.54 ms                                                                | 5.38 ms: 1.03x faster                                              |
| thrift                     | 895 us                                                                 | 877 us: 1.02x faster                                               |
| coverage                   | 114 ms                                                                 | 111 ms: 1.02x faster                                               |
| deepcopy_reduce            | 2.97 us                                                                | 2.92 us: 1.02x faster                                              |
| crypto_pyaes               | 86.7 ms                                                                | 85.0 ms: 1.02x faster                                              |
| chaos                      | 62.4 ms                                                                | 61.2 ms: 1.02x faster                                              |
| json_loads                 | 32.8 us                                                                | 32.2 us: 1.02x faster                                              |
| xml_etree_parse            | 132 ms                                                                 | 129 ms: 1.02x faster                                               |
| meteor_contest             | 123 ms                                                                 | 121 ms: 1.02x faster                                               |
| logging_format             | 7.90 us                                                                | 7.79 us: 1.01x faster                                              |
| k_core                     | 2.21 sec                                                               | 2.18 sec: 1.01x faster                                             |
| shortest_path              | 530 ms                                                                 | 526 ms: 1.01x faster                                               |
| connected_components       | 482 ms                                                                 | 479 ms: 1.01x faster                                               |
| telco                      | 177 ms                                                                 | 176 ms: 1.01x faster                                               |
| asyncio_websockets         | 510 ms                                                                 | 511 ms: 1.00x slower                                               |
| python_startup_no_site     | 9.54 ms                                                                | 9.56 ms: 1.00x slower                                              |
| python_startup             | 15.9 ms                                                                | 15.9 ms: 1.00x slower                                              |
| regex_effbot               | 2.90 ms                                                                | 2.92 ms: 1.01x slower                                              |
| scimark_sparse_mat_mult    | 5.40 ms                                                                | 5.44 ms: 1.01x slower                                              |
| create_gc_cycles           | 1.45 ms                                                                | 1.46 ms: 1.01x slower                                              |
| 2to3                       | 276 ms                                                                 | 278 ms: 1.01x slower                                               |
| coroutines                 | 24.0 ms                                                                | 24.2 ms: 1.01x slower                                              |
| logging_simple             | 6.86 us                                                                | 6.94 us: 1.01x slower                                              |
| async_tree_cpu_io_mixed    | 548 ms                                                                 | 556 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed_tg | 523 ms                                                                 | 533 ms: 1.02x slower                                               |
| regex_v8                   | 21.5 ms                                                                | 21.9 ms: 1.02x slower                                              |
| many_optionals             | 1.04 ms                                                                | 1.06 ms: 1.02x slower                                              |
| regex_dna                  | 177 ms                                                                 | 180 ms: 1.02x slower                                               |
| pathlib                    | 17.7 ms                                                                | 18.0 ms: 1.02x slower                                              |
| deepcopy                   | 276 us                                                                 | 281 us: 1.02x slower                                               |
| pycparser                  | 1.14 sec                                                               | 1.16 sec: 1.02x slower                                             |
| async_tree_io              | 618 ms                                                                 | 633 ms: 1.02x slower                                               |
| regex_compile              | 143 ms                                                                 | 146 ms: 1.02x slower                                               |
| genshi_text                | 27.3 ms                                                                | 28.0 ms: 1.03x slower                                              |
| async_tree_io_tg           | 590 ms                                                                 | 607 ms: 1.03x slower                                               |
| sphinx                     | 1.07 sec                                                               | 1.10 sec: 1.03x slower                                             |
| comprehensions             | 18.8 us                                                                | 19.4 us: 1.03x slower                                              |
| raytrace                   | 300 ms                                                                 | 311 ms: 1.04x slower                                               |
| typing_runtime_protocols   | 192 us                                                                 | 200 us: 1.04x slower                                               |
| generators                 | 29.6 ms                                                                | 31.0 ms: 1.05x slower                                              |
| async_generators           | 371 ms                                                                 | 391 ms: 1.05x slower                                               |
| docutils                   | 2.77 sec                                                               | 2.94 sec: 1.06x slower                                             |
| html5lib                   | 66.0 ms                                                                | 70.3 ms: 1.07x slower                                              |
| sympy_integrate            | 21.8 ms                                                                | 23.2 ms: 1.07x slower                                              |
| dulwich_log                | 70.0 ms                                                                | 74.6 ms: 1.07x slower                                              |
| sqlglot_v2_optimize        | 59.5 ms                                                                | 63.7 ms: 1.07x slower                                              |
| sqlglot_v2_normalize       | 118 ms                                                                 | 128 ms: 1.08x slower                                               |
| pylint                     | 306 ms                                                                 | 331 ms: 1.08x slower                                               |
| nqueens                    | 92.7 ms                                                                | 100 ms: 1.08x slower                                               |
| sympy_sum                  | 178 ms                                                                 | 194 ms: 1.09x slower                                               |
| sympy_expand               | 525 ms                                                                 | 585 ms: 1.11x slower                                               |
| hexiom                     | 6.46 ms                                                                | 7.19 ms: 1.11x slower                                              |
| sympy_str                  | 312 ms                                                                 | 353 ms: 1.13x slower                                               |
| genshi_xml                 | 57.7 ms                                                                | 67.7 ms: 1.17x slower                                              |
| mdp                        | 1.33 sec                                                               | 1.58 sec: 1.18x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                       |

Benchmark hidden because not significant (12): subparsers, django_template, bench_mp_pool, gc_traversal, xml_etree_iterparse, bench_thread_pool, async_tree_memoization, sqlglot_v2_parse, async_tree_none_tg, async_tree_none, sqlglot_v2_transpile, async_tree_memoization_tg

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 63.16% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.03x