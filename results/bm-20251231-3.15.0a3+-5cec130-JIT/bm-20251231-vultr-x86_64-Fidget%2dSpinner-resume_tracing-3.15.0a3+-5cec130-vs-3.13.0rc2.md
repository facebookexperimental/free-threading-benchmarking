# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 5cec130
- commit date: 2025-12-31
- overall geometric mean: 1.082x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 245 ms: 1.06x faster                                                       |
| docutils       | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                     |
| html5lib       | 67.0 ms                                                      | 63.7 ms: 1.05x faster                                                      |
| Geometric mean | (ref)                                                        | 1.03x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 542 ms: 1.62x faster                                                       |
| async_tree_io_tg           | 913 ms                                                       | 568 ms: 1.61x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 293 ms: 1.57x faster                                                       |
| async_tree_none            | 354 ms                                                       | 236 ms: 1.50x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 229 ms: 1.47x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 291 ms: 1.42x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 481 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                                       |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                       |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                      |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.3 ms: 1.28x faster                                                      |
| nbody          | 85.1 ms                                                      | 74.9 ms: 1.14x faster                                                      |
| pidigits       | 217 ms                                                       | 207 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                        | 1.15x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.74 ms: 1.12x faster                                                      |
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                       |
| regex_dna      | 180 ms                                                       | 171 ms: 1.06x faster                                                       |
| regex_v8       | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                        | 1.07x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 175 us: 1.20x faster                                                       |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                      |
| json_dumps           | 10.5 ms                                                      | 9.31 ms: 1.13x faster                                                      |
| xml_etree_process    | 59.3 ms                                                      | 52.9 ms: 1.12x faster                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 78.9 ms: 1.08x faster                                                      |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                                       |
| pickle_pure_python   | 294 us                                                       | 280 us: 1.05x faster                                                       |
| tomli_loads          | 2.01 sec                                                     | 2.02 sec: 1.01x slower                                                     |
| json_loads           | 27.0 us                                                      | 27.4 us: 1.01x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.32 ms: 1.01x faster                                                      |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                      |
| genshi_text    | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                      |
| genshi_xml     | 48.8 ms                                                      | 54.3 ms: 1.11x slower                                                      |
| Geometric mean | (ref)                                                        | 1.01x slower                                                               |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 18.3 ms: 2.47x faster                                                      |
| richards_super             | 51.6 ms                                                      | 21.9 ms: 2.36x faster                                                      |
| mdp                        | 2.36 sec                                                     | 1.45 sec: 1.62x faster                                                     |
| async_tree_io              | 876 ms                                                       | 542 ms: 1.62x faster                                                       |
| async_tree_io_tg           | 913 ms                                                       | 568 ms: 1.61x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 293 ms: 1.57x faster                                                       |
| deepcopy_memo              | 39.1 us                                                      | 25.1 us: 1.56x faster                                                      |
| go                         | 141 ms                                                       | 91.4 ms: 1.54x faster                                                      |
| async_tree_none            | 354 ms                                                       | 236 ms: 1.50x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 229 ms: 1.47x faster                                                       |
| deepcopy                   | 355 us                                                       | 246 us: 1.44x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 291 ms: 1.42x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 481 ms: 1.38x faster                                                       |
| scimark_sor                | 134 ms                                                       | 98.3 ms: 1.37x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                                       |
| scimark_fft                | 349 ms                                                       | 263 ms: 1.33x faster                                                       |
| float                      | 77.5 ms                                                      | 60.3 ms: 1.28x faster                                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 51.6 ms: 1.27x faster                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 2.47 us: 1.26x faster                                                      |
| pyflate                    | 449 ms                                                       | 357 ms: 1.26x faster                                                       |
| spectral_norm              | 111 ms                                                       | 88.8 ms: 1.25x faster                                                      |
| deltablue                  | 3.12 ms                                                      | 2.59 ms: 1.21x faster                                                      |
| logging_silent             | 103 ns                                                       | 84.9 ns: 1.21x faster                                                      |
| unpickle_pure_python       | 210 us                                                       | 175 us: 1.20x faster                                                       |
| pprint_safe_repr           | 738 ms                                                       | 632 ms: 1.17x faster                                                       |
| logging_simple             | 6.16 us                                                      | 5.34 us: 1.15x faster                                                      |
| scimark_lu                 | 113 ms                                                       | 98.3 ms: 1.15x faster                                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.31 sec: 1.15x faster                                                     |
| chaos                      | 57.3 ms                                                      | 50.1 ms: 1.14x faster                                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                      |
| nbody                      | 85.1 ms                                                      | 74.9 ms: 1.14x faster                                                      |
| json_dumps                 | 10.5 ms                                                      | 9.31 ms: 1.13x faster                                                      |
| regex_effbot               | 3.08 ms                                                      | 2.74 ms: 1.12x faster                                                      |
| xml_etree_process          | 59.3 ms                                                      | 52.9 ms: 1.12x faster                                                      |
| pathlib                    | 19.2 ms                                                      | 17.1 ms: 1.12x faster                                                      |
| logging_format             | 6.84 us                                                      | 6.22 us: 1.10x faster                                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 4.05 sec: 1.10x faster                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 78.9 ms: 1.08x faster                                                      |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                      |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                       |
| dulwich_log                | 74.8 ms                                                      | 70.3 ms: 1.06x faster                                                      |
| 2to3                       | 260 ms                                                       | 245 ms: 1.06x faster                                                       |
| fannkuch                   | 370 ms                                                       | 350 ms: 1.06x faster                                                       |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.06x faster                                                       |
| typing_runtime_protocols   | 155 us                                                       | 147 us: 1.05x faster                                                       |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                       |
| pickle_pure_python         | 294 us                                                       | 280 us: 1.05x faster                                                       |
| html5lib                   | 67.0 ms                                                      | 63.7 ms: 1.05x faster                                                      |
| pidigits                   | 217 ms                                                       | 207 ms: 1.05x faster                                                       |
| comprehensions             | 16.5 us                                                      | 15.7 us: 1.05x faster                                                      |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                       |
| meteor_contest             | 102 ms                                                       | 97.7 ms: 1.04x faster                                                      |
| thrift                     | 778 us                                                       | 751 us: 1.04x faster                                                       |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.58 ms: 1.03x faster                                                      |
| coverage                   | 83.0 ms                                                      | 81.0 ms: 1.02x faster                                                      |
| crypto_pyaes               | 67.9 ms                                                      | 66.3 ms: 1.02x faster                                                      |
| regex_v8                   | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                      |
| genshi_text                | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                      |
| json                       | 4.93 ms                                                      | 4.86 ms: 1.01x faster                                                      |
| python_startup_no_site     | 7.39 ms                                                      | 7.32 ms: 1.01x faster                                                      |
| tomli_loads                | 2.01 sec                                                     | 2.02 sec: 1.01x slower                                                     |
| json_loads                 | 27.0 us                                                      | 27.4 us: 1.01x slower                                                      |
| hexiom                     | 5.99 ms                                                      | 6.08 ms: 1.02x slower                                                      |
| docutils                   | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                      |
| raytrace                   | 253 ms                                                       | 262 ms: 1.04x slower                                                       |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                       |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.07x slower                                                     |
| pylint                     | 317 ms                                                       | 343 ms: 1.08x slower                                                       |
| sympy_integrate            | 19.8 ms                                                      | 21.6 ms: 1.09x slower                                                      |
| nqueens                    | 78.6 ms                                                      | 87.3 ms: 1.11x slower                                                      |
| genshi_xml                 | 48.8 ms                                                      | 54.3 ms: 1.11x slower                                                      |
| sympy_expand               | 457 ms                                                       | 519 ms: 1.14x slower                                                       |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                      |
| sympy_sum                  | 156 ms                                                       | 181 ms: 1.16x slower                                                       |
| sympy_str                  | 275 ms                                                       | 326 ms: 1.19x slower                                                       |
| generators                 | 28.8 ms                                                      | 34.8 ms: 1.21x slower                                                      |
| gc_traversal               | 3.14 ms                                                      | 4.40 ms: 1.40x slower                                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.89 ms: 1.42x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.45x slower                                                      |
| bench_mp_pool              | 11.0 ms                                                      | 186 ms: 16.88x slower                                                      |
| telco                      | 7.82 ms                                                      | 152 ms: 19.37x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                               |

Benchmark hidden because not significant (2): sqlite_synth, django_template
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251231-3.15.0a3+-5cec130-JIT/bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x