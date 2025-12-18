# Results vs. base

- fork: Fidget-Spinner
- ref: jit_ft
- machine: linux-x86_64
- commit hash: 00ae7b5
- commit date: 2025-12-18
- overall geometric mean: 1.034x faster
- HPT reliability: 51.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 276 ms                                                                 | 281 ms: 1.02x slower                                               |
| docutils       | 2.77 sec                                                               | 2.88 sec: 1.04x slower                                             |
| html5lib       | 66.0 ms                                                                | 70.6 ms: 1.07x slower                                              |
| sphinx         | 1.07 sec                                                               | 1.10 sec: 1.04x slower                                             |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| coroutines                | 24.0 ms                                                                | 24.4 ms: 1.02x slower                                              |
| async_tree_memoization_tg | 324 ms                                                                 | 331 ms: 1.02x slower                                               |
| async_tree_none_tg        | 263 ms                                                                 | 269 ms: 1.02x slower                                               |
| async_tree_none           | 284 ms                                                                 | 291 ms: 1.02x slower                                               |
| async_tree_io             | 618 ms                                                                 | 635 ms: 1.03x slower                                               |
| async_tree_io_tg          | 590 ms                                                                 | 615 ms: 1.04x slower                                               |
| async_generators          | 371 ms                                                                 | 399 ms: 1.07x slower                                               |
| Geometric mean            | (ref)                                                                  | 1.02x slower                                                       |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| nbody          | 121 ms                                                                 | 93.9 ms: 1.29x faster                                              |
| float          | 72.2 ms                                                                | 58.6 ms: 1.23x faster                                              |
| pidigits       | 211 ms                                                                 | 199 ms: 1.06x faster                                               |
| Geometric mean | (ref)                                                                  | 1.19x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 2.90 ms                                                                | 2.88 ms: 1.01x faster                                              |
| regex_dna      | 177 ms                                                                 | 176 ms: 1.00x faster                                               |
| regex_compile  | 143 ms                                                                 | 144 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                       |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| unpickle_pure_python | 239 us                                                                 | 204 us: 1.17x faster                                               |
| xml_etree_process    | 70.1 ms                                                                | 63.1 ms: 1.11x faster                                              |
| xml_etree_generate   | 97.9 ms                                                                | 89.8 ms: 1.09x faster                                              |
| tomli_loads          | 2.31 sec                                                               | 2.17 sec: 1.06x faster                                             |
| pickle_pure_python   | 334 us                                                                 | 314 us: 1.06x faster                                               |
| json_dumps           | 11.3 ms                                                                | 10.7 ms: 1.05x faster                                              |
| xml_etree_iterparse  | 87.5 ms                                                                | 87.0 ms: 1.01x faster                                              |
| Geometric mean       | (ref)                                                                  | 1.06x faster                                                       |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 16.0 ms: 1.01x slower                                              |
| python_startup_no_site | 9.54 ms                                                                | 9.63 ms: 1.01x slower                                              |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| mako            | 15.9 ms                                                                | 14.9 ms: 1.06x faster                                              |
| django_template | 41.2 ms                                                                | 40.3 ms: 1.02x faster                                              |
| genshi_text     | 27.3 ms                                                                | 27.6 ms: 1.01x slower                                              |
| genshi_xml      | 57.7 ms                                                                | 68.8 ms: 1.19x slower                                              |
| Geometric mean  | (ref)                                                                  | 1.03x slower                                                       |

All benchmarks:
===============

