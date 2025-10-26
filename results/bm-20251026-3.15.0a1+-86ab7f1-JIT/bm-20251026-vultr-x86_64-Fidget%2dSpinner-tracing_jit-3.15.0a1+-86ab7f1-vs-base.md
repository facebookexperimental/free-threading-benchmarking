# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 86ab7f1
- commit date: 2025-10-26
- overall geometric mean: 1.006x faster
- HPT reliability: 99.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 2.60 sec                                                               | 2.68 sec: 1.03x slower                                                  |
| html5lib       | 60.7 ms                                                                | 69.5 ms: 1.14x slower                                                   |
| sphinx         | 989 ms                                                                 | 1.01 sec: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators           | 367 ms                                                                 | 370 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 591 ms                                                                 | 599 ms: 1.01x slower                                                    |
| async_tree_memoization_tg  | 305 ms                                                                 | 309 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 243 ms                                                                 | 247 ms: 1.02x slower                                                    |
| coroutines                 | 23.9 ms                                                                | 24.4 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 491 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 493 ms: 1.03x slower                                                    |
| async_tree_io              | 552 ms                                                                 | 568 ms: 1.03x slower                                                    |
| async_tree_none            | 243 ms                                                                 | 250 ms: 1.03x slower                                                    |
| async_tree_memoization     | 304 ms                                                                 | 317 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.9 ms                                                                | 61.7 ms: 1.17x faster                                                   |
| nbody          | 92.6 ms                                                                | 87.7 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 23.1 ms                                                                | 22.1 ms: 1.05x faster                                                   |
| regex_dna      | 187 ms                                                                 | 188 ms: 1.01x slower                                                    |
| regex_effbot   | 2.86 ms                                                                | 2.90 ms: 1.02x slower                                                   |
| regex_compile  | 124 ms                                                                 | 129 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 309 us                                                                 | 301 us: 1.03x faster                                                    |
| json_dumps           | 9.46 ms                                                                | 9.21 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 85.2 ms                                                                | 83.0 ms: 1.03x faster                                                   |
| xml_etree_parse      | 129 ms                                                                 | 129 ms: 1.00x faster                                                    |
| unpickle_pure_python | 183 us                                                                 | 185 us: 1.01x slower                                                    |
| json_loads           | 27.9 us                                                                | 28.3 us: 1.01x slower                                                   |
| tomli_loads          | 1.72 sec                                                               | 1.77 sec: 1.03x slower                                                  |
| xml_etree_generate   | 77.1 ms                                                                | 79.9 ms: 1.04x slower                                                   |
| xml_etree_process    | 53.7 ms                                                                | 56.0 ms: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup | 12.4 ms                                                                | 12.4 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 20.8 ms                                                                | 20.6 ms: 1.01x faster                                                   |
| mako            | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                   |
| genshi_xml      | 49.7 ms                                                                | 53.5 ms: 1.08x slower                                                   |
| django_template | 34.5 ms                                                                | 38.1 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251026-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-86ab7f1 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 40.8 ms                                                                | 20.8 ms: 1.96x faster                                                   |
| richards_super             | 46.7 ms                                                                | 25.6 ms: 1.83x faster                                                   |
| spectral_norm              | 99.1 ms                                                                | 83.4 ms: 1.19x faster                                                   |
| logging_silent             | 101 ns                                                                 | 86.0 ns: 1.18x faster                                                   |
| float                      | 71.9 ms                                                                | 61.7 ms: 1.17x faster                                                   |
| deltablue                  | 3.28 ms                                                                | 2.82 ms: 1.16x faster                                                   |
| deepcopy_memo              | 26.8 us                                                                | 23.7 us: 1.13x faster                                                   |
| scimark_sor                | 109 ms                                                                 | 98.5 ms: 1.11x faster                                                   |
| scimark_lu                 | 111 ms                                                                 | 102 ms: 1.08x faster                                                    |
| scimark_monte_carlo        | 61.8 ms                                                                | 57.2 ms: 1.08x faster                                                   |
| gc_traversal               | 4.32 ms                                                                | 4.06 ms: 1.06x faster                                                   |
| comprehensions             | 16.3 us                                                                | 15.3 us: 1.06x faster                                                   |
| nbody                      | 92.6 ms                                                                | 87.7 ms: 1.06x faster                                                   |
| regex_v8                   | 23.1 ms                                                                | 22.1 ms: 1.05x faster                                                   |
| chaos                      | 56.5 ms                                                                | 54.4 ms: 1.04x faster                                                   |
| pickle_pure_python         | 309 us                                                                 | 301 us: 1.03x faster                                                    |
| json_dumps                 | 9.46 ms                                                                | 9.21 ms: 1.03x faster                                                   |
| xml_etree_iterparse        | 85.2 ms                                                                | 83.0 ms: 1.03x faster                                                   |
| create_gc_cycles           | 1.95 ms                                                                | 1.91 ms: 1.02x faster                                                   |
| deepcopy_reduce            | 2.66 us                                                                | 2.61 us: 1.02x faster                                                   |
| pyflate                    | 401 ms                                                                 | 394 ms: 1.02x faster                                                    |
| crypto_pyaes               | 68.6 ms                                                                | 67.7 ms: 1.01x faster                                                   |
| scimark_fft                | 262 ms                                                                 | 259 ms: 1.01x faster                                                    |
| genshi_text                | 20.8 ms                                                                | 20.6 ms: 1.01x faster                                                   |
| k_core                     | 1.88 sec                                                               | 1.87 sec: 1.01x faster                                                  |
| typing_runtime_protocols   | 160 us                                                                 | 158 us: 1.01x faster                                                    |
| coverage                   | 82.3 ms                                                                | 81.9 ms: 1.01x faster                                                   |
| xml_etree_parse            | 129 ms                                                                 | 129 ms: 1.00x faster                                                    |
| python_startup             | 12.4 ms                                                                | 12.4 ms: 1.00x slower                                                   |
| mako                       | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                   |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.22 ms: 1.01x slower                                                   |
| unpickle_pure_python       | 183 us                                                                 | 185 us: 1.01x slower                                                    |
| regex_dna                  | 187 ms                                                                 | 188 ms: 1.01x slower                                                    |
| async_generators           | 367 ms                                                                 | 370 ms: 1.01x slower                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.53 ms: 1.01x slower                                                   |
| fannkuch                   | 367 ms                                                                 | 372 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 591 ms                                                                 | 599 ms: 1.01x slower                                                    |
| json_loads                 | 27.9 us                                                                | 28.3 us: 1.01x slower                                                   |
| async_tree_memoization_tg  | 305 ms                                                                 | 309 ms: 1.01x slower                                                    |
| sympy_expand               | 489 ms                                                                 | 496 ms: 1.02x slower                                                    |
| sympy_integrate            | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                   |
| regex_effbot               | 2.86 ms                                                                | 2.90 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.19 us                                                                | 2.23 us: 1.02x slower                                                   |
| async_tree_none_tg         | 243 ms                                                                 | 247 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult    | 4.32 ms                                                                | 4.41 ms: 1.02x slower                                                   |
| pprint_pformat             | 1.41 sec                                                               | 1.44 sec: 1.02x slower                                                  |
| sphinx                     | 989 ms                                                                 | 1.01 sec: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                                | 24.4 ms: 1.02x slower                                                   |
| pylint                     | 292 ms                                                                 | 298 ms: 1.02x slower                                                    |
| hexiom                     | 5.88 ms                                                                | 6.03 ms: 1.02x slower                                                   |
| sqlglot_v2_optimize        | 51.7 ms                                                                | 53.0 ms: 1.03x slower                                                   |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 491 ms: 1.03x slower                                                    |
| generators                 | 28.0 ms                                                                | 28.7 ms: 1.03x slower                                                   |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 493 ms: 1.03x slower                                                    |
| sympy_str                  | 282 ms                                                                 | 290 ms: 1.03x slower                                                    |
| async_tree_io              | 552 ms                                                                 | 568 ms: 1.03x slower                                                    |
| sympy_sum                  | 157 ms                                                                 | 162 ms: 1.03x slower                                                    |
| async_tree_none            | 243 ms                                                                 | 250 ms: 1.03x slower                                                    |
| telco                      | 158 ms                                                                 | 163 ms: 1.03x slower                                                    |
| tomli_loads                | 1.72 sec                                                               | 1.77 sec: 1.03x slower                                                  |
| docutils                   | 2.60 sec                                                               | 2.68 sec: 1.03x slower                                                  |
| nqueens                    | 79.2 ms                                                                | 81.9 ms: 1.03x slower                                                   |
| deepcopy                   | 249 us                                                                 | 257 us: 1.03x slower                                                    |
| xml_etree_generate         | 77.1 ms                                                                | 79.9 ms: 1.04x slower                                                   |
| many_optionals             | 1.25 ms                                                                | 1.30 ms: 1.04x slower                                                   |
| xml_etree_process          | 53.7 ms                                                                | 56.0 ms: 1.04x slower                                                   |
| regex_compile              | 124 ms                                                                 | 129 ms: 1.04x slower                                                    |
| async_tree_memoization     | 304 ms                                                                 | 317 ms: 1.04x slower                                                    |
| mdp                        | 1.17 sec                                                               | 1.23 sec: 1.05x slower                                                  |
| dulwich_log                | 68.5 ms                                                                | 72.9 ms: 1.06x slower                                                   |
| logging_format             | 6.59 us                                                                | 7.01 us: 1.06x slower                                                   |
| subparsers                 | 44.7 ms                                                                | 47.7 ms: 1.07x slower                                                   |
| thrift                     | 742 us                                                                 | 792 us: 1.07x slower                                                    |
| logging_simple             | 5.78 us                                                                | 6.19 us: 1.07x slower                                                   |
| pycparser                  | 1.08 sec                                                               | 1.16 sec: 1.08x slower                                                  |
| genshi_xml                 | 49.7 ms                                                                | 53.5 ms: 1.08x slower                                                   |
| sqlglot_v2_normalize       | 102 ms                                                                 | 110 ms: 1.09x slower                                                    |
| go                         | 107 ms                                                                 | 117 ms: 1.10x slower                                                    |
| raytrace                   | 251 ms                                                                 | 277 ms: 1.10x slower                                                    |
| django_template            | 34.5 ms                                                                | 38.1 ms: 1.11x slower                                                   |
| html5lib                   | 60.7 ms                                                                | 69.5 ms: 1.14x slower                                                   |
| pathlib                    | 17.6 ms                                                                | 20.3 ms: 1.15x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (12): json, pprint_safe_repr, pidigits, connected_components, asyncio_websockets, python_startup_no_site, bench_thread_pool, 2to3, bench_mp_pool, shortest_path, bpe_tokeniser, meteor_contest

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 99.91% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x