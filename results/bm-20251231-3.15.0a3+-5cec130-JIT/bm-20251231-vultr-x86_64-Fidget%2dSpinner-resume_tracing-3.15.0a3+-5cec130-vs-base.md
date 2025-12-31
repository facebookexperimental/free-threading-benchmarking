# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 5cec130
- commit date: 2025-12-31
- overall geometric mean: 1.002x slower
- HPT reliability: 70.30%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 245 ms: 1.01x faster                                                       |
| html5lib       | 64.6 ms                                                                | 63.7 ms: 1.01x faster                                                      |
| sphinx         | 1.01 sec                                                               | 993 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 242 ms                                                                 | 229 ms: 1.06x faster                                                       |
| async_tree_memoization_tg  | 306 ms                                                                 | 291 ms: 1.05x faster                                                       |
| async_tree_memoization     | 302 ms                                                                 | 293 ms: 1.03x faster                                                       |
| async_tree_io_tg           | 586 ms                                                                 | 568 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 473 ms: 1.03x faster                                                       |
| async_tree_none            | 240 ms                                                                 | 236 ms: 1.02x faster                                                       |
| asyncio_websockets         | 544 ms                                                                 | 543 ms: 1.00x faster                                                       |
| coroutines                 | 23.9 ms                                                                | 24.3 ms: 1.02x slower                                                      |
| async_generators           | 355 ms                                                                 | 362 ms: 1.02x slower                                                       |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (2): async_tree_io, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 73.8 ms                                                                | 74.9 ms: 1.01x slower                                                      |
| pidigits       | 203 ms                                                                 | 207 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 2.74 ms                                                                | 2.74 ms: 1.00x slower                                                      |
| regex_dna      | 168 ms                                                                 | 171 ms: 1.02x slower                                                       |
| regex_v8       | 22.0 ms                                                                | 22.3 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_process    | 55.2 ms                                                                | 52.9 ms: 1.04x faster                                                      |
| unpickle_pure_python | 179 us                                                                 | 175 us: 1.03x faster                                                       |
| json_dumps           | 9.51 ms                                                                | 9.31 ms: 1.02x faster                                                      |
| json_loads           | 27.9 us                                                                | 27.4 us: 1.02x faster                                                      |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                       |
| xml_etree_generate   | 78.0 ms                                                                | 78.9 ms: 1.01x slower                                                      |
| tomli_loads          | 1.95 sec                                                               | 2.02 sec: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                                | 7.32 ms: 1.00x faster                                                      |
| python_startup         | 12.5 ms                                                                | 12.6 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 35.5 ms                                                                | 34.3 ms: 1.03x faster                                                      |
| mako            | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                      |
| genshi_text     | 20.9 ms                                                                | 21.2 ms: 1.02x slower                                                      |
| genshi_xml      | 52.7 ms                                                                | 54.3 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20251229-vultr-x86_64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| bench_mp_pool              | 242 ms                                                                 | 186 ms: 1.30x faster                                                       |
| logging_simple             | 5.84 us                                                                | 5.34 us: 1.09x faster                                                      |
| typing_runtime_protocols   | 159 us                                                                 | 147 us: 1.08x faster                                                       |
| telco                      | 161 ms                                                                 | 152 ms: 1.06x faster                                                       |
| async_tree_none_tg         | 242 ms                                                                 | 229 ms: 1.06x faster                                                       |
| dulwich_log                | 74.1 ms                                                                | 70.3 ms: 1.05x faster                                                      |
| async_tree_memoization_tg  | 306 ms                                                                 | 291 ms: 1.05x faster                                                       |
| logging_format             | 6.51 us                                                                | 6.22 us: 1.05x faster                                                      |
| deepcopy_reduce            | 2.58 us                                                                | 2.47 us: 1.04x faster                                                      |
| xml_etree_process          | 55.2 ms                                                                | 52.9 ms: 1.04x faster                                                      |
| pprint_safe_repr           | 659 ms                                                                 | 632 ms: 1.04x faster                                                       |
| chaos                      | 52.0 ms                                                                | 50.1 ms: 1.04x faster                                                      |
| pathlib                    | 17.7 ms                                                                | 17.1 ms: 1.03x faster                                                      |
| django_template            | 35.5 ms                                                                | 34.3 ms: 1.03x faster                                                      |
| async_tree_memoization     | 302 ms                                                                 | 293 ms: 1.03x faster                                                       |
| async_tree_io_tg           | 586 ms                                                                 | 568 ms: 1.03x faster                                                       |
| deltablue                  | 2.66 ms                                                                | 2.59 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 473 ms: 1.03x faster                                                       |
| pprint_pformat             | 1.34 sec                                                               | 1.31 sec: 1.03x faster                                                     |
| unpickle_pure_python       | 179 us                                                                 | 175 us: 1.03x faster                                                       |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.03x faster                                                      |
| scimark_sor                | 101 ms                                                                 | 98.3 ms: 1.02x faster                                                      |
| json_dumps                 | 9.51 ms                                                                | 9.31 ms: 1.02x faster                                                      |
| async_tree_none            | 240 ms                                                                 | 236 ms: 1.02x faster                                                       |
| json_loads                 | 27.9 us                                                                | 27.4 us: 1.02x faster                                                      |
| scimark_monte_carlo        | 52.5 ms                                                                | 51.6 ms: 1.02x faster                                                      |
| sphinx                     | 1.01 sec                                                               | 993 ms: 1.01x faster                                                       |
| hexiom                     | 6.18 ms                                                                | 6.08 ms: 1.01x faster                                                      |
| pyflate                    | 363 ms                                                                 | 357 ms: 1.01x faster                                                       |
| html5lib                   | 64.6 ms                                                                | 63.7 ms: 1.01x faster                                                      |
| comprehensions             | 15.9 us                                                                | 15.7 us: 1.01x faster                                                      |
| k_core                     | 1.86 sec                                                               | 1.84 sec: 1.01x faster                                                     |
| connected_components       | 384 ms                                                                 | 379 ms: 1.01x faster                                                       |
| json                       | 4.91 ms                                                                | 4.86 ms: 1.01x faster                                                      |
| 2to3                       | 248 ms                                                                 | 245 ms: 1.01x faster                                                       |
| mako                       | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                      |
| python_startup_no_site     | 7.35 ms                                                                | 7.32 ms: 1.00x faster                                                      |
| coverage                   | 81.2 ms                                                                | 81.0 ms: 1.00x faster                                                      |
| shortest_path              | 424 ms                                                                 | 423 ms: 1.00x faster                                                       |
| asyncio_websockets         | 544 ms                                                                 | 543 ms: 1.00x faster                                                       |
| regex_effbot               | 2.74 ms                                                                | 2.74 ms: 1.00x slower                                                      |
| python_startup             | 12.5 ms                                                                | 12.6 ms: 1.01x slower                                                      |
| scimark_lu                 | 97.7 ms                                                                | 98.3 ms: 1.01x slower                                                      |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                       |
| create_gc_cycles           | 1.87 ms                                                                | 1.89 ms: 1.01x slower                                                      |
| nqueens                    | 86.3 ms                                                                | 87.3 ms: 1.01x slower                                                      |
| xml_etree_generate         | 78.0 ms                                                                | 78.9 ms: 1.01x slower                                                      |
| deepcopy_memo              | 24.8 us                                                                | 25.1 us: 1.01x slower                                                      |
| nbody                      | 73.8 ms                                                                | 74.9 ms: 1.01x slower                                                      |
| deepcopy                   | 243 us                                                                 | 246 us: 1.02x slower                                                       |
| regex_dna                  | 168 ms                                                                 | 171 ms: 1.02x slower                                                       |
| coroutines                 | 23.9 ms                                                                | 24.3 ms: 1.02x slower                                                      |
| regex_v8                   | 22.0 ms                                                                | 22.3 ms: 1.02x slower                                                      |
| genshi_text                | 20.9 ms                                                                | 21.2 ms: 1.02x slower                                                      |
| richards                   | 18.0 ms                                                                | 18.3 ms: 1.02x slower                                                      |
| pidigits                   | 203 ms                                                                 | 207 ms: 1.02x slower                                                       |
| async_generators           | 355 ms                                                                 | 362 ms: 1.02x slower                                                       |
| thrift                     | 736 us                                                                 | 751 us: 1.02x slower                                                       |
| scimark_fft                | 257 ms                                                                 | 263 ms: 1.02x slower                                                       |
| gc_traversal               | 4.28 ms                                                                | 4.40 ms: 1.03x slower                                                      |
| genshi_xml                 | 52.7 ms                                                                | 54.3 ms: 1.03x slower                                                      |
| sqlglot_v2_normalize       | 110 ms                                                                 | 114 ms: 1.03x slower                                                       |
| tomli_loads                | 1.95 sec                                                               | 2.02 sec: 1.04x slower                                                     |
| spectral_norm              | 85.4 ms                                                                | 88.8 ms: 1.04x slower                                                      |
| logging_silent             | 81.1 ns                                                                | 84.9 ns: 1.05x slower                                                      |
| sqlglot_v2_transpile       | 1.54 ms                                                                | 1.62 ms: 1.05x slower                                                      |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.27 ms: 1.05x slower                                                      |
| mdp                        | 1.38 sec                                                               | 1.45 sec: 1.05x slower                                                     |
| sqlglot_v2_optimize        | 54.3 ms                                                                | 57.3 ms: 1.06x slower                                                      |
| scimark_sparse_mat_mult    | 4.31 ms                                                                | 4.58 ms: 1.06x slower                                                      |
| sympy_integrate            | 20.3 ms                                                                | 21.6 ms: 1.06x slower                                                      |
| sympy_str                  | 306 ms                                                                 | 326 ms: 1.07x slower                                                       |
| sympy_sum                  | 169 ms                                                                 | 181 ms: 1.07x slower                                                       |
| pycparser                  | 1.09 sec                                                               | 1.19 sec: 1.09x slower                                                     |
| pylint                     | 309 ms                                                                 | 343 ms: 1.11x slower                                                       |
| generators                 | 28.8 ms                                                                | 34.8 ms: 1.21x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (18): async_tree_io, async_tree_cpu_io_mixed, go, xml_etree_iterparse, meteor_contest, richards_super, bpe_tokeniser, regex_compile, raytrace, crypto_pyaes, fannkuch, pickle_pure_python, docutils, sympy_expand, many_optionals, subparsers, bench_thread_pool, float

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 70.30% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x