| Benchmark                 | bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3+-8b64dd8 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| richards                  | 52.4 ms                                                                | 20.3 ms: 2.58x faster                                              |
| richards_super            | 59.9 ms                                                                | 25.8 ms: 2.32x faster                                              |
| nbody                     | 121 ms                                                                 | 93.9 ms: 1.29x faster                                              |
| logging_silent            | 106 ns                                                                 | 82.6 ns: 1.28x faster                                              |
| float                     | 72.2 ms                                                                | 58.6 ms: 1.23x faster                                              |
| deltablue                 | 3.65 ms                                                                | 3.05 ms: 1.20x faster                                              |
| unpickle_pure_python      | 239 us                                                                 | 204 us: 1.17x faster                                               |
| scimark_fft               | 347 ms                                                                 | 296 ms: 1.17x faster                                               |
| pyflate                   | 474 ms                                                                 | 408 ms: 1.16x faster                                               |
| scimark_monte_carlo       | 78.0 ms                                                                | 67.9 ms: 1.15x faster                                              |
| go                        | 120 ms                                                                 | 104 ms: 1.15x faster                                               |
| fannkuch                  | 465 ms                                                                 | 417 ms: 1.11x faster                                               |
| xml_etree_process         | 70.1 ms                                                                | 63.1 ms: 1.11x faster                                              |
| spectral_norm             | 111 ms                                                                 | 100 ms: 1.10x faster                                               |
| pprint_safe_repr          | 774 ms                                                                 | 706 ms: 1.10x faster                                               |
| xml_etree_generate        | 97.9 ms                                                                | 89.8 ms: 1.09x faster                                              |
| bpe_tokeniser             | 4.36 sec                                                               | 4.03 sec: 1.08x faster                                             |
| pprint_pformat            | 1.61 sec                                                               | 1.49 sec: 1.08x faster                                             |
| deepcopy_memo             | 30.6 us                                                                | 28.5 us: 1.07x faster                                              |
| scimark_sor               | 122 ms                                                                 | 114 ms: 1.07x faster                                               |
| tomli_loads               | 2.31 sec                                                               | 2.17 sec: 1.06x faster                                             |
| pickle_pure_python        | 334 us                                                                 | 314 us: 1.06x faster                                               |
| mako                      | 15.9 ms                                                                | 14.9 ms: 1.06x faster                                              |
| pidigits                  | 211 ms                                                                 | 199 ms: 1.06x faster                                               |
| json_dumps                | 11.3 ms                                                                | 10.7 ms: 1.05x faster                                              |
| chaos                     | 62.4 ms                                                                | 59.5 ms: 1.05x faster                                              |
| scimark_lu                | 131 ms                                                                 | 125 ms: 1.05x faster                                               |
| sqlite_synth              | 2.09 us                                                                | 2.01 us: 1.04x faster                                              |
| crypto_pyaes              | 86.7 ms                                                                | 83.6 ms: 1.04x faster                                              |
| comprehensions            | 18.8 us                                                                | 18.2 us: 1.03x faster                                              |
| meteor_contest            | 123 ms                                                                 | 119 ms: 1.03x faster                                               |
| json                      | 5.54 ms                                                                | 5.39 ms: 1.03x faster                                              |
| sqlglot_v2_parse          | 1.45 ms                                                                | 1.42 ms: 1.02x faster                                              |
| thrift                    | 895 us                                                                 | 875 us: 1.02x faster                                               |
| django_template           | 41.2 ms                                                                | 40.3 ms: 1.02x faster                                              |
| connected_components      | 482 ms                                                                 | 473 ms: 1.02x faster                                               |
| shortest_path             | 530 ms                                                                 | 522 ms: 1.01x faster                                               |
| k_core                    | 2.21 sec                                                               | 2.18 sec: 1.01x faster                                             |
| deepcopy_reduce           | 2.97 us                                                                | 2.95 us: 1.01x faster                                              |
| regex_effbot              | 2.90 ms                                                                | 2.88 ms: 1.01x faster                                              |
| xml_etree_iterparse       | 87.5 ms                                                                | 87.0 ms: 1.01x faster                                              |
| regex_dna                 | 177 ms                                                                 | 176 ms: 1.00x faster                                               |
| regex_compile             | 143 ms                                                                 | 144 ms: 1.01x slower                                               |
| python_startup            | 15.9 ms                                                                | 16.0 ms: 1.01x slower                                              |
| raytrace                  | 300 ms                                                                 | 302 ms: 1.01x slower                                               |
| python_startup_no_site    | 9.54 ms                                                                | 9.63 ms: 1.01x slower                                              |
| telco                     | 177 ms                                                                 | 179 ms: 1.01x slower                                               |
| genshi_text               | 27.3 ms                                                                | 27.6 ms: 1.01x slower                                              |
| many_optionals            | 1.04 ms                                                                | 1.05 ms: 1.01x slower                                              |
| coroutines                | 24.0 ms                                                                | 24.4 ms: 1.02x slower                                              |
| 2to3                      | 276 ms                                                                 | 281 ms: 1.02x slower                                               |
| typing_runtime_protocols  | 192 us                                                                 | 196 us: 1.02x slower                                               |
| logging_simple            | 6.86 us                                                                | 7.00 us: 1.02x slower                                              |
| async_tree_memoization_tg | 324 ms                                                                 | 331 ms: 1.02x slower                                               |
| async_tree_none_tg        | 263 ms                                                                 | 269 ms: 1.02x slower                                               |
| async_tree_none           | 284 ms                                                                 | 291 ms: 1.02x slower                                               |
| deepcopy                  | 276 us                                                                 | 283 us: 1.03x slower                                               |
| create_gc_cycles          | 1.45 ms                                                                | 1.49 ms: 1.03x slower                                              |
| async_tree_io             | 618 ms                                                                 | 635 ms: 1.03x slower                                               |
| gc_traversal              | 1.89 ms                                                                | 1.94 ms: 1.03x slower                                              |
| nqueens                   | 92.7 ms                                                                | 95.9 ms: 1.03x slower                                              |
| pathlib                   | 17.7 ms                                                                | 18.3 ms: 1.03x slower                                              |
| sphinx                    | 1.07 sec                                                               | 1.10 sec: 1.04x slower                                             |
| hexiom                    | 6.46 ms                                                                | 6.72 ms: 1.04x slower                                              |
| async_tree_io_tg          | 590 ms                                                                 | 615 ms: 1.04x slower                                               |
| docutils                  | 2.77 sec                                                               | 2.88 sec: 1.04x slower                                             |
| sympy_integrate           | 21.8 ms                                                                | 23.0 ms: 1.05x slower                                              |
| sqlglot_v2_optimize       | 59.5 ms                                                                | 63.0 ms: 1.06x slower                                              |
| html5lib                  | 66.0 ms                                                                | 70.6 ms: 1.07x slower                                              |
| async_generators          | 371 ms                                                                 | 399 ms: 1.07x slower                                               |
| pylint                    | 306 ms                                                                 | 329 ms: 1.08x slower                                               |
| generators                | 29.6 ms                                                                | 31.9 ms: 1.08x slower                                              |
| sqlglot_v2_normalize      | 118 ms                                                                 | 127 ms: 1.08x slower                                               |
| sympy_sum                 | 178 ms                                                                 | 193 ms: 1.09x slower                                               |
| sympy_expand              | 525 ms                                                                 | 575 ms: 1.09x slower                                               |
| dulwich_log               | 70.0 ms                                                                | 77.3 ms: 1.10x slower                                              |
| sympy_str                 | 312 ms                                                                 | 354 ms: 1.13x slower                                               |
| mdp                       | 1.33 sec                                                               | 1.55 sec: 1.16x slower                                             |
| genshi_xml                | 57.7 ms                                                                | 68.8 ms: 1.19x slower                                              |
| Geometric mean            | (ref)                                                                  | 1.03x faster                                                       |

Benchmark hidden because not significant (15): sqlglot_v2_transpile, coverage, subparsers, xml_etree_parse, json_loads, async_tree_cpu_io_mixed, asyncio_websockets, bench_mp_pool, regex_v8, async_tree_cpu_io_mixed_tg, pycparser, logging_format, bench_thread_pool, scimark_sparse_mat_mult, async_tree_memoization

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 51.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x