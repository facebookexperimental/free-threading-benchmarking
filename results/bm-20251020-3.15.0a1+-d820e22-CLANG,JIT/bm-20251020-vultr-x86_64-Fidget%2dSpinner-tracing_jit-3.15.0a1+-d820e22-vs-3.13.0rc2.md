# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: d820e22
- commit date: 2025-10-20
- overall geometric mean: 1.048x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 250 ms: 1.04x faster                                                    |
| docutils       | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 306 ms: 1.50x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 594 ms: 1.48x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 611 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 473 ms: 1.41x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.37x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 475 ms: 1.33x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 22.1 ms: 1.05x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                    |
| async_generators           | 375 ms                                                                 | 487 ms: 1.30x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 61.8 ms: 1.24x faster                                                   |
| pidigits       | 216 ms                                                                 | 192 ms: 1.13x faster                                                    |
| nbody          | 85.3 ms                                                                | 96.8 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 3.05 ms: 1.05x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 22.6 ms: 1.03x faster                                                   |
| regex_dna      | 189 ms                                                                 | 185 ms: 1.02x faster                                                    |
| regex_compile  | 131 ms                                                                 | 133 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 8.89 ms: 1.20x faster                                                   |
| unpickle_pure_python | 208 us                                                                 | 183 us: 1.14x faster                                                    |
| xml_etree_process    | 59.2 ms                                                                | 52.2 ms: 1.13x faster                                                   |
| tomli_loads          | 2.01 sec                                                               | 1.82 sec: 1.11x faster                                                  |
| json_loads           | 27.3 us                                                                | 25.7 us: 1.06x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                                | 83.2 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 95.5 ms: 1.01x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 305 us: 1.04x slower                                                    |
| xml_etree_parse      | 136 ms                                                                 | 147 ms: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                   |
| python_startup         | 11.0 ms                                                                | 12.7 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                                   |
| genshi_xml      | 49.1 ms                                                                | 51.8 ms: 1.06x slower                                                   |
| django_template | 34.2 ms                                                                | 37.2 ms: 1.09x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.17 sec: 2.00x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 22.4 us: 1.70x faster                                                   |
| deepcopy                   | 357 us                                                                 | 228 us: 1.57x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 306 ms: 1.50x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 594 ms: 1.48x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 611 ms: 1.47x faster                                                    |
| richards                   | 44.4 ms                                                                | 30.7 ms: 1.45x faster                                                   |
| scimark_fft                | 348 ms                                                                 | 247 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 473 ms: 1.41x faster                                                    |
| richards_super             | 50.4 ms                                                                | 36.3 ms: 1.39x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.37x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.36x faster                                                    |
| deepcopy_reduce            | 3.12 us                                                                | 2.32 us: 1.35x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 475 ms: 1.33x faster                                                    |
| scimark_sor                | 134 ms                                                                 | 101 ms: 1.32x faster                                                    |
| spectral_norm              | 108 ms                                                                 | 84.5 ms: 1.27x faster                                                   |
| float                      | 76.7 ms                                                                | 61.8 ms: 1.24x faster                                                   |
| logging_silent             | 98.2 ns                                                                | 80.0 ns: 1.23x faster                                                   |
| go                         | 141 ms                                                                 | 115 ms: 1.22x faster                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 55.0 ms: 1.20x faster                                                   |
| json_dumps                 | 10.6 ms                                                                | 8.89 ms: 1.20x faster                                                   |
| pyflate                    | 449 ms                                                                 | 384 ms: 1.17x faster                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.09 ms: 1.16x faster                                                   |
| pylint                     | 317 ms                                                                 | 277 ms: 1.15x faster                                                    |
| unpickle_pure_python       | 208 us                                                                 | 183 us: 1.14x faster                                                    |
| xml_etree_process          | 59.2 ms                                                                | 52.2 ms: 1.13x faster                                                   |
| pidigits                   | 216 ms                                                                 | 192 ms: 1.13x faster                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 3.99 sec: 1.12x faster                                                  |
| deltablue                  | 3.10 ms                                                                | 2.78 ms: 1.11x faster                                                   |
| tomli_loads                | 2.01 sec                                                               | 1.82 sec: 1.11x faster                                                  |
| comprehensions             | 16.6 us                                                                | 15.1 us: 1.10x faster                                                   |
| coverage                   | 82.5 ms                                                                | 75.5 ms: 1.09x faster                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 667 ms: 1.08x faster                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 146 us: 1.07x faster                                                    |
| json_loads                 | 27.3 us                                                                | 25.7 us: 1.06x faster                                                   |
| thrift                     | 772 us                                                                 | 726 us: 1.06x faster                                                    |
| sympy_integrate            | 19.7 ms                                                                | 18.7 ms: 1.06x faster                                                   |
| chaos                      | 56.3 ms                                                                | 53.4 ms: 1.05x faster                                                   |
| fannkuch                   | 376 ms                                                                 | 357 ms: 1.05x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 22.1 ms: 1.05x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 3.05 ms: 1.05x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.14 us: 1.05x faster                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 64.8 ms: 1.05x faster                                                   |
| 2to3                       | 259 ms                                                                 | 250 ms: 1.04x faster                                                    |
| pprint_pformat             | 1.46 sec                                                               | 1.41 sec: 1.03x faster                                                  |
| generators                 | 28.5 ms                                                                | 27.8 ms: 1.03x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 22.6 ms: 1.03x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 83.2 ms: 1.03x faster                                                   |
| hexiom                     | 5.95 ms                                                                | 5.82 ms: 1.02x faster                                                   |
| json                       | 4.98 ms                                                                | 4.88 ms: 1.02x faster                                                   |
| genshi_text                | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                                   |
| docutils                   | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 185 ms: 1.02x faster                                                    |
| nqueens                    | 77.7 ms                                                                | 77.0 ms: 1.01x faster                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                   |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 75.0 ms: 1.01x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 277 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.5 ms: 1.01x slower                                                   |
| regex_compile              | 131 ms                                                                 | 133 ms: 1.01x slower                                                    |
| logging_simple             | 6.14 us                                                                | 6.28 us: 1.02x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 105 ms: 1.04x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 305 us: 1.04x slower                                                    |
| logging_format             | 6.92 us                                                                | 7.24 us: 1.05x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 968 us: 1.05x slower                                                    |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 51.8 ms: 1.06x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 479 ms: 1.06x slower                                                    |
| raytrace                   | 250 ms                                                                 | 269 ms: 1.08x slower                                                    |
| xml_etree_parse            | 136 ms                                                                 | 147 ms: 1.08x slower                                                    |
| django_template            | 34.2 ms                                                                | 37.2 ms: 1.09x slower                                                   |
| pathlib                    | 19.3 ms                                                                | 21.1 ms: 1.10x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                   |
| nbody                      | 85.3 ms                                                                | 96.8 ms: 1.13x slower                                                   |
| python_startup             | 11.0 ms                                                                | 12.7 ms: 1.15x slower                                                   |
| async_generators           | 375 ms                                                                 | 487 ms: 1.30x slower                                                    |
| gc_traversal               | 3.32 ms                                                                | 4.40 ms: 1.33x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 160 ms: 1.42x slower                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 2.03 ms: 1.52x slower                                                   |
| telco                      | 7.77 ms                                                                | 154 ms: 19.85x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                            |

Benchmark hidden because not significant (3): sympy_sum, html5lib, mako
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251020-3.15.0a1+-d820e22-CLANG,JIT/bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.048x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.21x