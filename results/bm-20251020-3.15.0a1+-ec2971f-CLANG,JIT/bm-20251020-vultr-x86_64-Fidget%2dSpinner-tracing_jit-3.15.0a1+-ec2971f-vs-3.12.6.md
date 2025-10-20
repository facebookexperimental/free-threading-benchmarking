# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: ec2971f
- commit date: 2025-10-20
- overall geometric mean: 1.117x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 252 ms: 1.05x faster                                                    |
| docutils       | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 596 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 613 ms: 1.81x faster                                                    |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.53x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 475 ms: 1.51x faster                                                    |
| async_generators           | 384 ms                                                 | 334 ms: 1.15x faster                                                    |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 62.0 ms: 1.30x faster                                                   |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| nbody          | 89.3 ms                                                | 99.8 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                   |
| regex_compile  | 142 ms                                                 | 138 ms: 1.03x faster                                                    |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                    |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 183 us: 1.20x faster                                                    |
| json_dumps           | 10.4 ms                                                | 8.74 ms: 1.19x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 52.0 ms: 1.13x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 75.5 ms: 1.13x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                  |
| json_loads           | 26.5 us                                                | 25.9 us: 1.02x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 94.6 ms: 1.02x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                            |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.0 ms: 1.14x faster                                                   |
| django_template | 34.7 ms                                                | 33.5 ms: 1.04x faster                                                   |
| genshi_xml      | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                   |
| mako            | 11.0 ms                                                | 10.9 ms: 1.01x faster                                                   |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 21.9 ms: 2.10x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.18 sec: 2.05x faster                                                  |
| richards_super             | 51.9 ms                                                | 26.5 ms: 1.96x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 21.9 us: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 596 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 613 ms: 1.81x faster                                                    |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                    |
| deepcopy                   | 352 us                                                 | 228 us: 1.55x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.53x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 475 ms: 1.51x faster                                                    |
| scimark_fft                | 342 ms                                                 | 242 ms: 1.41x faster                                                    |
| logging_silent             | 109 ns                                                 | 78.4 ns: 1.39x faster                                                   |
| comprehensions             | 19.8 us                                                | 14.6 us: 1.36x faster                                                   |
| scimark_sor                | 130 ms                                                 | 97.0 ms: 1.34x faster                                                   |
| spectral_norm              | 110 ms                                                 | 83.5 ms: 1.32x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.35 us: 1.31x faster                                                   |
| float                      | 80.8 ms                                                | 62.0 ms: 1.30x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 54.4 ms: 1.26x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.75 ms: 1.25x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 93.6 ms: 1.22x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 183 us: 1.20x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 3.94 sec: 1.20x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 8.74 ms: 1.19x faster                                                   |
| chaos                      | 62.8 ms                                                | 53.1 ms: 1.18x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 65.8 ms: 1.16x faster                                                   |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.16x faster                                                   |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                    |
| async_generators           | 384 ms                                                 | 334 ms: 1.15x faster                                                    |
| genshi_text                | 22.8 ms                                                | 20.0 ms: 1.14x faster                                                   |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 655 ms: 1.14x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 52.0 ms: 1.13x faster                                                   |
| pyflate                    | 448 ms                                                 | 395 ms: 1.13x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.34 sec: 1.13x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 75.5 ms: 1.13x faster                                                   |
| raytrace                   | 299 ms                                                 | 266 ms: 1.12x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.91 ms: 1.12x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.93 us: 1.12x faster                                                   |
| logging_format             | 7.35 us                                                | 6.59 us: 1.12x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 147 us: 1.11x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                   |
| thrift                     | 791 us                                                 | 728 us: 1.09x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 73.6 ms: 1.07x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.81 ms: 1.06x faster                                                   |
| 2to3                       | 264 ms                                                 | 252 ms: 1.05x faster                                                    |
| sympy_str                  | 292 ms                                                 | 279 ms: 1.05x faster                                                    |
| json                       | 5.02 ms                                                | 4.83 ms: 1.04x faster                                                   |
| django_template            | 34.7 ms                                                | 33.5 ms: 1.04x faster                                                   |
| fannkuch                   | 372 ms                                                 | 360 ms: 1.03x faster                                                    |
| genshi_xml                 | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                   |
| regex_compile              | 142 ms                                                 | 138 ms: 1.03x faster                                                    |
| json_loads                 | 26.5 us                                                | 25.9 us: 1.02x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 94.6 ms: 1.02x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.17 us: 1.01x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                  |
| mako                       | 11.0 ms                                                | 10.9 ms: 1.01x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                  |
| sympy_expand               | 468 ms                                                 | 477 ms: 1.02x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 963 us: 1.02x slower                                                    |
| meteor_contest             | 104 ms                                                 | 106 ms: 1.02x slower                                                    |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                   |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| coverage                   | 71.4 ms                                                | 74.6 ms: 1.04x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                   |
| nbody                      | 89.3 ms                                                | 99.8 ms: 1.12x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.3 ms: 1.14x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.31 ms: 1.25x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 2.04 ms: 1.87x slower                                                   |
| telco                      | 6.53 ms                                                | 159 ms: 24.38x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.12x faster                                                            |

Benchmark hidden because not significant (3): pickle_pure_python, nqueens, html5lib
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251020-3.15.0a1+-ec2971f-CLANG,JIT/bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.117x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.22x