# Results vs. base

- fork: mpage
- ref: gh_XXX_noinline
- machine: linux-x86_64
- commit hash: a851750
- commit date: 2025-04-09
- overall geometric mean: 1.036x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 289 ms                                                                 | 279 ms: 1.04x faster                                             |
| docutils       | 2.77 sec                                                               | 2.69 sec: 1.03x faster                                           |
| html5lib       | 70.5 ms                                                                | 64.8 ms: 1.09x faster                                            |
| sphinx         | 1.09 sec                                                               | 1.06 sec: 1.03x faster                                           |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_none            | 268 ms                                                                 | 254 ms: 1.06x faster                                             |
| async_tree_memoization_tg  | 292 ms                                                                 | 278 ms: 1.05x faster                                             |
| async_tree_none_tg         | 233 ms                                                                 | 223 ms: 1.05x faster                                             |
| async_tree_memoization     | 321 ms                                                                 | 307 ms: 1.05x faster                                             |
| async_tree_io              | 562 ms                                                                 | 538 ms: 1.04x faster                                             |
| async_tree_io_tg           | 534 ms                                                                 | 513 ms: 1.04x faster                                             |
| coroutines                 | 23.3 ms                                                                | 22.4 ms: 1.04x faster                                            |
| async_generators           | 368 ms                                                                 | 356 ms: 1.03x faster                                             |
| async_tree_cpu_io_mixed    | 508 ms                                                                 | 542 ms: 1.07x slower                                             |
| async_tree_cpu_io_mixed_tg | 478 ms                                                                 | 515 ms: 1.08x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                     |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 114 ms                                                                 | 109 ms: 1.05x faster                                             |
| float          | 70.3 ms                                                                | 67.3 ms: 1.05x faster                                            |
| pidigits       | 193 ms                                                                 | 222 ms: 1.15x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 152 ms                                                                 | 142 ms: 1.07x faster                                             |
| regex_dna      | 184 ms                                                                 | 174 ms: 1.06x faster                                             |
| regex_effbot   | 2.73 ms                                                                | 2.83 ms: 1.03x slower                                            |
| regex_v8       | 21.1 ms                                                                | 22.0 ms: 1.04x slower                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| unpickle_pure_python | 241 us                                                                 | 224 us: 1.07x faster                                             |
| pickle_pure_python   | 342 us                                                                 | 323 us: 1.06x faster                                             |
| xml_etree_process    | 68.5 ms                                                                | 65.6 ms: 1.04x faster                                            |
| tomli_loads          | 2.18 sec                                                               | 2.09 sec: 1.04x faster                                           |
| xml_etree_iterparse  | 86.5 ms                                                                | 83.9 ms: 1.03x faster                                            |
| xml_etree_generate   | 94.7 ms                                                                | 91.9 ms: 1.03x faster                                            |
| json_dumps           | 12.8 ms                                                                | 12.6 ms: 1.02x faster                                            |
| xml_etree_parse      | 128 ms                                                                 | 128 ms: 1.01x faster                                             |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                     |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                            |
| python_startup         | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                            |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| genshi_text     | 27.5 ms                                                                | 25.6 ms: 1.08x faster                                            |
| django_template | 42.0 ms                                                                | 39.6 ms: 1.06x faster                                            |
| genshi_xml      | 58.3 ms                                                                | 54.9 ms: 1.06x faster                                            |
| mako            | 15.6 ms                                                                | 15.0 ms: 1.04x faster                                            |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7+-1f5682f | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| logging_silent             | 110 ns                                                                 | 99.0 ns: 1.11x faster                                            |
| hexiom                     | 7.07 ms                                                                | 6.48 ms: 1.09x faster                                            |
| html5lib                   | 70.5 ms                                                                | 64.8 ms: 1.09x faster                                            |
| deltablue                  | 3.76 ms                                                                | 3.46 ms: 1.09x faster                                            |
| generators                 | 32.0 ms                                                                | 29.4 ms: 1.09x faster                                            |
| go                         | 134 ms                                                                 | 124 ms: 1.08x faster                                             |
| scimark_sparse_mat_mult    | 5.26 ms                                                                | 4.87 ms: 1.08x faster                                            |
| spectral_norm              | 108 ms                                                                 | 100 ms: 1.08x faster                                             |
| genshi_text                | 27.5 ms                                                                | 25.6 ms: 1.08x faster                                            |
| unpickle_pure_python       | 241 us                                                                 | 224 us: 1.07x faster                                             |
| richards                   | 53.7 ms                                                                | 50.1 ms: 1.07x faster                                            |
| richards_super             | 61.7 ms                                                                | 57.5 ms: 1.07x faster                                            |
| scimark_sor                | 128 ms                                                                 | 119 ms: 1.07x faster                                             |
| regex_compile              | 152 ms                                                                 | 142 ms: 1.07x faster                                             |
| raytrace                   | 304 ms                                                                 | 285 ms: 1.07x faster                                             |
| pyflate                    | 486 ms                                                                 | 456 ms: 1.07x faster                                             |
| django_template            | 42.0 ms                                                                | 39.6 ms: 1.06x faster                                            |
| genshi_xml                 | 58.3 ms                                                                | 54.9 ms: 1.06x faster                                            |
| logging_simple             | 7.36 us                                                                | 6.95 us: 1.06x faster                                            |
| pickle_pure_python         | 342 us                                                                 | 323 us: 1.06x faster                                             |
| regex_dna                  | 184 ms                                                                 | 174 ms: 1.06x faster                                             |
| scimark_fft                | 354 ms                                                                 | 335 ms: 1.06x faster                                             |
| logging_format             | 8.27 us                                                                | 7.83 us: 1.06x faster                                            |
| chaos                      | 63.8 ms                                                                | 60.4 ms: 1.06x faster                                            |
| sqlglot_v2_parse           | 1.53 ms                                                                | 1.45 ms: 1.06x faster                                            |
| async_tree_none            | 268 ms                                                                 | 254 ms: 1.06x faster                                             |
| deepcopy_memo              | 36.9 us                                                                | 34.9 us: 1.06x faster                                            |
| scimark_lu                 | 134 ms                                                                 | 127 ms: 1.05x faster                                             |
| nbody                      | 114 ms                                                                 | 109 ms: 1.05x faster                                             |
| nqueens                    | 88.4 ms                                                                | 84.0 ms: 1.05x faster                                            |
| sqlglot_v2_normalize       | 118 ms                                                                 | 112 ms: 1.05x faster                                             |
| pprint_pformat             | 1.65 sec                                                               | 1.57 sec: 1.05x faster                                           |
| sqlglot_v2_transpile       | 1.84 ms                                                                | 1.75 ms: 1.05x faster                                            |
| async_tree_memoization_tg  | 292 ms                                                                 | 278 ms: 1.05x faster                                             |
| pprint_safe_repr           | 792 ms                                                                 | 755 ms: 1.05x faster                                             |
| deepcopy                   | 299 us                                                                 | 285 us: 1.05x faster                                             |
| async_tree_none_tg         | 233 ms                                                                 | 223 ms: 1.05x faster                                             |
| async_tree_memoization     | 321 ms                                                                 | 307 ms: 1.05x faster                                             |
| float                      | 70.3 ms                                                                | 67.3 ms: 1.05x faster                                            |
| mdp                        | 1.35 sec                                                               | 1.29 sec: 1.05x faster                                           |
| xml_etree_process          | 68.5 ms                                                                | 65.6 ms: 1.04x faster                                            |
| scimark_monte_carlo        | 76.7 ms                                                                | 73.5 ms: 1.04x faster                                            |
| sqlglot_v2_optimize        | 59.3 ms                                                                | 56.9 ms: 1.04x faster                                            |
| async_tree_io              | 562 ms                                                                 | 538 ms: 1.04x faster                                             |
| async_tree_io_tg           | 534 ms                                                                 | 513 ms: 1.04x faster                                             |
| tomli_loads                | 2.18 sec                                                               | 2.09 sec: 1.04x faster                                           |
| comprehensions             | 20.0 us                                                                | 19.3 us: 1.04x faster                                            |
| mako                       | 15.6 ms                                                                | 15.0 ms: 1.04x faster                                            |
| sympy_expand               | 545 ms                                                                 | 524 ms: 1.04x faster                                             |
| subparsers                 | 25.3 ms                                                                | 24.3 ms: 1.04x faster                                            |
| coroutines                 | 23.3 ms                                                                | 22.4 ms: 1.04x faster                                            |
| sqlalchemy_imperative      | 24.3 ms                                                                | 23.4 ms: 1.04x faster                                            |
| crypto_pyaes               | 85.2 ms                                                                | 82.0 ms: 1.04x faster                                            |
| many_optionals             | 1.16 ms                                                                | 1.11 ms: 1.04x faster                                            |
| sympy_str                  | 329 ms                                                                 | 317 ms: 1.04x faster                                             |
| pylint                     | 316 ms                                                                 | 305 ms: 1.04x faster                                             |
| sympy_integrate            | 23.0 ms                                                                | 22.2 ms: 1.04x faster                                            |
| sympy_sum                  | 184 ms                                                                 | 178 ms: 1.04x faster                                             |
| 2to3                       | 289 ms                                                                 | 279 ms: 1.04x faster                                             |
| async_generators           | 368 ms                                                                 | 356 ms: 1.03x faster                                             |
| dulwich_log                | 73.2 ms                                                                | 70.8 ms: 1.03x faster                                            |
| deepcopy_reduce            | 3.01 us                                                                | 2.91 us: 1.03x faster                                            |
| create_gc_cycles           | 1.37 ms                                                                | 1.33 ms: 1.03x faster                                            |
| xml_etree_iterparse        | 86.5 ms                                                                | 83.9 ms: 1.03x faster                                            |
| fannkuch                   | 459 ms                                                                 | 446 ms: 1.03x faster                                             |
| xml_etree_generate         | 94.7 ms                                                                | 91.9 ms: 1.03x faster                                            |
| sphinx                     | 1.09 sec                                                               | 1.06 sec: 1.03x faster                                           |
| meteor_contest             | 127 ms                                                                 | 124 ms: 1.03x faster                                             |
| docutils                   | 2.77 sec                                                               | 2.69 sec: 1.03x faster                                           |
| pycparser                  | 1.17 sec                                                               | 1.14 sec: 1.03x faster                                           |
| gc_traversal               | 1.82 ms                                                                | 1.77 ms: 1.03x faster                                            |
| sqlalchemy_declarative     | 157 ms                                                                 | 153 ms: 1.02x faster                                             |
| typing_runtime_protocols   | 194 us                                                                 | 190 us: 1.02x faster                                             |
| pathlib                    | 19.7 ms                                                                | 19.3 ms: 1.02x faster                                            |
| json_dumps                 | 12.8 ms                                                                | 12.6 ms: 1.02x faster                                            |
| bpe_tokeniser              | 4.55 sec                                                               | 4.47 sec: 1.02x faster                                           |
| bench_mp_pool              | 96.3 ms                                                                | 94.7 ms: 1.02x faster                                            |
| sqlite_synth               | 2.03 us                                                                | 2.00 us: 1.02x faster                                            |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                            |
| python_startup             | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                            |
| k_core                     | 2.25 sec                                                               | 2.23 sec: 1.01x faster                                           |
| xml_etree_parse            | 128 ms                                                                 | 128 ms: 1.01x faster                                             |
| bench_thread_pool          | 3.15 ms                                                                | 3.13 ms: 1.00x faster                                            |
| regex_effbot               | 2.73 ms                                                                | 2.83 ms: 1.03x slower                                            |
| regex_v8                   | 21.1 ms                                                                | 22.0 ms: 1.04x slower                                            |
| async_tree_cpu_io_mixed    | 508 ms                                                                 | 542 ms: 1.07x slower                                             |
| async_tree_cpu_io_mixed_tg | 478 ms                                                                 | 515 ms: 1.08x slower                                             |
| pidigits                   | 193 ms                                                                 | 222 ms: 1.15x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                     |

Benchmark hidden because not significant (7): connected_components, telco, shortest_path, asyncio_websockets, coverage, json_loads, json

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.00x