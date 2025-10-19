# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f38ef69
- commit date: 2025-10-19
- overall geometric mean: 1.032x slower
- HPT reliability: 58.54%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 291 ms: 1.12x slower                                                    |
| docutils       | 2.63 sec                                                               | 2.74 sec: 1.04x slower                                                  |
| html5lib       | 68.6 ms                                                                | 75.1 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 675 ms: 1.31x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 354 ms: 1.30x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 696 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 535 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 528 ms: 1.20x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 344 ms: 1.19x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 281 ms: 1.19x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 301 ms: 1.17x faster                                                    |
| async_generators           | 375 ms                                                                 | 391 ms: 1.04x slower                                                    |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                    |
| coroutines                 | 23.3 ms                                                                | 27.5 ms: 1.18x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 63.5 ms: 1.21x faster                                                   |
| pidigits       | 216 ms                                                                 | 194 ms: 1.12x faster                                                    |
| nbody          | 85.3 ms                                                                | 131 ms: 1.54x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.56 ms: 1.26x faster                                                   |
| regex_dna      | 189 ms                                                                 | 168 ms: 1.12x faster                                                    |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.07x faster                                                   |
| regex_compile  | 131 ms                                                                 | 160 ms: 1.22x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.33 ms: 1.14x faster                                                   |
| unpickle_pure_python | 208 us                                                                 | 190 us: 1.10x faster                                                    |
| tomli_loads          | 2.01 sec                                                               | 1.85 sec: 1.09x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 133 ms: 1.03x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.9 ms: 1.02x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                                | 87.9 ms: 1.03x slower                                                   |
| json_loads           | 27.3 us                                                                | 28.4 us: 1.04x slower                                                   |
| xml_etree_process    | 59.2 ms                                                                | 63.6 ms: 1.07x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 343 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                   |
| python_startup         | 11.0 ms                                                                | 12.9 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 10.6 ms: 1.06x faster                                                   |
| genshi_text     | 21.7 ms                                                                | 24.9 ms: 1.15x slower                                                   |
| django_template | 34.2 ms                                                                | 43.2 ms: 1.26x slower                                                   |
| genshi_xml      | 49.1 ms                                                                | 70.1 ms: 1.43x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.18x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.43 sec: 1.64x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 23.2 us: 1.64x faster                                                   |
| richards                   | 44.4 ms                                                                | 30.4 ms: 1.46x faster                                                   |
| richards_super             | 50.4 ms                                                                | 34.7 ms: 1.45x faster                                                   |
| deepcopy                   | 357 us                                                                 | 268 us: 1.33x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 675 ms: 1.31x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 354 ms: 1.30x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 696 ms: 1.30x faster                                                    |
| spectral_norm              | 108 ms                                                                 | 84.1 ms: 1.28x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.56 ms: 1.26x faster                                                   |
| scimark_fft                | 348 ms                                                                 | 279 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 535 ms: 1.25x faster                                                    |
| float                      | 76.7 ms                                                                | 63.5 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 528 ms: 1.20x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 344 ms: 1.19x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 281 ms: 1.19x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 301 ms: 1.17x faster                                                    |
| logging_silent             | 98.2 ns                                                                | 84.1 ns: 1.17x faster                                                   |
| pyflate                    | 449 ms                                                                 | 393 ms: 1.14x faster                                                    |
| json_dumps                 | 10.6 ms                                                                | 9.33 ms: 1.14x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 168 ms: 1.12x faster                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 3.97 sec: 1.12x faster                                                  |
| pidigits                   | 216 ms                                                                 | 194 ms: 1.12x faster                                                    |
| unpickle_pure_python       | 208 us                                                                 | 190 us: 1.10x faster                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 59.9 ms: 1.10x faster                                                   |
| tomli_loads                | 2.01 sec                                                               | 1.85 sec: 1.09x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.41 ms: 1.08x faster                                                   |
| comprehensions             | 16.6 us                                                                | 15.4 us: 1.08x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.90 us: 1.08x faster                                                   |
| go                         | 141 ms                                                                 | 131 ms: 1.07x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.07x faster                                                   |
| mako                       | 11.2 ms                                                                | 10.6 ms: 1.06x faster                                                   |
| fannkuch                   | 376 ms                                                                 | 362 ms: 1.04x faster                                                    |
| xml_etree_parse            | 136 ms                                                                 | 133 ms: 1.03x faster                                                    |
| deltablue                  | 3.10 ms                                                                | 3.05 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.9 ms: 1.02x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 132 ms: 1.01x faster                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 69.3 ms: 1.02x slower                                                   |
| dulwich_log                | 74.5 ms                                                                | 76.4 ms: 1.03x slower                                                   |
| coverage                   | 82.5 ms                                                                | 84.8 ms: 1.03x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 87.9 ms: 1.03x slower                                                   |
| json_loads                 | 27.3 us                                                                | 28.4 us: 1.04x slower                                                   |
| docutils                   | 2.63 sec                                                               | 2.74 sec: 1.04x slower                                                  |
| async_generators           | 375 ms                                                                 | 391 ms: 1.04x slower                                                    |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                    |
| chaos                      | 56.3 ms                                                                | 59.2 ms: 1.05x slower                                                   |
| thrift                     | 772 us                                                                 | 817 us: 1.06x slower                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 768 ms: 1.07x slower                                                    |
| xml_etree_process          | 59.2 ms                                                                | 63.6 ms: 1.07x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.57 sec: 1.08x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 20.8 ms: 1.08x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 84.1 ms: 1.08x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 21.3 ms: 1.08x slower                                                   |
| hexiom                     | 5.95 ms                                                                | 6.50 ms: 1.09x slower                                                   |
| html5lib                   | 68.6 ms                                                                | 75.1 ms: 1.09x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 171 us: 1.10x slower                                                    |
| 2to3                       | 259 ms                                                                 | 291 ms: 1.12x slower                                                    |
| sympy_sum                  | 154 ms                                                                 | 173 ms: 1.12x slower                                                    |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.13x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.27 sec: 1.13x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 24.9 ms: 1.15x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 315 ms: 1.15x slower                                                    |
| logging_format             | 6.92 us                                                                | 7.98 us: 1.15x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                                | 12.7 ms: 1.16x slower                                                   |
| logging_simple             | 6.14 us                                                                | 7.12 us: 1.16x slower                                                   |
| python_startup             | 11.0 ms                                                                | 12.9 ms: 1.17x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 132 ms: 1.18x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 343 us: 1.18x slower                                                    |
| coroutines                 | 23.3 ms                                                                | 27.5 ms: 1.18x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 540 ms: 1.19x slower                                                    |
| regex_compile              | 131 ms                                                                 | 160 ms: 1.22x slower                                                    |
| raytrace                   | 250 ms                                                                 | 308 ms: 1.23x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                    |
| django_template            | 34.2 ms                                                                | 43.2 ms: 1.26x slower                                                   |
| generators                 | 28.5 ms                                                                | 37.2 ms: 1.30x slower                                                   |
| gc_traversal               | 3.32 ms                                                                | 4.53 ms: 1.37x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 70.1 ms: 1.43x slower                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 1.93 ms: 1.45x slower                                                   |
| nbody                      | 85.3 ms                                                                | 131 ms: 1.54x slower                                                    |
| telco                      | 7.77 ms                                                                | 189 ms: 24.26x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (3): sqlite_synth, pylint, json
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251019-3.15.0a1+-f38ef69-JIT/bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x slower

# HPT report

- Reliability score: 58.54% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.18x