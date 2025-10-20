# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: d820e22
- commit date: 2025-10-20
- overall geometric mean: 1.085x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                    |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                  |
| html5lib       | 63.6 ms                                                | 68.6 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 306 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                    |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.80x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 473 ms: 1.51x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| async_generators           | 384 ms                                                 | 487 ms: 1.27x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 61.8 ms: 1.31x faster                                                   |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| nbody          | 89.3 ms                                                | 96.8 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 133 ms: 1.07x faster                                                    |
| regex_effbot   | 3.17 ms                                                | 3.05 ms: 1.04x faster                                                   |
| regex_v8       | 20.6 ms                                                | 22.6 ms: 1.10x slower                                                   |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                  | 1.02x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 183 us: 1.20x faster                                                    |
| json_dumps           | 10.4 ms                                                | 8.89 ms: 1.17x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 52.2 ms: 1.13x faster                                                   |
| json_loads           | 26.5 us                                                | 25.7 us: 1.03x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 95.5 ms: 1.01x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 147 ms: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                   |
| mako            | 11.0 ms                                                | 11.2 ms: 1.02x slower                                                   |
| genshi_xml      | 50.2 ms                                                | 51.8 ms: 1.03x slower                                                   |
| django_template | 34.7 ms                                                | 37.2 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.17 sec: 2.06x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 306 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 22.4 us: 1.80x faster                                                   |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.80x faster                                                    |
| deepcopy                   | 352 us                                                 | 228 us: 1.54x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 473 ms: 1.51x faster                                                    |
| richards                   | 45.9 ms                                                | 30.7 ms: 1.50x faster                                                   |
| richards_super             | 51.9 ms                                                | 36.3 ms: 1.43x faster                                                   |
| scimark_fft                | 342 ms                                                 | 247 ms: 1.38x faster                                                    |
| logging_silent             | 109 ns                                                 | 80.0 ns: 1.36x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.32 us: 1.33x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.1 us: 1.32x faster                                                   |
| float                      | 80.8 ms                                                | 61.8 ms: 1.31x faster                                                   |
| spectral_norm              | 110 ms                                                 | 84.5 ms: 1.30x faster                                                   |
| scimark_sor                | 130 ms                                                 | 101 ms: 1.28x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 55.0 ms: 1.24x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.78 ms: 1.24x faster                                                   |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 183 us: 1.20x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 3.99 sec: 1.19x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 64.8 ms: 1.18x faster                                                   |
| chaos                      | 62.8 ms                                                | 53.4 ms: 1.18x faster                                                   |
| pyflate                    | 448 ms                                                 | 384 ms: 1.17x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 8.89 ms: 1.17x faster                                                   |
| generators                 | 32.2 ms                                                | 27.8 ms: 1.16x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.82 sec: 1.16x faster                                                  |
| pylint                     | 319 ms                                                 | 277 ms: 1.15x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 52.2 ms: 1.13x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 146 us: 1.12x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 667 ms: 1.11x faster                                                    |
| raytrace                   | 299 ms                                                 | 269 ms: 1.11x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                   |
| thrift                     | 791 us                                                 | 726 us: 1.09x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.09 ms: 1.07x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                   |
| regex_compile              | 142 ms                                                 | 133 ms: 1.07x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.82 ms: 1.06x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.28 us: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 277 ms: 1.05x faster                                                    |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 75.0 ms: 1.05x faster                                                   |
| fannkuch                   | 372 ms                                                 | 357 ms: 1.04x faster                                                    |
| nqueens                    | 80.1 ms                                                | 77.0 ms: 1.04x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 3.05 ms: 1.04x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                  |
| json_loads                 | 26.5 us                                                | 25.7 us: 1.03x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.14 us: 1.03x faster                                                   |
| json                       | 5.02 ms                                                | 4.88 ms: 1.03x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                  |
| pathlib                    | 21.5 ms                                                | 21.1 ms: 1.02x faster                                                   |
| logging_format             | 7.35 us                                                | 7.24 us: 1.02x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 95.5 ms: 1.01x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                                    |
| meteor_contest             | 104 ms                                                 | 105 ms: 1.02x slower                                                    |
| mako                       | 11.0 ms                                                | 11.2 ms: 1.02x slower                                                   |
| sympy_expand               | 468 ms                                                 | 479 ms: 1.03x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 968 us: 1.03x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 51.8 ms: 1.03x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                   |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| coverage                   | 71.4 ms                                                | 75.5 ms: 1.06x slower                                                   |
| xml_etree_parse            | 139 ms                                                 | 147 ms: 1.06x slower                                                    |
| django_template            | 34.7 ms                                                | 37.2 ms: 1.07x slower                                                   |
| html5lib                   | 63.6 ms                                                | 68.6 ms: 1.08x slower                                                   |
| nbody                      | 89.3 ms                                                | 96.8 ms: 1.08x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.6 ms: 1.10x slower                                                   |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 12.3 ms: 1.14x slower                                                   |
| async_generators           | 384 ms                                                 | 487 ms: 1.27x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 4.40 ms: 1.27x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 160 ms: 1.40x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 2.03 ms: 1.86x slower                                                   |
| telco                      | 6.53 ms                                                | 154 ms: 23.64x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                            |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251020-3.15.0a1+-d820e22-CLANG,JIT/bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.22x