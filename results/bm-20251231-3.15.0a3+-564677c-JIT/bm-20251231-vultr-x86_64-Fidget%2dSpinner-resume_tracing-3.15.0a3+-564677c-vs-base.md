# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 564677c
- commit date: 2025-12-31
- overall geometric mean: 1.002x faster
- HPT reliability: 71.13%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 245 ms: 1.01x faster                                                       |
| docutils       | 2.69 sec                                                               | 2.61 sec: 1.03x faster                                                     |
| html5lib       | 64.6 ms                                                                | 63.2 ms: 1.02x faster                                                      |
| sphinx         | 1.01 sec                                                               | 971 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 306 ms                                                                 | 288 ms: 1.06x faster                                                       |
| async_tree_memoization     | 302 ms                                                                 | 289 ms: 1.05x faster                                                       |
| async_tree_none_tg         | 242 ms                                                                 | 231 ms: 1.05x faster                                                       |
| async_tree_none            | 240 ms                                                                 | 232 ms: 1.03x faster                                                       |
| async_tree_io              | 548 ms                                                                 | 532 ms: 1.03x faster                                                       |
| async_tree_io_tg           | 586 ms                                                                 | 570 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 474 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed    | 485 ms                                                                 | 474 ms: 1.02x faster                                                       |
| coroutines                 | 23.9 ms                                                                | 24.3 ms: 1.02x slower                                                      |
| async_generators           | 355 ms                                                                 | 365 ms: 1.03x slower                                                       |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 203 ms                                                                 | 203 ms: 1.00x slower                                                       |
| nbody          | 73.8 ms                                                                | 75.8 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 2.74 ms                                                                | 2.69 ms: 1.02x faster                                                      |
| regex_v8       | 22.0 ms                                                                | 21.7 ms: 1.01x faster                                                      |
| regex_dna      | 168 ms                                                                 | 173 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_process    | 55.2 ms                                                                | 53.3 ms: 1.04x faster                                                      |
| unpickle_pure_python | 179 us                                                                 | 175 us: 1.03x faster                                                       |
| xml_etree_iterparse  | 83.5 ms                                                                | 83.0 ms: 1.01x faster                                                      |
| json_loads           | 27.9 us                                                                | 28.0 us: 1.00x slower                                                      |
| xml_etree_generate   | 78.0 ms                                                                | 78.5 ms: 1.01x slower                                                      |
| tomli_loads          | 1.95 sec                                                               | 1.97 sec: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                                | 7.36 ms: 1.00x slower                                                      |
| python_startup         | 12.5 ms                                                                | 12.6 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 35.5 ms                                                                | 33.8 ms: 1.05x faster                                                      |
| mako            | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                                      |
| genshi_text     | 20.9 ms                                                                | 21.1 ms: 1.01x slower                                                      |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| bench_mp_pool              | 242 ms                                                                 | 203 ms: 1.19x faster                                                       |
| telco                      | 161 ms                                                                 | 145 ms: 1.11x faster                                                       |
| typing_runtime_protocols   | 159 us                                                                 | 148 us: 1.08x faster                                                       |
| async_tree_memoization_tg  | 306 ms                                                                 | 288 ms: 1.06x faster                                                       |
| dulwich_log                | 74.1 ms                                                                | 69.8 ms: 1.06x faster                                                      |
| django_template            | 35.5 ms                                                                | 33.8 ms: 1.05x faster                                                      |
| async_tree_memoization     | 302 ms                                                                 | 289 ms: 1.05x faster                                                       |
| async_tree_none_tg         | 242 ms                                                                 | 231 ms: 1.05x faster                                                       |
| deltablue                  | 2.66 ms                                                                | 2.54 ms: 1.05x faster                                                      |
| sphinx                     | 1.01 sec                                                               | 971 ms: 1.04x faster                                                       |
| chaos                      | 52.0 ms                                                                | 50.1 ms: 1.04x faster                                                      |
| xml_etree_process          | 55.2 ms                                                                | 53.3 ms: 1.04x faster                                                      |
| async_tree_none            | 240 ms                                                                 | 232 ms: 1.03x faster                                                       |
| sqlite_synth               | 2.25 us                                                                | 2.18 us: 1.03x faster                                                      |
| logging_simple             | 5.84 us                                                                | 5.66 us: 1.03x faster                                                      |
| deepcopy_reduce            | 2.58 us                                                                | 2.51 us: 1.03x faster                                                      |
| async_tree_io              | 548 ms                                                                 | 532 ms: 1.03x faster                                                       |
| pprint_safe_repr           | 659 ms                                                                 | 641 ms: 1.03x faster                                                       |
| docutils                   | 2.69 sec                                                               | 2.61 sec: 1.03x faster                                                     |
| scimark_sor                | 101 ms                                                                 | 97.8 ms: 1.03x faster                                                      |
| async_tree_io_tg           | 586 ms                                                                 | 570 ms: 1.03x faster                                                       |
| unpickle_pure_python       | 179 us                                                                 | 175 us: 1.03x faster                                                       |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 474 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed    | 485 ms                                                                 | 474 ms: 1.02x faster                                                       |
| html5lib                   | 64.6 ms                                                                | 63.2 ms: 1.02x faster                                                      |
| generators                 | 28.8 ms                                                                | 28.2 ms: 1.02x faster                                                      |
| scimark_monte_carlo        | 52.5 ms                                                                | 51.5 ms: 1.02x faster                                                      |
| regex_effbot               | 2.74 ms                                                                | 2.69 ms: 1.02x faster                                                      |
| richards_super             | 21.8 ms                                                                | 21.5 ms: 1.02x faster                                                      |
| logging_format             | 6.51 us                                                                | 6.41 us: 1.01x faster                                                      |
| regex_v8                   | 22.0 ms                                                                | 21.7 ms: 1.01x faster                                                      |
| connected_components       | 384 ms                                                                 | 378 ms: 1.01x faster                                                       |
| raytrace                   | 261 ms                                                                 | 258 ms: 1.01x faster                                                       |
| sqlglot_v2_normalize       | 110 ms                                                                 | 109 ms: 1.01x faster                                                       |
| 2to3                       | 248 ms                                                                 | 245 ms: 1.01x faster                                                       |
| json                       | 4.91 ms                                                                | 4.87 ms: 1.01x faster                                                      |
| coverage                   | 81.2 ms                                                                | 80.7 ms: 1.01x faster                                                      |
| k_core                     | 1.86 sec                                                               | 1.85 sec: 1.01x faster                                                     |
| xml_etree_iterparse        | 83.5 ms                                                                | 83.0 ms: 1.01x faster                                                      |
| mako                       | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                                      |
| python_startup_no_site     | 7.35 ms                                                                | 7.36 ms: 1.00x slower                                                      |
| pidigits                   | 203 ms                                                                 | 203 ms: 1.00x slower                                                       |
| shortest_path              | 424 ms                                                                 | 426 ms: 1.00x slower                                                       |
| json_loads                 | 27.9 us                                                                | 28.0 us: 1.00x slower                                                      |
| scimark_lu                 | 97.7 ms                                                                | 98.2 ms: 1.01x slower                                                      |
| fannkuch                   | 350 ms                                                                 | 352 ms: 1.01x slower                                                       |
| comprehensions             | 15.9 us                                                                | 16.0 us: 1.01x slower                                                      |
| xml_etree_generate         | 78.0 ms                                                                | 78.5 ms: 1.01x slower                                                      |
| nqueens                    | 86.3 ms                                                                | 86.9 ms: 1.01x slower                                                      |
| meteor_contest             | 97.7 ms                                                                | 98.5 ms: 1.01x slower                                                      |
| bpe_tokeniser              | 4.05 sec                                                               | 4.08 sec: 1.01x slower                                                     |
| tomli_loads                | 1.95 sec                                                               | 1.97 sec: 1.01x slower                                                     |
| scimark_fft                | 257 ms                                                                 | 259 ms: 1.01x slower                                                       |
| python_startup             | 12.5 ms                                                                | 12.6 ms: 1.01x slower                                                      |
| genshi_text                | 20.9 ms                                                                | 21.1 ms: 1.01x slower                                                      |
| many_optionals             | 996 us                                                                 | 1.01 ms: 1.01x slower                                                      |
| crypto_pyaes               | 66.2 ms                                                                | 67.1 ms: 1.01x slower                                                      |
| coroutines                 | 23.9 ms                                                                | 24.3 ms: 1.02x slower                                                      |
| scimark_sparse_mat_mult    | 4.31 ms                                                                | 4.40 ms: 1.02x slower                                                      |
| logging_silent             | 81.1 ns                                                                | 82.9 ns: 1.02x slower                                                      |
| sqlglot_v2_transpile       | 1.54 ms                                                                | 1.58 ms: 1.02x slower                                                      |
| spectral_norm              | 85.4 ms                                                                | 87.5 ms: 1.02x slower                                                      |
| regex_dna                  | 168 ms                                                                 | 173 ms: 1.03x slower                                                       |
| nbody                      | 73.8 ms                                                                | 75.8 ms: 1.03x slower                                                      |
| async_generators           | 355 ms                                                                 | 365 ms: 1.03x slower                                                       |
| hexiom                     | 6.18 ms                                                                | 6.35 ms: 1.03x slower                                                      |
| create_gc_cycles           | 1.87 ms                                                                | 1.93 ms: 1.03x slower                                                      |
| sqlglot_v2_optimize        | 54.3 ms                                                                | 56.0 ms: 1.03x slower                                                      |
| go                         | 91.9 ms                                                                | 94.9 ms: 1.03x slower                                                      |
| mdp                        | 1.38 sec                                                               | 1.43 sec: 1.04x slower                                                     |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.26 ms: 1.04x slower                                                      |
| pylint                     | 309 ms                                                                 | 323 ms: 1.05x slower                                                       |
| sympy_integrate            | 20.3 ms                                                                | 21.3 ms: 1.05x slower                                                      |
| sympy_str                  | 306 ms                                                                 | 323 ms: 1.06x slower                                                       |
| sympy_sum                  | 169 ms                                                                 | 180 ms: 1.06x slower                                                       |
| gc_traversal               | 4.28 ms                                                                | 4.56 ms: 1.07x slower                                                      |
| pycparser                  | 1.09 sec                                                               | 1.27 sec: 1.16x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (17): genshi_xml, sympy_expand, pprint_pformat, richards, deepcopy, thrift, asyncio_websockets, regex_compile, pickle_pure_python, deepcopy_memo, pathlib, xml_etree_parse, pyflate, json_dumps, bench_thread_pool, subparsers, float

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 71.13% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x