# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: abecfd6
- commit date: 2025-10-24
- overall geometric mean: 1.002x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 254 ms: 1.01x slower                                                    |
| docutils       | 2.60 sec                                                               | 2.66 sec: 1.02x slower                                                  |
| html5lib       | 60.7 ms                                                                | 69.3 ms: 1.14x slower                                                   |
| sphinx         | 989 ms                                                                 | 996 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators           | 367 ms                                                                 | 371 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 591 ms                                                                 | 599 ms: 1.01x slower                                                    |
| async_tree_memoization_tg  | 305 ms                                                                 | 310 ms: 1.02x slower                                                    |
| async_tree_none_tg         | 243 ms                                                                 | 247 ms: 1.02x slower                                                    |
| async_tree_none            | 243 ms                                                                 | 251 ms: 1.03x slower                                                    |
| async_tree_memoization     | 304 ms                                                                 | 315 ms: 1.04x slower                                                    |
| coroutines                 | 23.9 ms                                                                | 24.9 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 512 ms: 1.07x slower                                                    |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 520 ms: 1.08x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.9 ms                                                                | 61.4 ms: 1.17x faster                                                   |
| pidigits       | 194 ms                                                                 | 216 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 161 ms: 1.16x faster                                                    |
| regex_effbot   | 2.86 ms                                                                | 2.50 ms: 1.14x faster                                                   |
| regex_v8       | 23.1 ms                                                                | 21.7 ms: 1.07x faster                                                   |
| regex_compile  | 124 ms                                                                 | 130 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 9.46 ms                                                                | 9.24 ms: 1.02x faster                                                   |
| xml_etree_iterparse  | 85.2 ms                                                                | 83.9 ms: 1.02x faster                                                   |
| pickle_pure_python   | 309 us                                                                 | 313 us: 1.01x slower                                                    |
| unpickle_pure_python | 183 us                                                                 | 185 us: 1.01x slower                                                    |
| json_loads           | 27.9 us                                                                | 28.2 us: 1.01x slower                                                   |
| xml_etree_process    | 53.7 ms                                                                | 55.7 ms: 1.04x slower                                                   |
| xml_etree_generate   | 77.1 ms                                                                | 79.9 ms: 1.04x slower                                                   |
| tomli_loads          | 1.72 sec                                                               | 1.80 sec: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.25 ms                                                                | 7.23 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 20.8 ms                                                                | 21.5 ms: 1.03x slower                                                   |
| django_template | 34.5 ms                                                                | 35.6 ms: 1.03x slower                                                   |
| genshi_xml      | 49.7 ms                                                                | 53.0 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-abecfd6 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 40.8 ms                                                                | 22.5 ms: 1.82x faster                                                   |
| richards_super             | 46.7 ms                                                                | 27.5 ms: 1.70x faster                                                   |
| float                      | 71.9 ms                                                                | 61.4 ms: 1.17x faster                                                   |
| logging_silent             | 101 ns                                                                 | 86.6 ns: 1.17x faster                                                   |
| regex_dna                  | 187 ms                                                                 | 161 ms: 1.16x faster                                                    |
| spectral_norm              | 99.1 ms                                                                | 85.6 ms: 1.16x faster                                                   |
| deltablue                  | 3.28 ms                                                                | 2.84 ms: 1.15x faster                                                   |
| regex_effbot               | 2.86 ms                                                                | 2.50 ms: 1.14x faster                                                   |
| deepcopy_memo              | 26.8 us                                                                | 24.0 us: 1.11x faster                                                   |
| scimark_sor                | 109 ms                                                                 | 100 ms: 1.09x faster                                                    |
| scimark_monte_carlo        | 61.8 ms                                                                | 57.9 ms: 1.07x faster                                                   |
| regex_v8                   | 23.1 ms                                                                | 21.7 ms: 1.07x faster                                                   |
| crypto_pyaes               | 68.6 ms                                                                | 64.5 ms: 1.06x faster                                                   |
| scimark_lu                 | 111 ms                                                                 | 104 ms: 1.06x faster                                                    |
| comprehensions             | 16.3 us                                                                | 15.4 us: 1.06x faster                                                   |
| chaos                      | 56.5 ms                                                                | 54.3 ms: 1.04x faster                                                   |
| scimark_sparse_mat_mult    | 4.32 ms                                                                | 4.19 ms: 1.03x faster                                                   |
| deepcopy_reduce            | 2.66 us                                                                | 2.58 us: 1.03x faster                                                   |
| json_dumps                 | 9.46 ms                                                                | 9.24 ms: 1.02x faster                                                   |
| create_gc_cycles           | 1.95 ms                                                                | 1.91 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 85.2 ms                                                                | 83.9 ms: 1.02x faster                                                   |
| coverage                   | 82.3 ms                                                                | 81.1 ms: 1.02x faster                                                   |
| pyflate                    | 401 ms                                                                 | 397 ms: 1.01x faster                                                    |
| k_core                     | 1.88 sec                                                               | 1.86 sec: 1.01x faster                                                  |
| json                       | 5.03 ms                                                                | 4.98 ms: 1.01x faster                                                   |
| scimark_fft                | 262 ms                                                                 | 260 ms: 1.01x faster                                                    |
| python_startup_no_site     | 7.25 ms                                                                | 7.23 ms: 1.00x faster                                                   |
| 2to3                       | 253 ms                                                                 | 254 ms: 1.01x slower                                                    |
| telco                      | 158 ms                                                                 | 159 ms: 1.01x slower                                                    |
| bpe_tokeniser              | 4.01 sec                                                               | 4.04 sec: 1.01x slower                                                  |
| sphinx                     | 989 ms                                                                 | 996 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 160 us                                                                 | 161 us: 1.01x slower                                                    |
| pickle_pure_python         | 309 us                                                                 | 313 us: 1.01x slower                                                    |
| async_generators           | 367 ms                                                                 | 371 ms: 1.01x slower                                                    |
| bench_thread_pool          | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                   |
| unpickle_pure_python       | 183 us                                                                 | 185 us: 1.01x slower                                                    |
| json_loads                 | 27.9 us                                                                | 28.2 us: 1.01x slower                                                   |
| deepcopy                   | 249 us                                                                 | 252 us: 1.01x slower                                                    |
| async_tree_io_tg           | 591 ms                                                                 | 599 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.19 us                                                                | 2.22 us: 1.01x slower                                                   |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.23 ms: 1.01x slower                                                   |
| async_tree_memoization_tg  | 305 ms                                                                 | 310 ms: 1.02x slower                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.54 ms: 1.02x slower                                                   |
| async_tree_none_tg         | 243 ms                                                                 | 247 ms: 1.02x slower                                                    |
| sympy_integrate            | 19.3 ms                                                                | 19.8 ms: 1.02x slower                                                   |
| docutils                   | 2.60 sec                                                               | 2.66 sec: 1.02x slower                                                  |
| sqlglot_v2_optimize        | 51.7 ms                                                                | 52.9 ms: 1.02x slower                                                   |
| pylint                     | 292 ms                                                                 | 299 ms: 1.02x slower                                                    |
| sympy_sum                  | 157 ms                                                                 | 162 ms: 1.03x slower                                                    |
| hexiom                     | 5.88 ms                                                                | 6.06 ms: 1.03x slower                                                   |
| genshi_text                | 20.8 ms                                                                | 21.5 ms: 1.03x slower                                                   |
| async_tree_none            | 243 ms                                                                 | 251 ms: 1.03x slower                                                    |
| django_template            | 34.5 ms                                                                | 35.6 ms: 1.03x slower                                                   |
| pprint_pformat             | 1.41 sec                                                               | 1.46 sec: 1.03x slower                                                  |
| async_tree_memoization     | 304 ms                                                                 | 315 ms: 1.04x slower                                                    |
| xml_etree_process          | 53.7 ms                                                                | 55.7 ms: 1.04x slower                                                   |
| xml_etree_generate         | 77.1 ms                                                                | 79.9 ms: 1.04x slower                                                   |
| sympy_expand               | 489 ms                                                                 | 507 ms: 1.04x slower                                                    |
| sympy_str                  | 282 ms                                                                 | 293 ms: 1.04x slower                                                    |
| coroutines                 | 23.9 ms                                                                | 24.9 ms: 1.04x slower                                                   |
| many_optionals             | 1.25 ms                                                                | 1.31 ms: 1.04x slower                                                   |
| tomli_loads                | 1.72 sec                                                               | 1.80 sec: 1.05x slower                                                  |
| regex_compile              | 124 ms                                                                 | 130 ms: 1.05x slower                                                    |
| subparsers                 | 44.7 ms                                                                | 46.9 ms: 1.05x slower                                                   |
| generators                 | 28.0 ms                                                                | 29.6 ms: 1.06x slower                                                   |
| mdp                        | 1.17 sec                                                               | 1.24 sec: 1.06x slower                                                  |
| thrift                     | 742 us                                                                 | 787 us: 1.06x slower                                                    |
| logging_format             | 6.59 us                                                                | 7.02 us: 1.07x slower                                                   |
| sqlglot_v2_normalize       | 102 ms                                                                 | 109 ms: 1.07x slower                                                    |
| genshi_xml                 | 49.7 ms                                                                | 53.0 ms: 1.07x slower                                                   |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 512 ms: 1.07x slower                                                    |
| gc_traversal               | 4.32 ms                                                                | 4.64 ms: 1.07x slower                                                   |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 520 ms: 1.08x slower                                                    |
| dulwich_log                | 68.5 ms                                                                | 74.2 ms: 1.08x slower                                                   |
| logging_simple             | 5.78 us                                                                | 6.27 us: 1.08x slower                                                   |
| nqueens                    | 79.2 ms                                                                | 86.3 ms: 1.09x slower                                                   |
| pycparser                  | 1.08 sec                                                               | 1.18 sec: 1.09x slower                                                  |
| pidigits                   | 194 ms                                                                 | 216 ms: 1.11x slower                                                    |
| raytrace                   | 251 ms                                                                 | 279 ms: 1.11x slower                                                    |
| html5lib                   | 60.7 ms                                                                | 69.3 ms: 1.14x slower                                                   |
| pathlib                    | 17.6 ms                                                                | 20.4 ms: 1.16x slower                                                   |
| go                         | 107 ms                                                                 | 124 ms: 1.16x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (12): meteor_contest, xml_etree_parse, bench_mp_pool, connected_components, python_startup, asyncio_websockets, mako, shortest_path, fannkuch, nbody, pprint_safe_repr, async_tree_io

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x