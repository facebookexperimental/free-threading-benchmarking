# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 86ab7f1
- commit date: 2025-10-26
- overall geometric mean: 1.093x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                    |
| docutils       | 2.64 sec                                               | 2.68 sec: 1.02x slower                                                  |
| html5lib       | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 568 ms: 1.91x faster                                                    |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 317 ms: 1.75x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                    |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                    |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 61.7 ms: 1.31x faster                                                   |
| nbody          | 89.3 ms                                                | 87.7 ms: 1.02x faster                                                   |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 129 ms: 1.10x faster                                                    |
| regex_effbot   | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                   |
| regex_v8       | 20.6 ms                                                | 22.1 ms: 1.07x slower                                                   |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                  | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 185 us: 1.20x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 1.77 sec: 1.19x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 83.0 ms: 1.17x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.21 ms: 1.13x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| xml_etree_generate   | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 56.0 ms: 1.05x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 301 us: 1.02x faster                                                    |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                   |
| mako            | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                   |
| genshi_xml      | 50.2 ms                                                | 53.5 ms: 1.07x slower                                                   |
| django_template | 34.7 ms                                                | 38.1 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 20.8 ms: 2.21x faster                                                   |
| richards_super             | 51.9 ms                                                | 25.6 ms: 2.03x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.23 sec: 1.96x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 568 ms: 1.91x faster                                                    |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 317 ms: 1.75x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 23.7 us: 1.70x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                    |
| deepcopy                   | 352 us                                                 | 257 us: 1.37x faster                                                    |
| spectral_norm              | 110 ms                                                 | 83.4 ms: 1.32x faster                                                   |
| scimark_fft                | 342 ms                                                 | 259 ms: 1.32x faster                                                    |
| scimark_sor                | 130 ms                                                 | 98.5 ms: 1.32x faster                                                   |
| float                      | 80.8 ms                                                | 61.7 ms: 1.31x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.3 us: 1.29x faster                                                   |
| logging_silent             | 109 ns                                                 | 86.0 ns: 1.27x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.82 ms: 1.22x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 57.2 ms: 1.20x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 185 us: 1.20x faster                                                    |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 1.77 sec: 1.19x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.03 sec: 1.18x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 83.0 ms: 1.17x faster                                                   |
| chaos                      | 62.8 ms                                                | 54.4 ms: 1.15x faster                                                   |
| pyflate                    | 448 ms                                                 | 394 ms: 1.14x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 67.7 ms: 1.13x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.21 ms: 1.13x faster                                                   |
| generators                 | 32.2 ms                                                | 28.7 ms: 1.12x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 102 ms: 1.12x faster                                                    |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                   |
| regex_compile              | 142 ms                                                 | 129 ms: 1.10x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 684 ms: 1.09x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 72.9 ms: 1.08x faster                                                   |
| raytrace                   | 299 ms                                                 | 277 ms: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| logging_simple             | 6.63 us                                                | 6.19 us: 1.07x faster                                                   |
| pylint                     | 319 ms                                                 | 298 ms: 1.07x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.05x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 56.0 ms: 1.05x faster                                                   |
| logging_format             | 7.35 us                                                | 7.01 us: 1.05x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.6 ms: 1.05x faster                                                   |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                    |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                    |
| mako                       | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                   |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 162 ms: 1.03x faster                                                    |
| hexiom                     | 6.17 ms                                                | 6.03 ms: 1.02x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 301 us: 1.02x faster                                                    |
| nbody                      | 89.3 ms                                                | 87.7 ms: 1.02x faster                                                   |
| sympy_str                  | 292 ms                                                 | 290 ms: 1.01x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.68 sec: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                   |
| nqueens                    | 80.1 ms                                                | 81.9 ms: 1.02x slower                                                   |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| sympy_expand               | 468 ms                                                 | 496 ms: 1.06x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 53.5 ms: 1.07x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.1 ms: 1.07x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.07x slower                                                   |
| html5lib                   | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                   |
| django_template            | 34.7 ms                                                | 38.1 ms: 1.10x slower                                                   |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                    |
| coverage                   | 71.4 ms                                                | 81.9 ms: 1.15x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.5 ms: 1.16x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.06 ms: 1.18x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.91 ms: 1.75x slower                                                   |
| telco                      | 6.53 ms                                                | 163 ms: 25.00x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                            |

Benchmark hidden because not significant (5): pycparser, json, fannkuch, thrift, scimark_sparse_mat_mult
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251026-3.15.0a1+-86ab7f1-JIT/bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.093x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x