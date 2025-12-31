# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 5cec130
- commit date: 2025-12-31
- overall geometric mean: 1.119x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 245 ms: 1.07x faster                                                       |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                     |
| Geometric mean | (ref)                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 542 ms: 2.00x faster                                                       |
| async_tree_none            | 464 ms                                                 | 236 ms: 1.97x faster                                                       |
| async_tree_io_tg           | 1.11 sec                                               | 568 ms: 1.95x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 291 ms: 1.92x faster                                                       |
| async_tree_memoization     | 555 ms                                                 | 293 ms: 1.89x faster                                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 481 ms: 1.49x faster                                                       |
| async_generators           | 384 ms                                                 | 362 ms: 1.06x faster                                                       |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                      |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 60.3 ms: 1.34x faster                                                      |
| nbody          | 89.3 ms                                                | 74.9 ms: 1.19x faster                                                      |
| pidigits       | 184 ms                                                 | 207 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                  | 1.12x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                       |
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.15x faster                                                      |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                       |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                      |
| Geometric mean | (ref)                                                  | 1.05x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 175 us: 1.26x faster                                                       |
| xml_etree_iterparse  | 96.7 ms                                                | 83.4 ms: 1.16x faster                                                      |
| xml_etree_process    | 59.0 ms                                                | 52.9 ms: 1.11x faster                                                      |
| json_dumps           | 10.4 ms                                                | 9.31 ms: 1.11x faster                                                      |
| pickle_pure_python   | 308 us                                                 | 280 us: 1.10x faster                                                       |
| xml_etree_generate   | 85.2 ms                                                | 78.9 ms: 1.08x faster                                                      |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                       |
| tomli_loads          | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                     |
| json_loads           | 26.5 us                                                | 27.4 us: 1.03x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                      |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                      |
| mako            | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                      |
| django_template | 34.7 ms                                                | 34.3 ms: 1.01x faster                                                      |
| genshi_xml      | 50.2 ms                                                | 54.3 ms: 1.08x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 18.3 ms: 2.51x faster                                                      |
| richards_super             | 51.9 ms                                                | 21.9 ms: 2.37x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 542 ms: 2.00x faster                                                       |
| async_tree_none            | 464 ms                                                 | 236 ms: 1.97x faster                                                       |
| async_tree_io_tg           | 1.11 sec                                               | 568 ms: 1.95x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 291 ms: 1.92x faster                                                       |
| async_tree_memoization     | 555 ms                                                 | 293 ms: 1.89x faster                                                       |
| mdp                        | 2.42 sec                                               | 1.45 sec: 1.67x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 25.1 us: 1.61x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                       |
| go                         | 139 ms                                                 | 91.4 ms: 1.52x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 481 ms: 1.49x faster                                                       |
| deepcopy                   | 352 us                                                 | 246 us: 1.43x faster                                                       |
| float                      | 80.8 ms                                                | 60.3 ms: 1.34x faster                                                      |
| deltablue                  | 3.45 ms                                                | 2.59 ms: 1.33x faster                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 51.6 ms: 1.33x faster                                                      |
| scimark_sor                | 130 ms                                                 | 98.3 ms: 1.32x faster                                                      |
| scimark_fft                | 342 ms                                                 | 263 ms: 1.30x faster                                                       |
| logging_silent             | 109 ns                                                 | 84.9 ns: 1.28x faster                                                      |
| unpickle_pure_python       | 221 us                                                 | 175 us: 1.26x faster                                                       |
| comprehensions             | 19.8 us                                                | 15.7 us: 1.26x faster                                                      |
| pathlib                    | 21.5 ms                                                | 17.1 ms: 1.26x faster                                                      |
| pyflate                    | 448 ms                                                 | 357 ms: 1.25x faster                                                       |
| chaos                      | 62.8 ms                                                | 50.1 ms: 1.25x faster                                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.47 us: 1.24x faster                                                      |
| logging_simple             | 6.63 us                                                | 5.34 us: 1.24x faster                                                      |
| spectral_norm              | 110 ms                                                 | 88.8 ms: 1.24x faster                                                      |
| nbody                      | 89.3 ms                                                | 74.9 ms: 1.19x faster                                                      |
| logging_format             | 7.35 us                                                | 6.22 us: 1.18x faster                                                      |
| pprint_safe_repr           | 743 ms                                                 | 632 ms: 1.18x faster                                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.05 sec: 1.17x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.31 sec: 1.16x faster                                                     |
| scimark_lu                 | 114 ms                                                 | 98.3 ms: 1.16x faster                                                      |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 83.4 ms: 1.16x faster                                                      |
| crypto_pyaes               | 76.6 ms                                                | 66.3 ms: 1.16x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.15x faster                                                      |
| raytrace                   | 299 ms                                                 | 262 ms: 1.14x faster                                                       |
| dulwich_log                | 78.9 ms                                                | 70.3 ms: 1.12x faster                                                      |
| xml_etree_process          | 59.0 ms                                                | 52.9 ms: 1.11x faster                                                      |
| json_dumps                 | 10.4 ms                                                | 9.31 ms: 1.11x faster                                                      |
| typing_runtime_protocols   | 163 us                                                 | 147 us: 1.11x faster                                                       |
| pickle_pure_python         | 308 us                                                 | 280 us: 1.10x faster                                                       |
| xml_etree_generate         | 85.2 ms                                                | 78.9 ms: 1.08x faster                                                      |
| genshi_text                | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                      |
| 2to3                       | 264 ms                                                 | 245 ms: 1.07x faster                                                       |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                       |
| fannkuch                   | 372 ms                                                 | 350 ms: 1.06x faster                                                       |
| async_generators           | 384 ms                                                 | 362 ms: 1.06x faster                                                       |
| meteor_contest             | 104 ms                                                 | 97.7 ms: 1.06x faster                                                      |
| thrift                     | 791 us                                                 | 751 us: 1.05x faster                                                       |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                      |
| tomli_loads                | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                     |
| json                       | 5.02 ms                                                | 4.86 ms: 1.03x faster                                                      |
| hexiom                     | 6.17 ms                                                | 6.08 ms: 1.01x faster                                                      |
| django_template            | 34.7 ms                                                | 34.3 ms: 1.01x faster                                                      |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                      |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                       |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                      |
| json_loads                 | 26.5 us                                                | 27.4 us: 1.03x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.58 ms: 1.04x slower                                                      |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                       |
| sympy_integrate            | 20.5 ms                                                | 21.6 ms: 1.05x slower                                                      |
| pylint                     | 319 ms                                                 | 343 ms: 1.08x slower                                                       |
| generators                 | 32.2 ms                                                | 34.8 ms: 1.08x slower                                                      |
| genshi_xml                 | 50.2 ms                                                | 54.3 ms: 1.08x slower                                                      |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                      |
| nqueens                    | 80.1 ms                                                | 87.3 ms: 1.09x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                                       |
| sympy_expand               | 468 ms                                                 | 519 ms: 1.11x slower                                                       |
| sympy_str                  | 292 ms                                                 | 326 ms: 1.12x slower                                                       |
| pidigits                   | 184 ms                                                 | 207 ms: 1.12x slower                                                       |
| coverage                   | 71.4 ms                                                | 81.0 ms: 1.13x slower                                                      |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                      |
| gc_traversal               | 3.46 ms                                                | 4.40 ms: 1.27x slower                                                      |
| bench_thread_pool          | 941 us                                                 | 1.33 ms: 1.41x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.89 ms: 1.74x slower                                                      |
| bench_mp_pool              | 10.8 ms                                                | 186 ms: 17.19x slower                                                      |
| telco                      | 6.53 ms                                                | 152 ms: 23.22x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                               |

Benchmark hidden because not significant (2): sqlite_synth, html5lib
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251231-3.15.0a3+-5cec130-JIT/bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.119x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.20x