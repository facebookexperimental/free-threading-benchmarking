# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 62ea35e
- commit date: 2026-03-15
- overall geometric mean: 1.133x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                       |
| docutils       | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                     |
| html5lib       | 63.6 ms                                                | 62.5 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 550 ms: 2.02x faster                                                       |
| async_tree_none            | 464 ms                                                 | 233 ms: 1.99x faster                                                       |
| async_tree_memoization     | 555 ms                                                 | 290 ms: 1.91x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.91x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 294 ms: 1.90x faster                                                       |
| async_tree_io              | 1.08 sec                                               | 573 ms: 1.89x faster                                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                       |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                      |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                       |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 58.9 ms: 1.37x faster                                                      |
| nbody          | 89.3 ms                                                | 76.6 ms: 1.17x faster                                                      |
| pidigits       | 184 ms                                                 | 201 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                  | 1.14x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                       |
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                      |
| regex_dna      | 168 ms                                                 | 179 ms: 1.06x slower                                                       |
| regex_v8       | 20.6 ms                                                | 23.4 ms: 1.13x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.55 sec: 1.36x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 83.8 ms: 1.15x faster                                                      |
| json_dumps           | 10.4 ms                                                | 9.15 ms: 1.13x faster                                                      |
| xml_etree_process    | 59.0 ms                                                | 53.0 ms: 1.11x faster                                                      |
| unpickle_pure_python | 221 us                                                 | 199 us: 1.11x faster                                                       |
| xml_etree_generate   | 85.2 ms                                                | 78.9 ms: 1.08x faster                                                      |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                       |
| pickle_pure_python   | 308 us                                                 | 315 us: 1.02x slower                                                       |
| json_loads           | 26.5 us                                                | 27.7 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.53 ms: 1.05x slower                                                      |
| python_startup         | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.3 ms: 1.12x faster                                                      |
| mako           | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                      |
| genshi_xml     | 50.2 ms                                                | 52.4 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 18.4 ms: 2.49x faster                                                      |
| richards_super             | 51.9 ms                                                | 22.1 ms: 2.34x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 550 ms: 2.02x faster                                                       |
| mdp                        | 2.42 sec                                               | 1.20 sec: 2.01x faster                                                     |
| async_tree_none            | 464 ms                                                 | 233 ms: 1.99x faster                                                       |
| async_tree_memoization     | 555 ms                                                 | 290 ms: 1.91x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.91x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 294 ms: 1.90x faster                                                       |
| async_tree_io              | 1.08 sec                                               | 573 ms: 1.89x faster                                                       |
| deepcopy_memo              | 40.3 us                                                | 22.6 us: 1.78x faster                                                      |
| scimark_sor                | 130 ms                                                 | 82.3 ms: 1.58x faster                                                      |
| deepcopy                   | 352 us                                                 | 229 us: 1.54x faster                                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                       |
| scimark_lu                 | 114 ms                                                 | 80.1 ms: 1.42x faster                                                      |
| spectral_norm              | 110 ms                                                 | 77.8 ms: 1.42x faster                                                      |
| float                      | 80.8 ms                                                | 58.9 ms: 1.37x faster                                                      |
| go                         | 139 ms                                                 | 102 ms: 1.37x faster                                                       |
| tomli_loads                | 2.11 sec                                               | 1.55 sec: 1.36x faster                                                     |
| logging_silent             | 109 ns                                                 | 81.0 ns: 1.35x faster                                                      |
| comprehensions             | 19.8 us                                                | 14.9 us: 1.33x faster                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 51.5 ms: 1.33x faster                                                      |
| scimark_fft                | 342 ms                                                 | 262 ms: 1.31x faster                                                       |
| deltablue                  | 3.45 ms                                                | 2.67 ms: 1.29x faster                                                      |
| pathlib                    | 21.5 ms                                                | 17.3 ms: 1.24x faster                                                      |
| pyflate                    | 448 ms                                                 | 363 ms: 1.23x faster                                                       |
| deepcopy_reduce            | 3.08 us                                                | 2.51 us: 1.23x faster                                                      |
| logging_simple             | 6.63 us                                                | 5.46 us: 1.21x faster                                                      |
| chaos                      | 62.8 ms                                                | 51.8 ms: 1.21x faster                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 3.96 sec: 1.20x faster                                                     |
| logging_format             | 7.35 us                                                | 6.17 us: 1.19x faster                                                      |
| crypto_pyaes               | 76.6 ms                                                | 65.4 ms: 1.17x faster                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.30 sec: 1.17x faster                                                     |
| nbody                      | 89.3 ms                                                | 76.6 ms: 1.17x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 83.8 ms: 1.15x faster                                                      |
| pprint_safe_repr           | 743 ms                                                 | 649 ms: 1.14x faster                                                       |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                       |
| json_dumps                 | 10.4 ms                                                | 9.15 ms: 1.13x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                      |
| genshi_text                | 22.8 ms                                                | 20.3 ms: 1.12x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                      |
| xml_etree_process          | 59.0 ms                                                | 53.0 ms: 1.11x faster                                                      |
| unpickle_pure_python       | 221 us                                                 | 199 us: 1.11x faster                                                       |
| nqueens                    | 80.1 ms                                                | 73.1 ms: 1.09x faster                                                      |
| fannkuch                   | 372 ms                                                 | 341 ms: 1.09x faster                                                       |
| typing_runtime_protocols   | 163 us                                                 | 151 us: 1.08x faster                                                       |
| xml_etree_generate         | 85.2 ms                                                | 78.9 ms: 1.08x faster                                                      |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                      |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                       |
| meteor_contest             | 104 ms                                                 | 96.7 ms: 1.07x faster                                                      |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                       |
| hexiom                     | 6.17 ms                                                | 5.82 ms: 1.06x faster                                                      |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                       |
| pylint                     | 319 ms                                                 | 305 ms: 1.04x faster                                                       |
| mako                       | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                      |
| json                       | 5.02 ms                                                | 4.90 ms: 1.03x faster                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.30 ms: 1.02x faster                                                      |
| raytrace                   | 299 ms                                                 | 293 ms: 1.02x faster                                                       |
| html5lib                   | 63.6 ms                                                | 62.5 ms: 1.02x faster                                                      |
| sympy_integrate            | 20.5 ms                                                | 20.4 ms: 1.01x faster                                                      |
| docutils                   | 2.64 sec                                               | 2.66 sec: 1.01x slower                                                     |
| thrift                     | 791 us                                                 | 804 us: 1.02x slower                                                       |
| pickle_pure_python         | 308 us                                                 | 315 us: 1.02x slower                                                       |
| sympy_str                  | 292 ms                                                 | 300 ms: 1.03x slower                                                       |
| sympy_sum                  | 166 ms                                                 | 171 ms: 1.03x slower                                                       |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.04x slower                                                      |
| genshi_xml                 | 50.2 ms                                                | 52.4 ms: 1.04x slower                                                      |
| sympy_expand               | 468 ms                                                 | 492 ms: 1.05x slower                                                       |
| python_startup_no_site     | 7.16 ms                                                | 7.53 ms: 1.05x slower                                                      |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                       |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.06x slower                                                       |
| generators                 | 32.2 ms                                                | 35.0 ms: 1.09x slower                                                      |
| pidigits                   | 184 ms                                                 | 201 ms: 1.09x slower                                                       |
| regex_v8                   | 20.6 ms                                                | 23.4 ms: 1.13x slower                                                      |
| coverage                   | 71.4 ms                                                | 83.1 ms: 1.16x slower                                                      |
| python_startup             | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                      |
| gc_traversal               | 3.46 ms                                                | 4.64 ms: 1.34x slower                                                      |
| bench_thread_pool          | 941 us                                                 | 1.33 ms: 1.41x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.71x slower                                                      |
| bench_mp_pool              | 10.8 ms                                                | 191 ms: 17.66x slower                                                      |
| telco                      | 6.53 ms                                                | 160 ms: 24.46x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                               |

Benchmark hidden because not significant (3): pycparser, django_template, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260315-3.15.0a7+-62ea35e-JIT/bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.133x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.20x