# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 01c2d73
- commit date: 2025-10-28
- overall geometric mean: 1.007x faster
- HPT reliability: 98.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 253 ms: 1.00x slower                                                    |
| docutils       | 2.59 sec                                                               | 2.74 sec: 1.06x slower                                                  |
| html5lib       | 60.6 ms                                                                | 68.5 ms: 1.13x slower                                                   |
| sphinx         | 977 ms                                                                 | 1.02 sec: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 482 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed    | 496 ms                                                                 | 488 ms: 1.02x faster                                                    |
| async_tree_io_tg           | 594 ms                                                                 | 589 ms: 1.01x faster                                                    |
| async_generators           | 361 ms                                                                 | 363 ms: 1.00x slower                                                    |
| coroutines                 | 23.8 ms                                                                | 24.2 ms: 1.01x slower                                                   |
| async_tree_none            | 245 ms                                                                 | 249 ms: 1.02x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (5): async_tree_memoization_tg, asyncio_websockets, async_tree_none_tg, async_tree_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.2 ms                                                                | 60.5 ms: 1.18x faster                                                   |
| pidigits       | 200 ms                                                                 | 193 ms: 1.04x faster                                                    |
| nbody          | 87.8 ms                                                                | 84.6 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 2.72 ms                                                                | 2.57 ms: 1.06x faster                                                   |
| regex_dna      | 178 ms                                                                 | 172 ms: 1.04x faster                                                    |
| regex_v8       | 21.9 ms                                                                | 21.4 ms: 1.02x faster                                                   |
| regex_compile  | 124 ms                                                                 | 126 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 84.3 ms                                                                | 82.8 ms: 1.02x faster                                                   |
| json_dumps           | 9.55 ms                                                                | 9.40 ms: 1.02x faster                                                   |
| pickle_pure_python   | 306 us                                                                 | 302 us: 1.01x faster                                                    |
| unpickle_pure_python | 183 us                                                                 | 184 us: 1.00x slower                                                    |
| xml_etree_process    | 53.9 ms                                                                | 54.5 ms: 1.01x slower                                                   |
| json_loads           | 27.9 us                                                                | 28.6 us: 1.02x slower                                                   |
| xml_etree_generate   | 77.2 ms                                                                | 79.6 ms: 1.03x slower                                                   |
| tomli_loads          | 1.77 sec                                                               | 1.86 sec: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.23 ms                                                                | 7.25 ms: 1.00x slower                                                   |
| python_startup         | 12.4 ms                                                                | 12.4 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 10.6 ms                                                                | 10.6 ms: 1.00x faster                                                   |
| genshi_text    | 20.4 ms                                                                | 21.3 ms: 1.04x slower                                                   |
| genshi_xml     | 47.8 ms                                                                | 54.4 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-01c2d73 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 41.1 ms                                                                | 21.4 ms: 1.92x faster                                                   |
| richards_super             | 47.0 ms                                                                | 25.4 ms: 1.85x faster                                                   |
| float                      | 71.2 ms                                                                | 60.5 ms: 1.18x faster                                                   |
| deltablue                  | 3.31 ms                                                                | 2.82 ms: 1.17x faster                                                   |
| logging_silent             | 102 ns                                                                 | 86.9 ns: 1.17x faster                                                   |
| deepcopy_memo              | 26.9 us                                                                | 23.1 us: 1.16x faster                                                   |
| spectral_norm              | 95.9 ms                                                                | 84.5 ms: 1.13x faster                                                   |
| scimark_sor                | 107 ms                                                                 | 98.5 ms: 1.09x faster                                                   |
| scimark_lu                 | 108 ms                                                                 | 101 ms: 1.07x faster                                                    |
| scimark_monte_carlo        | 61.5 ms                                                                | 57.5 ms: 1.07x faster                                                   |
| regex_effbot               | 2.72 ms                                                                | 2.57 ms: 1.06x faster                                                   |
| pyflate                    | 400 ms                                                                 | 380 ms: 1.05x faster                                                    |
| pidigits                   | 200 ms                                                                 | 193 ms: 1.04x faster                                                    |
| nbody                      | 87.8 ms                                                                | 84.6 ms: 1.04x faster                                                   |
| regex_dna                  | 178 ms                                                                 | 172 ms: 1.04x faster                                                    |
| chaos                      | 56.0 ms                                                                | 54.2 ms: 1.03x faster                                                   |
| regex_v8                   | 21.9 ms                                                                | 21.4 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 482 ms: 1.02x faster                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 153 us: 1.02x faster                                                    |
| xml_etree_iterparse        | 84.3 ms                                                                | 82.8 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed    | 496 ms                                                                 | 488 ms: 1.02x faster                                                    |
| json_dumps                 | 9.55 ms                                                                | 9.40 ms: 1.02x faster                                                   |
| scimark_sparse_mat_mult    | 4.27 ms                                                                | 4.20 ms: 1.02x faster                                                   |
| pickle_pure_python         | 306 us                                                                 | 302 us: 1.01x faster                                                    |
| deepcopy_reduce            | 2.59 us                                                                | 2.56 us: 1.01x faster                                                   |
| async_tree_io_tg           | 594 ms                                                                 | 589 ms: 1.01x faster                                                    |
| mako                       | 10.6 ms                                                                | 10.6 ms: 1.00x faster                                                   |
| 2to3                       | 253 ms                                                                 | 253 ms: 1.00x slower                                                    |
| python_startup_no_site     | 7.23 ms                                                                | 7.25 ms: 1.00x slower                                                   |
| unpickle_pure_python       | 183 us                                                                 | 184 us: 1.00x slower                                                    |
| bench_thread_pool          | 1.01 ms                                                                | 1.01 ms: 1.00x slower                                                   |
| async_generators           | 361 ms                                                                 | 363 ms: 1.00x slower                                                    |
| bench_mp_pool              | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| create_gc_cycles           | 1.92 ms                                                                | 1.93 ms: 1.01x slower                                                   |
| python_startup             | 12.4 ms                                                                | 12.4 ms: 1.01x slower                                                   |
| shortest_path              | 434 ms                                                                 | 437 ms: 1.01x slower                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.52 ms: 1.01x slower                                                   |
| comprehensions             | 15.8 us                                                                | 16.0 us: 1.01x slower                                                   |
| k_core                     | 1.87 sec                                                               | 1.89 sec: 1.01x slower                                                  |
| sqlglot_v2_parse           | 1.20 ms                                                                | 1.21 ms: 1.01x slower                                                   |
| connected_components       | 390 ms                                                                 | 394 ms: 1.01x slower                                                    |
| logging_simple             | 5.75 us                                                                | 5.82 us: 1.01x slower                                                   |
| xml_etree_process          | 53.9 ms                                                                | 54.5 ms: 1.01x slower                                                   |
| subparsers                 | 44.9 ms                                                                | 45.5 ms: 1.01x slower                                                   |
| coroutines                 | 23.8 ms                                                                | 24.2 ms: 1.01x slower                                                   |
| regex_compile              | 124 ms                                                                 | 126 ms: 1.01x slower                                                    |
| scimark_fft                | 257 ms                                                                 | 261 ms: 1.02x slower                                                    |
| async_tree_none            | 245 ms                                                                 | 249 ms: 1.02x slower                                                    |
| bpe_tokeniser              | 3.96 sec                                                               | 4.03 sec: 1.02x slower                                                  |
| pathlib                    | 17.8 ms                                                                | 18.2 ms: 1.02x slower                                                   |
| fannkuch                   | 362 ms                                                                 | 370 ms: 1.02x slower                                                    |
| sympy_expand               | 491 ms                                                                 | 501 ms: 1.02x slower                                                    |
| generators                 | 27.7 ms                                                                | 28.3 ms: 1.02x slower                                                   |
| json_loads                 | 27.9 us                                                                | 28.6 us: 1.02x slower                                                   |
| deepcopy                   | 244 us                                                                 | 251 us: 1.03x slower                                                    |
| xml_etree_generate         | 77.2 ms                                                                | 79.6 ms: 1.03x slower                                                   |
| sqlglot_v2_optimize        | 51.3 ms                                                                | 53.3 ms: 1.04x slower                                                   |
| sphinx                     | 977 ms                                                                 | 1.02 sec: 1.04x slower                                                  |
| pprint_safe_repr           | 682 ms                                                                 | 710 ms: 1.04x slower                                                    |
| sympy_integrate            | 19.3 ms                                                                | 20.2 ms: 1.04x slower                                                   |
| genshi_text                | 20.4 ms                                                                | 21.3 ms: 1.04x slower                                                   |
| many_optionals             | 1.25 ms                                                                | 1.31 ms: 1.05x slower                                                   |
| dulwich_log                | 69.2 ms                                                                | 72.4 ms: 1.05x slower                                                   |
| sqlglot_v2_normalize       | 102 ms                                                                 | 107 ms: 1.05x slower                                                    |
| telco                      | 156 ms                                                                 | 164 ms: 1.05x slower                                                    |
| tomli_loads                | 1.77 sec                                                               | 1.86 sec: 1.05x slower                                                  |
| docutils                   | 2.59 sec                                                               | 2.74 sec: 1.06x slower                                                  |
| gc_traversal               | 4.30 ms                                                                | 4.55 ms: 1.06x slower                                                   |
| pycparser                  | 1.09 sec                                                               | 1.15 sec: 1.06x slower                                                  |
| thrift                     | 742 us                                                                 | 788 us: 1.06x slower                                                    |
| sympy_sum                  | 156 ms                                                                 | 167 ms: 1.07x slower                                                    |
| raytrace                   | 252 ms                                                                 | 271 ms: 1.08x slower                                                    |
| hexiom                     | 5.81 ms                                                                | 6.25 ms: 1.08x slower                                                   |
| pylint                     | 289 ms                                                                 | 312 ms: 1.08x slower                                                    |
| sympy_str                  | 281 ms                                                                 | 304 ms: 1.08x slower                                                    |
| nqueens                    | 78.6 ms                                                                | 85.5 ms: 1.09x slower                                                   |
| go                         | 105 ms                                                                 | 119 ms: 1.13x slower                                                    |
| html5lib                   | 60.6 ms                                                                | 68.5 ms: 1.13x slower                                                   |
| genshi_xml                 | 47.8 ms                                                                | 54.4 ms: 1.14x slower                                                   |
| mdp                        | 1.16 sec                                                               | 1.34 sec: 1.15x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (14): crypto_pyaes, async_tree_memoization_tg, coverage, pprint_pformat, meteor_contest, xml_etree_parse, asyncio_websockets, async_tree_none_tg, async_tree_io, async_tree_memoization, sqlite_synth, json, django_template, logging_format

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 98.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x