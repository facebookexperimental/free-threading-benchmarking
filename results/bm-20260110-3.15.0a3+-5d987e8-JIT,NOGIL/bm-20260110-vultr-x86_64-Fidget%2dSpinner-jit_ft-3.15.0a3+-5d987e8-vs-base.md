# Results vs. base

- fork: Fidget-Spinner
- ref: jit_ft
- machine: linux-x86_64
- commit hash: 5d987e8
- commit date: 2026-01-10
- overall geometric mean: 1.049x faster
- HPT reliability: 99.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 280 ms                                                                 | 278 ms: 1.01x faster                                               |
| docutils       | 2.75 sec                                                               | 2.90 sec: 1.05x slower                                             |
| html5lib       | 65.6 ms                                                                | 69.9 ms: 1.07x slower                                              |
| sphinx         | 1.06 sec                                                               | 1.07 sec: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| coroutines                 | 23.9 ms                                                                | 23.6 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed    | 541 ms                                                                 | 548 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed_tg | 516 ms                                                                 | 528 ms: 1.02x slower                                               |
| async_generators           | 374 ms                                                                 | 394 ms: 1.05x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (7): async_tree_none, async_tree_io_tg, async_tree_io, async_tree_memoization, asyncio_websockets, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| nbody          | 126 ms                                                                 | 91.9 ms: 1.37x faster                                              |
| float          | 73.6 ms                                                                | 55.4 ms: 1.33x faster                                              |
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                               |
| Geometric mean | (ref)                                                                  | 1.27x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.06 ms                                                                | 2.78 ms: 1.10x faster                                              |
| regex_dna      | 181 ms                                                                 | 174 ms: 1.04x faster                                               |
| regex_v8       | 21.6 ms                                                                | 20.9 ms: 1.04x faster                                              |
| regex_compile  | 142 ms                                                                 | 143 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| unpickle_pure_python | 238 us                                                                 | 200 us: 1.19x faster                                               |
| xml_etree_process    | 70.1 ms                                                                | 63.7 ms: 1.10x faster                                              |
| xml_etree_generate   | 97.1 ms                                                                | 89.7 ms: 1.08x faster                                              |
| pickle_pure_python   | 335 us                                                                 | 311 us: 1.08x faster                                               |
| tomli_loads          | 1.98 sec                                                               | 1.87 sec: 1.06x faster                                             |
| json_dumps           | 11.0 ms                                                                | 10.5 ms: 1.04x faster                                              |
| xml_etree_iterparse  | 89.1 ms                                                                | 87.3 ms: 1.02x faster                                              |
| json_loads           | 31.3 us                                                                | 32.2 us: 1.03x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.06x faster                                                       |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| mako           | 16.1 ms                                                                | 14.5 ms: 1.11x faster                                              |
| genshi_text    | 27.1 ms                                                                | 28.3 ms: 1.04x slower                                              |
| genshi_xml     | 57.2 ms                                                                | 68.2 ms: 1.19x slower                                              |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                       |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20260109-vultr-x86_64-python-95259116ecb4346b570b-3.15.0a3+-9525911 | bm-20260110-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| richards                   | 52.4 ms                                                                | 20.1 ms: 2.60x faster                                              |
| richards_super             | 60.0 ms                                                                | 25.1 ms: 2.39x faster                                              |
| nbody                      | 126 ms                                                                 | 91.9 ms: 1.37x faster                                              |
| float                      | 73.6 ms                                                                | 55.4 ms: 1.33x faster                                              |
| logging_silent             | 101 ns                                                                 | 83.0 ns: 1.21x faster                                              |
| pyflate                    | 467 ms                                                                 | 385 ms: 1.21x faster                                               |
| scimark_fft                | 351 ms                                                                 | 293 ms: 1.20x faster                                               |
| unpickle_pure_python       | 238 us                                                                 | 200 us: 1.19x faster                                               |
| scimark_monte_carlo        | 78.8 ms                                                                | 66.5 ms: 1.18x faster                                              |
| deltablue                  | 3.60 ms                                                                | 3.07 ms: 1.17x faster                                              |
| go                         | 120 ms                                                                 | 104 ms: 1.15x faster                                               |
| spectral_norm              | 112 ms                                                                 | 98.8 ms: 1.14x faster                                              |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                               |
| fannkuch                   | 458 ms                                                                 | 408 ms: 1.12x faster                                               |
| scimark_lu                 | 131 ms                                                                 | 118 ms: 1.11x faster                                               |
| mako                       | 16.1 ms                                                                | 14.5 ms: 1.11x faster                                              |
| pprint_safe_repr           | 772 ms                                                                 | 700 ms: 1.10x faster                                               |
| regex_effbot               | 3.06 ms                                                                | 2.78 ms: 1.10x faster                                              |
| xml_etree_process          | 70.1 ms                                                                | 63.7 ms: 1.10x faster                                              |
| deepcopy_memo              | 30.6 us                                                                | 27.9 us: 1.10x faster                                              |
| bpe_tokeniser              | 4.44 sec                                                               | 4.07 sec: 1.09x faster                                             |
| xml_etree_generate         | 97.1 ms                                                                | 89.7 ms: 1.08x faster                                              |
| pickle_pure_python         | 335 us                                                                 | 311 us: 1.08x faster                                               |
| pprint_pformat             | 1.59 sec                                                               | 1.49 sec: 1.07x faster                                             |
| chaos                      | 63.5 ms                                                                | 59.4 ms: 1.07x faster                                              |
| tomli_loads                | 1.98 sec                                                               | 1.87 sec: 1.06x faster                                             |
| crypto_pyaes               | 87.1 ms                                                                | 82.5 ms: 1.06x faster                                              |
| meteor_contest             | 125 ms                                                                 | 119 ms: 1.06x faster                                               |
| sqlglot_v2_parse           | 1.45 ms                                                                | 1.37 ms: 1.05x faster                                              |
| scimark_sparse_mat_mult    | 5.66 ms                                                                | 5.38 ms: 1.05x faster                                              |
| subparsers                 | 10.4 ms                                                                | 9.87 ms: 1.05x faster                                              |
| deepcopy_reduce            | 2.91 us                                                                | 2.78 us: 1.05x faster                                              |
| json_dumps                 | 11.0 ms                                                                | 10.5 ms: 1.04x faster                                              |
| scimark_sor                | 121 ms                                                                 | 116 ms: 1.04x faster                                               |
| regex_dna                  | 181 ms                                                                 | 174 ms: 1.04x faster                                               |
| regex_v8                   | 21.6 ms                                                                | 20.9 ms: 1.04x faster                                              |
| comprehensions             | 18.7 us                                                                | 18.1 us: 1.03x faster                                              |
| sqlglot_v2_transpile       | 1.78 ms                                                                | 1.72 ms: 1.03x faster                                              |
| deepcopy                   | 269 us                                                                 | 261 us: 1.03x faster                                               |
| create_gc_cycles           | 1.51 ms                                                                | 1.47 ms: 1.03x faster                                              |
| k_core                     | 2.21 sec                                                               | 2.16 sec: 1.03x faster                                             |
| sqlite_synth               | 2.07 us                                                                | 2.02 us: 1.02x faster                                              |
| xml_etree_iterparse        | 89.1 ms                                                                | 87.3 ms: 1.02x faster                                              |
| thrift                     | 899 us                                                                 | 881 us: 1.02x faster                                               |
| connected_components       | 483 ms                                                                 | 474 ms: 1.02x faster                                               |
| gc_traversal               | 1.93 ms                                                                | 1.90 ms: 1.02x faster                                              |
| coroutines                 | 23.9 ms                                                                | 23.6 ms: 1.01x faster                                              |
| shortest_path              | 537 ms                                                                 | 531 ms: 1.01x faster                                               |
| 2to3                       | 280 ms                                                                 | 278 ms: 1.01x faster                                               |
| bench_thread_pool          | 1.47 ms                                                                | 1.47 ms: 1.01x faster                                              |
| regex_compile              | 142 ms                                                                 | 143 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed    | 541 ms                                                                 | 548 ms: 1.01x slower                                               |
| sphinx                     | 1.06 sec                                                               | 1.07 sec: 1.01x slower                                             |
| many_optionals             | 1.03 ms                                                                | 1.05 ms: 1.02x slower                                              |
| async_tree_cpu_io_mixed_tg | 516 ms                                                                 | 528 ms: 1.02x slower                                               |
| raytrace                   | 300 ms                                                                 | 307 ms: 1.02x slower                                               |
| telco                      | 176 ms                                                                 | 180 ms: 1.03x slower                                               |
| generators                 | 32.8 ms                                                                | 33.7 ms: 1.03x slower                                              |
| json_loads                 | 31.3 us                                                                | 32.2 us: 1.03x slower                                              |
| sympy_integrate            | 22.0 ms                                                                | 23.0 ms: 1.04x slower                                              |
| genshi_text                | 27.1 ms                                                                | 28.3 ms: 1.04x slower                                              |
| sqlglot_v2_optimize        | 59.7 ms                                                                | 62.4 ms: 1.05x slower                                              |
| sqlglot_v2_normalize       | 117 ms                                                                 | 123 ms: 1.05x slower                                               |
| async_generators           | 374 ms                                                                 | 394 ms: 1.05x slower                                               |
| docutils                   | 2.75 sec                                                               | 2.90 sec: 1.05x slower                                             |
| hexiom                     | 6.58 ms                                                                | 6.96 ms: 1.06x slower                                              |
| pylint                     | 305 ms                                                                 | 324 ms: 1.06x slower                                               |
| html5lib                   | 65.6 ms                                                                | 69.9 ms: 1.07x slower                                              |
| dulwich_log                | 69.9 ms                                                                | 74.6 ms: 1.07x slower                                              |
| sympy_sum                  | 180 ms                                                                 | 193 ms: 1.07x slower                                               |
| sympy_expand               | 526 ms                                                                 | 578 ms: 1.10x slower                                               |
| sympy_str                  | 315 ms                                                                 | 356 ms: 1.13x slower                                               |
| mdp                        | 1.36 sec                                                               | 1.57 sec: 1.16x slower                                             |
| genshi_xml                 | 57.2 ms                                                                | 68.2 ms: 1.19x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                       |

Benchmark hidden because not significant (20): async_tree_none, async_tree_io_tg, async_tree_io, json, async_tree_memoization, pycparser, nqueens, django_template, coverage, xml_etree_parse, pathlib, asyncio_websockets, python_startup, python_startup_no_site, async_tree_none_tg, async_tree_memoization_tg, bench_mp_pool, logging_format, typing_runtime_protocols, logging_simple

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 99.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x