# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 2e9b980
- commit date: 2026-03-15
- overall geometric mean: 1.005x faster
- HPT reliability: 72.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| html5lib       | 62.2 ms                                                                | 60.9 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_generators           | 391 ms                                                                 | 354 ms: 1.10x faster                                                       |
| coroutines                 | 23.7 ms                                                                | 22.1 ms: 1.07x faster                                                      |
| async_tree_memoization     | 300 ms                                                                 | 284 ms: 1.06x faster                                                       |
| async_tree_none            | 239 ms                                                                 | 232 ms: 1.03x faster                                                       |
| async_tree_io              | 580 ms                                                                 | 567 ms: 1.02x faster                                                       |
| async_tree_io_tg           | 561 ms                                                                 | 551 ms: 1.02x faster                                                       |
| async_tree_memoization_tg  | 298 ms                                                                 | 294 ms: 1.01x faster                                                       |
| async_tree_cpu_io_mixed    | 497 ms                                                                 | 492 ms: 1.01x faster                                                       |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                 | 502 ms: 1.01x faster                                                       |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (2): async_tree_none_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 204 ms                                                                 | 208 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_v8       | 23.5 ms                                                                | 20.9 ms: 1.13x faster                                                      |
| regex_dna      | 183 ms                                                                 | 168 ms: 1.09x faster                                                       |
| regex_effbot   | 2.76 ms                                                                | 2.71 ms: 1.02x faster                                                      |
| regex_compile  | 125 ms                                                                 | 124 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|---------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_loads          | 27.6 us                                                                | 26.9 us: 1.03x faster                                                      |
| xml_etree_process   | 54.2 ms                                                                | 53.1 ms: 1.02x faster                                                      |
| tomli_loads         | 1.53 sec                                                               | 1.51 sec: 1.01x faster                                                     |
| xml_etree_iterparse | 83.6 ms                                                                | 83.3 ms: 1.00x faster                                                      |
| xml_etree_generate  | 77.2 ms                                                                | 79.8 ms: 1.03x slower                                                      |
| json_dumps          | 8.95 ms                                                                | 9.32 ms: 1.04x slower                                                      |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (3): pickle_pure_python, unpickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.48 ms                                                                | 7.52 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 35.0 ms                                                                | 31.9 ms: 1.10x faster                                                      |
| genshi_text     | 20.2 ms                                                                | 20.7 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_v8                   | 23.5 ms                                                                | 20.9 ms: 1.13x faster                                                      |
| async_generators           | 391 ms                                                                 | 354 ms: 1.10x faster                                                       |
| django_template            | 35.0 ms                                                                | 31.9 ms: 1.10x faster                                                      |
| logging_simple             | 5.75 us                                                                | 5.25 us: 1.09x faster                                                      |
| regex_dna                  | 183 ms                                                                 | 168 ms: 1.09x faster                                                       |
| coroutines                 | 23.7 ms                                                                | 22.1 ms: 1.07x faster                                                      |
| logging_format             | 6.46 us                                                                | 6.06 us: 1.07x faster                                                      |
| typing_runtime_protocols   | 161 us                                                                 | 151 us: 1.06x faster                                                       |
| async_tree_memoization     | 300 ms                                                                 | 284 ms: 1.06x faster                                                       |
| sqlglot_v2_normalize       | 104 ms                                                                 | 99.5 ms: 1.05x faster                                                      |
| async_tree_none            | 239 ms                                                                 | 232 ms: 1.03x faster                                                       |
| json_loads                 | 27.6 us                                                                | 26.9 us: 1.03x faster                                                      |
| telco                      | 159 ms                                                                 | 155 ms: 1.02x faster                                                       |
| pprint_pformat             | 1.32 sec                                                               | 1.29 sec: 1.02x faster                                                     |
| async_tree_io              | 580 ms                                                                 | 567 ms: 1.02x faster                                                       |
| html5lib                   | 62.2 ms                                                                | 60.9 ms: 1.02x faster                                                      |
| deltablue                  | 2.72 ms                                                                | 2.66 ms: 1.02x faster                                                      |
| meteor_contest             | 99.5 ms                                                                | 97.4 ms: 1.02x faster                                                      |
| regex_effbot               | 2.76 ms                                                                | 2.71 ms: 1.02x faster                                                      |
| xml_etree_process          | 54.2 ms                                                                | 53.1 ms: 1.02x faster                                                      |
| create_gc_cycles           | 1.87 ms                                                                | 1.83 ms: 1.02x faster                                                      |
| scimark_sor                | 85.1 ms                                                                | 83.6 ms: 1.02x faster                                                      |
| async_tree_io_tg           | 561 ms                                                                 | 551 ms: 1.02x faster                                                       |
| sympy_expand               | 491 ms                                                                 | 482 ms: 1.02x faster                                                       |
| thrift                     | 793 us                                                                 | 779 us: 1.02x faster                                                       |
| nqueens                    | 73.7 ms                                                                | 72.7 ms: 1.01x faster                                                      |
| async_tree_memoization_tg  | 298 ms                                                                 | 294 ms: 1.01x faster                                                       |
| tomli_loads                | 1.53 sec                                                               | 1.51 sec: 1.01x faster                                                     |
| json                       | 4.90 ms                                                                | 4.84 ms: 1.01x faster                                                      |
| deepcopy_reduce            | 2.38 us                                                                | 2.35 us: 1.01x faster                                                      |
| async_tree_cpu_io_mixed    | 497 ms                                                                 | 492 ms: 1.01x faster                                                       |
| sqlglot_v2_optimize        | 51.4 ms                                                                | 51.0 ms: 1.01x faster                                                      |
| deepcopy_memo              | 22.6 us                                                                | 22.4 us: 1.01x faster                                                      |
| hexiom                     | 5.86 ms                                                                | 5.81 ms: 1.01x faster                                                      |
| regex_compile              | 125 ms                                                                 | 124 ms: 1.01x faster                                                       |
| scimark_monte_carlo        | 52.0 ms                                                                | 51.7 ms: 1.01x faster                                                      |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                 | 502 ms: 1.01x faster                                                       |
| xml_etree_iterparse        | 83.6 ms                                                                | 83.3 ms: 1.00x faster                                                      |
| scimark_lu                 | 79.6 ms                                                                | 79.8 ms: 1.00x slower                                                      |
| mdp                        | 1.20 sec                                                               | 1.21 sec: 1.00x slower                                                     |
| python_startup_no_site     | 7.48 ms                                                                | 7.52 ms: 1.01x slower                                                      |
| bpe_tokeniser              | 3.92 sec                                                               | 3.94 sec: 1.01x slower                                                     |
| comprehensions             | 14.8 us                                                                | 14.9 us: 1.01x slower                                                      |
| k_core                     | 1.84 sec                                                               | 1.86 sec: 1.01x slower                                                     |
| logging_silent             | 80.1 ns                                                                | 80.6 ns: 1.01x slower                                                      |
| crypto_pyaes               | 65.6 ms                                                                | 66.0 ms: 1.01x slower                                                      |
| connected_components       | 373 ms                                                                 | 375 ms: 1.01x slower                                                       |
| coverage                   | 82.0 ms                                                                | 82.6 ms: 1.01x slower                                                      |
| gc_traversal               | 4.23 ms                                                                | 4.27 ms: 1.01x slower                                                      |
| sympy_str                  | 289 ms                                                                 | 292 ms: 1.01x slower                                                       |
| sqlite_synth               | 2.14 us                                                                | 2.16 us: 1.01x slower                                                      |
| bench_thread_pool          | 1.31 ms                                                                | 1.32 ms: 1.01x slower                                                      |
| sqlglot_v2_transpile       | 1.47 ms                                                                | 1.50 ms: 1.02x slower                                                      |
| sympy_integrate            | 19.7 ms                                                                | 20.1 ms: 1.02x slower                                                      |
| pidigits                   | 204 ms                                                                 | 208 ms: 1.02x slower                                                       |
| spectral_norm              | 76.8 ms                                                                | 78.7 ms: 1.02x slower                                                      |
| fannkuch                   | 338 ms                                                                 | 347 ms: 1.03x slower                                                       |
| sqlglot_v2_parse           | 1.17 ms                                                                | 1.20 ms: 1.03x slower                                                      |
| richards_super             | 21.5 ms                                                                | 22.1 ms: 1.03x slower                                                      |
| genshi_text                | 20.2 ms                                                                | 20.7 ms: 1.03x slower                                                      |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 4.38 ms: 1.03x slower                                                      |
| go                         | 99.7 ms                                                                | 103 ms: 1.03x slower                                                       |
| sympy_sum                  | 164 ms                                                                 | 168 ms: 1.03x slower                                                       |
| xml_etree_generate         | 77.2 ms                                                                | 79.8 ms: 1.03x slower                                                      |
| pylint                     | 291 ms                                                                 | 302 ms: 1.04x slower                                                       |
| richards                   | 17.7 ms                                                                | 18.3 ms: 1.04x slower                                                      |
| json_dumps                 | 8.95 ms                                                                | 9.32 ms: 1.04x slower                                                      |
| raytrace                   | 277 ms                                                                 | 297 ms: 1.07x slower                                                       |
| pycparser                  | 1.08 sec                                                               | 1.17 sec: 1.08x slower                                                     |
| generators                 | 29.0 ms                                                                | 35.3 ms: 1.22x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (24): bench_mp_pool, async_tree_none_tg, chaos, sphinx, deepcopy, mako, subparsers, pathlib, python_startup, pprint_safe_repr, asyncio_websockets, shortest_path, scimark_fft, docutils, pyflate, nbody, pickle_pure_python, 2to3, unpickle_pure_python, xml_etree_parse, many_optionals, dulwich_log, genshi_xml, float

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 72.22% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x