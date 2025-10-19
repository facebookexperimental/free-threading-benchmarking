# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f38ef69
- commit date: 2025-10-19
- overall geometric mean: 1.059x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 251 ms: 1.03x faster                                                    |
| docutils       | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                  |
| html5lib       | 68.6 ms                                                                | 64.4 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 305 ms: 1.51x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 595 ms: 1.48x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 612 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 472 ms: 1.41x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 305 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 474 ms: 1.34x faster                                                    |
| async_generators           | 375 ms                                                                 | 332 ms: 1.13x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.29x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 62.6 ms: 1.23x faster                                                   |
| pidigits       | 216 ms                                                                 | 192 ms: 1.13x faster                                                    |
| nbody          | 85.3 ms                                                                | 90.2 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 3.10 ms: 1.04x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 22.8 ms: 1.02x faster                                                   |
| regex_dna      | 189 ms                                                                 | 186 ms: 1.01x faster                                                    |
| regex_compile  | 131 ms                                                                 | 140 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 8.71 ms: 1.22x faster                                                   |
| unpickle_pure_python | 208 us                                                                 | 185 us: 1.13x faster                                                    |
| tomli_loads          | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 54.7 ms: 1.08x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                                | 80.2 ms: 1.06x faster                                                   |
| json_loads           | 27.3 us                                                                | 25.9 us: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 93.6 ms: 1.01x faster                                                   |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                   |
| python_startup         | 11.0 ms                                                                | 12.7 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text    | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                                   |
| mako           | 11.2 ms                                                                | 11.0 ms: 1.02x faster                                                   |
| genshi_xml     | 49.1 ms                                                                | 57.7 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.22 sec: 1.92x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 21.7 us: 1.75x faster                                                   |
| richards                   | 44.4 ms                                                                | 28.8 ms: 1.54x faster                                                   |
| deepcopy                   | 357 us                                                                 | 232 us: 1.54x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 305 ms: 1.51x faster                                                    |
| richards_super             | 50.4 ms                                                                | 33.6 ms: 1.50x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 595 ms: 1.48x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 612 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 472 ms: 1.41x faster                                                    |
| scimark_fft                | 348 ms                                                                 | 250 ms: 1.40x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 305 ms: 1.34x faster                                                    |
| scimark_sor                | 134 ms                                                                 | 99.9 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 474 ms: 1.34x faster                                                    |
| spectral_norm              | 108 ms                                                                 | 82.4 ms: 1.31x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.40 us: 1.30x faster                                                   |
| logging_silent             | 98.2 ns                                                                | 79.6 ns: 1.23x faster                                                   |
| float                      | 76.7 ms                                                                | 62.6 ms: 1.23x faster                                                   |
| json_dumps                 | 10.6 ms                                                                | 8.71 ms: 1.22x faster                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.03 ms: 1.18x faster                                                   |
| go                         | 141 ms                                                                 | 122 ms: 1.15x faster                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 57.5 ms: 1.15x faster                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 3.91 sec: 1.14x faster                                                  |
| pylint                     | 317 ms                                                                 | 279 ms: 1.14x faster                                                    |
| pyflate                    | 449 ms                                                                 | 396 ms: 1.13x faster                                                    |
| pidigits                   | 216 ms                                                                 | 192 ms: 1.13x faster                                                    |
| comprehensions             | 16.6 us                                                                | 14.7 us: 1.13x faster                                                   |
| async_generators           | 375 ms                                                                 | 332 ms: 1.13x faster                                                    |
| unpickle_pure_python       | 208 us                                                                 | 185 us: 1.13x faster                                                    |
| deltablue                  | 3.10 ms                                                                | 2.77 ms: 1.12x faster                                                   |
| tomli_loads                | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 102 ms: 1.10x faster                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 654 ms: 1.10x faster                                                    |
| xml_etree_process          | 59.2 ms                                                                | 54.7 ms: 1.08x faster                                                   |
| coverage                   | 82.5 ms                                                                | 76.2 ms: 1.08x faster                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 145 us: 1.07x faster                                                    |
| pprint_pformat             | 1.46 sec                                                               | 1.37 sec: 1.07x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 64.4 ms: 1.07x faster                                                   |
| logging_format             | 6.92 us                                                                | 6.49 us: 1.07x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 80.2 ms: 1.06x faster                                                   |
| logging_simple             | 6.14 us                                                                | 5.79 us: 1.06x faster                                                   |
| json_loads                 | 27.3 us                                                                | 25.9 us: 1.06x faster                                                   |
| fannkuch                   | 376 ms                                                                 | 356 ms: 1.05x faster                                                    |
| chaos                      | 56.3 ms                                                                | 53.5 ms: 1.05x faster                                                   |
| sympy_integrate            | 19.7 ms                                                                | 18.8 ms: 1.05x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.16 us: 1.04x faster                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 65.5 ms: 1.04x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 3.10 ms: 1.04x faster                                                   |
| 2to3                       | 259 ms                                                                 | 251 ms: 1.03x faster                                                    |
| thrift                     | 772 us                                                                 | 747 us: 1.03x faster                                                    |
| hexiom                     | 5.95 ms                                                                | 5.80 ms: 1.03x faster                                                   |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.03x faster                                                  |
| json                       | 4.98 ms                                                                | 4.88 ms: 1.02x faster                                                   |
| genshi_text                | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                                   |
| docutils                   | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                  |
| mako                       | 11.2 ms                                                                | 11.0 ms: 1.02x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 22.8 ms: 1.02x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 73.2 ms: 1.02x faster                                                   |
| pathlib                    | 19.3 ms                                                                | 19.0 ms: 1.01x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 186 ms: 1.01x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 93.6 ms: 1.01x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                   |
| sympy_str                  | 274 ms                                                                 | 277 ms: 1.01x slower                                                    |
| nqueens                    | 77.7 ms                                                                | 79.5 ms: 1.02x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 471 ms: 1.04x slower                                                    |
| bench_thread_pool          | 924 us                                                                 | 966 us: 1.05x slower                                                    |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                    |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                    |
| nbody                      | 85.3 ms                                                                | 90.2 ms: 1.06x slower                                                   |
| regex_compile              | 131 ms                                                                 | 140 ms: 1.06x slower                                                    |
| raytrace                   | 250 ms                                                                 | 269 ms: 1.08x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                   |
| python_startup             | 11.0 ms                                                                | 12.7 ms: 1.15x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 57.7 ms: 1.17x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.22x slower                                                    |
| generators                 | 28.5 ms                                                                | 36.2 ms: 1.27x slower                                                   |
| gc_traversal               | 3.32 ms                                                                | 4.48 ms: 1.35x slower                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 2.02 ms: 1.52x slower                                                   |
| telco                      | 7.77 ms                                                                | 157 ms: 20.20x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                            |

Benchmark hidden because not significant (3): django_template, sympy_sum, pickle_pure_python
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251019-3.15.0a1+-f38ef69-CLANG,JIT/bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.059x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.21x