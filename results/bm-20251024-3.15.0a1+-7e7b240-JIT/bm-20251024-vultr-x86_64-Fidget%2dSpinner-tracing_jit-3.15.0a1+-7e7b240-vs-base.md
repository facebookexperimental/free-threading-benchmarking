# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 7e7b240
- commit date: 2025-10-24
- overall geometric mean: 1.000x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 256 ms: 1.01x slower                                                    |
| docutils       | 2.60 sec                                                               | 2.67 sec: 1.03x slower                                                  |
| html5lib       | 60.7 ms                                                                | 70.2 ms: 1.16x slower                                                   |
| sphinx         | 989 ms                                                                 | 1.00 sec: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 591 ms                                                                 | 596 ms: 1.01x slower                                                    |
| async_tree_memoization_tg  | 305 ms                                                                 | 308 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 243 ms                                                                 | 247 ms: 1.02x slower                                                    |
| async_generators           | 367 ms                                                                 | 374 ms: 1.02x slower                                                    |
| async_tree_none            | 243 ms                                                                 | 248 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 488 ms: 1.02x slower                                                    |
| coroutines                 | 23.9 ms                                                                | 24.4 ms: 1.02x slower                                                   |
| async_tree_memoization     | 304 ms                                                                 | 310 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 491 ms: 1.02x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.9 ms                                                                | 61.9 ms: 1.16x faster                                                   |
| nbody          | 92.6 ms                                                                | 91.1 ms: 1.02x faster                                                   |
| pidigits       | 194 ms                                                                 | 193 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 23.1 ms                                                                | 22.3 ms: 1.04x faster                                                   |
| regex_effbot   | 2.86 ms                                                                | 2.80 ms: 1.02x faster                                                   |
| regex_dna      | 187 ms                                                                 | 185 ms: 1.01x faster                                                    |
| regex_compile  | 124 ms                                                                 | 131 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 85.2 ms                                                                | 83.3 ms: 1.02x faster                                                   |
| json_dumps           | 9.46 ms                                                                | 9.55 ms: 1.01x slower                                                   |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                    |
| json_loads           | 27.9 us                                                                | 28.2 us: 1.01x slower                                                   |
| xml_etree_process    | 53.7 ms                                                                | 55.5 ms: 1.03x slower                                                   |
| unpickle_pure_python | 183 us                                                                 | 190 us: 1.04x slower                                                    |
| xml_etree_generate   | 77.1 ms                                                                | 80.2 ms: 1.04x slower                                                   |
| tomli_loads          | 1.72 sec                                                               | 1.82 sec: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.25 ms                                                                | 7.30 ms: 1.01x slower                                                   |
| python_startup         | 12.4 ms                                                                | 12.6 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.5 ms                                                                | 10.8 ms: 1.02x slower                                                   |
| genshi_text     | 20.8 ms                                                                | 21.7 ms: 1.04x slower                                                   |
| django_template | 34.5 ms                                                                | 36.3 ms: 1.05x slower                                                   |
| genshi_xml      | 49.7 ms                                                                | 53.7 ms: 1.08x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7e7b240 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 40.8 ms                                                                | 22.5 ms: 1.82x faster                                                   |
| richards_super             | 46.7 ms                                                                | 27.3 ms: 1.71x faster                                                   |
| float                      | 71.9 ms                                                                | 61.9 ms: 1.16x faster                                                   |
| spectral_norm              | 99.1 ms                                                                | 85.4 ms: 1.16x faster                                                   |
| deltablue                  | 3.28 ms                                                                | 2.83 ms: 1.16x faster                                                   |
| logging_silent             | 101 ns                                                                 | 88.2 ns: 1.15x faster                                                   |
| deepcopy_memo              | 26.8 us                                                                | 23.9 us: 1.12x faster                                                   |
| scimark_sor                | 109 ms                                                                 | 99.2 ms: 1.10x faster                                                   |
| scimark_lu                 | 111 ms                                                                 | 103 ms: 1.08x faster                                                    |
| scimark_monte_carlo        | 61.8 ms                                                                | 57.9 ms: 1.07x faster                                                   |
| comprehensions             | 16.3 us                                                                | 15.3 us: 1.06x faster                                                   |
| crypto_pyaes               | 68.6 ms                                                                | 65.4 ms: 1.05x faster                                                   |
| pyflate                    | 401 ms                                                                 | 385 ms: 1.04x faster                                                    |
| chaos                      | 56.5 ms                                                                | 54.4 ms: 1.04x faster                                                   |
| regex_v8                   | 23.1 ms                                                                | 22.3 ms: 1.04x faster                                                   |
| deepcopy_reduce            | 2.66 us                                                                | 2.58 us: 1.03x faster                                                   |
| xml_etree_iterparse        | 85.2 ms                                                                | 83.3 ms: 1.02x faster                                                   |
| regex_effbot               | 2.86 ms                                                                | 2.80 ms: 1.02x faster                                                   |
| nbody                      | 92.6 ms                                                                | 91.1 ms: 1.02x faster                                                   |
| coverage                   | 82.3 ms                                                                | 81.5 ms: 1.01x faster                                                   |
| regex_dna                  | 187 ms                                                                 | 185 ms: 1.01x faster                                                    |
| shortest_path              | 440 ms                                                                 | 437 ms: 1.01x faster                                                    |
| k_core                     | 1.88 sec                                                               | 1.87 sec: 1.01x faster                                                  |
| pidigits                   | 194 ms                                                                 | 193 ms: 1.01x faster                                                    |
| bpe_tokeniser              | 4.01 sec                                                               | 4.04 sec: 1.01x slower                                                  |
| python_startup_no_site     | 7.25 ms                                                                | 7.30 ms: 1.01x slower                                                   |
| bench_thread_pool          | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                   |
| async_tree_io_tg           | 591 ms                                                                 | 596 ms: 1.01x slower                                                    |
| json_dumps                 | 9.46 ms                                                                | 9.55 ms: 1.01x slower                                                   |
| async_tree_memoization_tg  | 305 ms                                                                 | 308 ms: 1.01x slower                                                    |
| meteor_contest             | 99.9 ms                                                                | 101 ms: 1.01x slower                                                    |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                    |
| python_startup             | 12.4 ms                                                                | 12.6 ms: 1.01x slower                                                   |
| json_loads                 | 27.9 us                                                                | 28.2 us: 1.01x slower                                                   |
| 2to3                       | 253 ms                                                                 | 256 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.19 us                                                                | 2.22 us: 1.01x slower                                                   |
| hexiom                     | 5.88 ms                                                                | 5.97 ms: 1.02x slower                                                   |
| async_tree_none_tg         | 243 ms                                                                 | 247 ms: 1.02x slower                                                    |
| sphinx                     | 989 ms                                                                 | 1.00 sec: 1.02x slower                                                  |
| scimark_fft                | 262 ms                                                                 | 266 ms: 1.02x slower                                                    |
| async_generators           | 367 ms                                                                 | 374 ms: 1.02x slower                                                    |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.23 ms: 1.02x slower                                                   |
| async_tree_none            | 243 ms                                                                 | 248 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 488 ms: 1.02x slower                                                    |
| coroutines                 | 23.9 ms                                                                | 24.4 ms: 1.02x slower                                                   |
| sympy_integrate            | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                   |
| async_tree_memoization     | 304 ms                                                                 | 310 ms: 1.02x slower                                                    |
| mako                       | 10.5 ms                                                                | 10.8 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 491 ms: 1.02x slower                                                    |
| telco                      | 158 ms                                                                 | 162 ms: 1.02x slower                                                    |
| pylint                     | 292 ms                                                                 | 300 ms: 1.03x slower                                                    |
| generators                 | 28.0 ms                                                                | 28.8 ms: 1.03x slower                                                   |
| docutils                   | 2.60 sec                                                               | 2.67 sec: 1.03x slower                                                  |
| pprint_safe_repr           | 686 ms                                                                 | 706 ms: 1.03x slower                                                    |
| deepcopy                   | 249 us                                                                 | 256 us: 1.03x slower                                                    |
| sqlglot_v2_optimize        | 51.7 ms                                                                | 53.2 ms: 1.03x slower                                                   |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.56 ms: 1.03x slower                                                   |
| sympy_sum                  | 157 ms                                                                 | 162 ms: 1.03x slower                                                    |
| pprint_pformat             | 1.41 sec                                                               | 1.46 sec: 1.03x slower                                                  |
| xml_etree_process          | 53.7 ms                                                                | 55.5 ms: 1.03x slower                                                   |
| unpickle_pure_python       | 183 us                                                                 | 190 us: 1.04x slower                                                    |
| thrift                     | 742 us                                                                 | 768 us: 1.04x slower                                                    |
| xml_etree_generate         | 77.1 ms                                                                | 80.2 ms: 1.04x slower                                                   |
| genshi_text                | 20.8 ms                                                                | 21.7 ms: 1.04x slower                                                   |
| many_optionals             | 1.25 ms                                                                | 1.30 ms: 1.04x slower                                                   |
| sympy_expand               | 489 ms                                                                 | 509 ms: 1.04x slower                                                    |
| sympy_str                  | 282 ms                                                                 | 294 ms: 1.04x slower                                                    |
| mdp                        | 1.17 sec                                                               | 1.23 sec: 1.05x slower                                                  |
| django_template            | 34.5 ms                                                                | 36.3 ms: 1.05x slower                                                   |
| tomli_loads                | 1.72 sec                                                               | 1.82 sec: 1.06x slower                                                  |
| regex_compile              | 124 ms                                                                 | 131 ms: 1.06x slower                                                    |
| subparsers                 | 44.7 ms                                                                | 47.4 ms: 1.06x slower                                                   |
| logging_format             | 6.59 us                                                                | 7.08 us: 1.07x slower                                                   |
| genshi_xml                 | 49.7 ms                                                                | 53.7 ms: 1.08x slower                                                   |
| sqlglot_v2_normalize       | 102 ms                                                                 | 110 ms: 1.08x slower                                                    |
| nqueens                    | 79.2 ms                                                                | 85.7 ms: 1.08x slower                                                   |
| dulwich_log                | 68.5 ms                                                                | 74.3 ms: 1.09x slower                                                   |
| logging_simple             | 5.78 us                                                                | 6.32 us: 1.09x slower                                                   |
| pycparser                  | 1.08 sec                                                               | 1.19 sec: 1.10x slower                                                  |
| raytrace                   | 251 ms                                                                 | 279 ms: 1.11x slower                                                    |
| pathlib                    | 17.6 ms                                                                | 20.3 ms: 1.15x slower                                                   |
| html5lib                   | 60.7 ms                                                                | 70.2 ms: 1.16x slower                                                   |
| go                         | 107 ms                                                                 | 123 ms: 1.16x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (11): typing_runtime_protocols, create_gc_cycles, connected_components, asyncio_websockets, json, pickle_pure_python, gc_traversal, bench_mp_pool, fannkuch, scimark_sparse_mat_mult, async_tree_io

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x