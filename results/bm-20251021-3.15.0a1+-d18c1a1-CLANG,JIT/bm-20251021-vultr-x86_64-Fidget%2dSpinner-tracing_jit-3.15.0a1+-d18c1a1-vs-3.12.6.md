# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: d18c1a1
- commit date: 2025-10-21
- overall geometric mean: 1.111x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                    |
| docutils       | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.83x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                    |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 470 ms: 1.52x faster                                                    |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 62.7 ms: 1.29x faster                                                   |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                    |
| nbody          | 89.3 ms                                                | 93.6 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                   |
| regex_compile  | 142 ms                                                 | 139 ms: 1.02x faster                                                    |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 185 us: 1.19x faster                                                    |
| json_dumps           | 10.4 ms                                                | 8.79 ms: 1.18x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 52.7 ms: 1.12x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 76.6 ms: 1.11x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.00 sec: 1.05x faster                                                  |
| json_loads           | 26.5 us                                                | 25.7 us: 1.03x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 95.2 ms: 1.02x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 148 ms: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.8 ms: 1.29x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.7 ms: 1.16x faster                                                   |
| django_template | 34.7 ms                                                | 33.4 ms: 1.04x faster                                                   |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                            |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 22.0 ms: 2.09x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.18 sec: 2.05x faster                                                  |
| richards_super             | 51.9 ms                                                | 26.8 ms: 1.93x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 22.0 us: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.83x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                    |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                    |
| deepcopy                   | 352 us                                                 | 229 us: 1.53x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 470 ms: 1.52x faster                                                    |
| scimark_fft                | 342 ms                                                 | 247 ms: 1.38x faster                                                    |
| logging_silent             | 109 ns                                                 | 78.9 ns: 1.38x faster                                                   |
| comprehensions             | 19.8 us                                                | 14.6 us: 1.36x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.33 us: 1.32x faster                                                   |
| spectral_norm              | 110 ms                                                 | 83.6 ms: 1.32x faster                                                   |
| scimark_sor                | 130 ms                                                 | 99.3 ms: 1.31x faster                                                   |
| float                      | 80.8 ms                                                | 62.7 ms: 1.29x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.78 ms: 1.24x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 56.0 ms: 1.22x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 3.94 sec: 1.20x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 185 us: 1.19x faster                                                    |
| chaos                      | 62.8 ms                                                | 52.9 ms: 1.19x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 96.6 ms: 1.18x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 8.79 ms: 1.18x faster                                                   |
| generators                 | 32.2 ms                                                | 27.6 ms: 1.17x faster                                                   |
| genshi_text                | 22.8 ms                                                | 19.7 ms: 1.16x faster                                                   |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 66.6 ms: 1.15x faster                                                   |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 653 ms: 1.14x faster                                                    |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                    |
| pyflate                    | 448 ms                                                 | 396 ms: 1.13x faster                                                    |
| logging_simple             | 6.63 us                                                | 5.87 us: 1.13x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 52.7 ms: 1.12x faster                                                   |
| logging_format             | 7.35 us                                                | 6.58 us: 1.12x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.11x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 76.6 ms: 1.11x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.37 sec: 1.11x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 148 us: 1.10x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                   |
| raytrace                   | 299 ms                                                 | 273 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.01 ms: 1.10x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 73.5 ms: 1.07x faster                                                   |
| fannkuch                   | 372 ms                                                 | 353 ms: 1.05x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                   |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 2.00 sec: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 753 us: 1.05x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.88 ms: 1.05x faster                                                   |
| sympy_str                  | 292 ms                                                 | 279 ms: 1.04x faster                                                    |
| django_template            | 34.7 ms                                                | 33.4 ms: 1.04x faster                                                   |
| json                       | 5.02 ms                                                | 4.84 ms: 1.04x faster                                                   |
| json_loads                 | 26.5 us                                                | 25.7 us: 1.03x faster                                                   |
| regex_compile              | 142 ms                                                 | 139 ms: 1.02x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.16 us: 1.02x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 95.2 ms: 1.02x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                    |
| docutils                   | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 81.1 ms: 1.01x slower                                                   |
| sympy_expand               | 468 ms                                                 | 475 ms: 1.02x slower                                                    |
| meteor_contest             | 104 ms                                                 | 106 ms: 1.02x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.02x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 970 us: 1.03x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                   |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                    |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| nbody                      | 89.3 ms                                                | 93.6 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| coverage                   | 71.4 ms                                                | 75.2 ms: 1.05x slower                                                   |
| xml_etree_parse            | 139 ms                                                 | 148 ms: 1.07x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.4 ms: 1.15x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.8 ms: 1.29x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.51 ms: 1.30x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 2.02 ms: 1.85x slower                                                   |
| telco                      | 6.53 ms                                                | 157 ms: 24.02x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                            |

Benchmark hidden because not significant (3): html5lib, mako, genshi_xml
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251021-3.15.0a1+-d18c1a1-CLANG,JIT/bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.22x