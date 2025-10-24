# Results vs. default_base_vs_NOGIL

- fork: kumaraditya303
- ref: interp_tls
- machine: linux-x86_64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 280 ms: 1.13x slower                                                 |
| docutils       | 2.56 sec                                                               | 2.70 sec: 1.05x slower                                               |
| html5lib       | 61.6 ms                                                                | 67.6 ms: 1.10x slower                                                |
| sphinx         | 977 ms                                                                 | 1.07 sec: 1.09x slower                                               |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 588 ms                                                                 | 519 ms: 1.13x faster                                                 |
| async_tree_none_tg         | 245 ms                                                                 | 225 ms: 1.09x faster                                                 |
| async_tree_memoization_tg  | 308 ms                                                                 | 283 ms: 1.09x faster                                                 |
| asyncio_websockets         | 544 ms                                                                 | 509 ms: 1.07x faster                                                 |
| async_tree_io              | 550 ms                                                                 | 540 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed_tg | 481 ms                                                                 | 474 ms: 1.01x faster                                                 |
| async_tree_none            | 246 ms                                                                 | 254 ms: 1.03x slower                                                 |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 499 ms: 1.04x slower                                                 |
| coroutines                 | 24.1 ms                                                                | 25.7 ms: 1.07x slower                                                |
| async_generators           | 344 ms                                                                 | 367 ms: 1.07x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 209 ms                                                                 | 196 ms: 1.07x faster                                                 |
| nbody          | 90.6 ms                                                                | 122 ms: 1.35x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                         |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 22.9 ms                                                                | 21.1 ms: 1.08x faster                                                |
| regex_effbot   | 2.87 ms                                                                | 2.66 ms: 1.08x faster                                                |
| regex_dna      | 184 ms                                                                 | 174 ms: 1.05x faster                                                 |
| regex_compile  | 124 ms                                                                 | 144 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 131 ms: 1.01x slower                                                 |
| xml_etree_iterparse  | 85.3 ms                                                                | 88.5 ms: 1.04x slower                                                |
| tomli_loads          | 1.92 sec                                                               | 2.04 sec: 1.06x slower                                               |
| json_loads           | 28.1 us                                                                | 30.9 us: 1.10x slower                                                |
| unpickle_pure_python | 211 us                                                                 | 235 us: 1.11x slower                                                 |
| pickle_pure_python   | 303 us                                                                 | 339 us: 1.12x slower                                                 |
| json_dumps           | 9.63 ms                                                                | 11.2 ms: 1.16x slower                                                |
| xml_etree_generate   | 82.3 ms                                                                | 95.8 ms: 1.16x slower                                                |
| xml_etree_process    | 58.4 ms                                                                | 68.9 ms: 1.18x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                | 15.7 ms: 1.26x slower                                                |
| python_startup_no_site | 7.26 ms                                                                | 9.54 ms: 1.31x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.29x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 34.6 ms                                                                | 40.3 ms: 1.17x slower                                                |
| genshi_xml      | 48.2 ms                                                                | 56.4 ms: 1.17x slower                                                |
| genshi_text     | 20.7 ms                                                                | 26.5 ms: 1.28x slower                                                |
| mako            | 11.7 ms                                                                | 15.6 ms: 1.33x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.23x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 4.19 ms                                                                | 1.90 ms: 2.20x faster                                                |
| create_gc_cycles           | 1.93 ms                                                                | 1.48 ms: 1.31x faster                                                |
| async_tree_io_tg           | 588 ms                                                                 | 519 ms: 1.13x faster                                                 |
| sqlite_synth               | 2.29 us                                                                | 2.04 us: 1.12x faster                                                |
| async_tree_none_tg         | 245 ms                                                                 | 225 ms: 1.09x faster                                                 |
| async_tree_memoization_tg  | 308 ms                                                                 | 283 ms: 1.09x faster                                                 |
| regex_v8                   | 22.9 ms                                                                | 21.1 ms: 1.08x faster                                                |
| regex_effbot               | 2.87 ms                                                                | 2.66 ms: 1.08x faster                                                |
| asyncio_websockets         | 544 ms                                                                 | 509 ms: 1.07x faster                                                 |
| pidigits                   | 209 ms                                                                 | 196 ms: 1.07x faster                                                 |
| regex_dna                  | 184 ms                                                                 | 174 ms: 1.05x faster                                                 |
| async_tree_io              | 550 ms                                                                 | 540 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed_tg | 481 ms                                                                 | 474 ms: 1.01x faster                                                 |
| pathlib                    | 17.6 ms                                                                | 17.8 ms: 1.01x slower                                                |
| xml_etree_parse            | 129 ms                                                                 | 131 ms: 1.01x slower                                                 |
| async_tree_none            | 246 ms                                                                 | 254 ms: 1.03x slower                                                 |
| bpe_tokeniser              | 4.24 sec                                                               | 4.38 sec: 1.03x slower                                               |
| xml_etree_iterparse        | 85.3 ms                                                                | 88.5 ms: 1.04x slower                                                |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 499 ms: 1.04x slower                                                 |
| json                       | 5.12 ms                                                                | 5.34 ms: 1.04x slower                                                |
| pycparser                  | 1.08 sec                                                               | 1.14 sec: 1.05x slower                                               |
| docutils                   | 2.56 sec                                                               | 2.70 sec: 1.05x slower                                               |
| pylint                     | 289 ms                                                                 | 306 ms: 1.06x slower                                                 |
| tomli_loads                | 1.92 sec                                                               | 2.04 sec: 1.06x slower                                               |
| dulwich_log                | 68.2 ms                                                                | 72.5 ms: 1.06x slower                                                |
| coroutines                 | 24.1 ms                                                                | 25.7 ms: 1.07x slower                                                |
| async_generators           | 344 ms                                                                 | 367 ms: 1.07x slower                                                 |
| sympy_expand               | 482 ms                                                                 | 516 ms: 1.07x slower                                                 |
| logging_silent             | 99.3 ns                                                                | 107 ns: 1.08x slower                                                 |
| sphinx                     | 977 ms                                                                 | 1.07 sec: 1.09x slower                                               |
| html5lib                   | 61.6 ms                                                                | 67.6 ms: 1.10x slower                                                |
| pyflate                    | 418 ms                                                                 | 460 ms: 1.10x slower                                                 |
| json_loads                 | 28.1 us                                                                | 30.9 us: 1.10x slower                                                |
| sympy_str                  | 278 ms                                                                 | 310 ms: 1.11x slower                                                 |
| many_optionals             | 1.23 ms                                                                | 1.37 ms: 1.11x slower                                                |
| unpickle_pure_python       | 211 us                                                                 | 235 us: 1.11x slower                                                 |
| pprint_safe_repr           | 703 ms                                                                 | 785 ms: 1.12x slower                                                 |
| pickle_pure_python         | 303 us                                                                 | 339 us: 1.12x slower                                                 |
| hexiom                     | 5.72 ms                                                                | 6.42 ms: 1.12x slower                                                |
| scimark_fft                | 314 ms                                                                 | 353 ms: 1.12x slower                                                 |
| telco                      | 158 ms                                                                 | 178 ms: 1.12x slower                                                 |
| 2to3                       | 249 ms                                                                 | 280 ms: 1.13x slower                                                 |
| nqueens                    | 78.3 ms                                                                | 88.4 ms: 1.13x slower                                                |
| generators                 | 27.6 ms                                                                | 31.2 ms: 1.13x slower                                                |
| comprehensions             | 15.8 us                                                                | 17.9 us: 1.13x slower                                                |
| chaos                      | 56.4 ms                                                                | 63.9 ms: 1.13x slower                                                |
| sqlglot_v2_normalize       | 101 ms                                                                 | 115 ms: 1.13x slower                                                 |
| pprint_pformat             | 1.42 sec                                                               | 1.62 sec: 1.14x slower                                               |
| sympy_sum                  | 155 ms                                                                 | 177 ms: 1.14x slower                                                 |
| mdp                        | 1.15 sec                                                               | 1.31 sec: 1.14x slower                                               |
| sqlglot_v2_optimize        | 50.8 ms                                                                | 58.1 ms: 1.14x slower                                                |
| fannkuch                   | 395 ms                                                                 | 452 ms: 1.14x slower                                                 |
| deepcopy                   | 245 us                                                                 | 281 us: 1.14x slower                                                 |
| scimark_sparse_mat_mult    | 4.51 ms                                                                | 5.19 ms: 1.15x slower                                                |
| sympy_integrate            | 19.1 ms                                                                | 22.0 ms: 1.15x slower                                                |
| go                         | 106 ms                                                                 | 122 ms: 1.16x slower                                                 |
| json_dumps                 | 9.63 ms                                                                | 11.2 ms: 1.16x slower                                                |
| scimark_lu                 | 111 ms                                                                 | 129 ms: 1.16x slower                                                 |
| regex_compile              | 124 ms                                                                 | 144 ms: 1.16x slower                                                 |
| xml_etree_generate         | 82.3 ms                                                                | 95.8 ms: 1.16x slower                                                |
| django_template            | 34.6 ms                                                                | 40.3 ms: 1.17x slower                                                |
| scimark_sor                | 107 ms                                                                 | 125 ms: 1.17x slower                                                 |
| spectral_norm              | 97.5 ms                                                                | 114 ms: 1.17x slower                                                 |
| subparsers                 | 44.3 ms                                                                | 51.8 ms: 1.17x slower                                                |
| logging_simple             | 5.91 us                                                                | 6.91 us: 1.17x slower                                                |
| deepcopy_memo              | 26.5 us                                                                | 31.0 us: 1.17x slower                                                |
| logging_format             | 6.71 us                                                                | 7.86 us: 1.17x slower                                                |
| genshi_xml                 | 48.2 ms                                                                | 56.4 ms: 1.17x slower                                                |
| deltablue                  | 3.08 ms                                                                | 3.61 ms: 1.17x slower                                                |
| xml_etree_process          | 58.4 ms                                                                | 68.9 ms: 1.18x slower                                                |
| k_core                     | 1.89 sec                                                               | 2.23 sec: 1.18x slower                                               |
| sqlglot_v2_transpile       | 1.49 ms                                                                | 1.77 ms: 1.19x slower                                                |
| raytrace                   | 250 ms                                                                 | 298 ms: 1.19x slower                                                 |
| deepcopy_reduce            | 2.60 us                                                                | 3.10 us: 1.20x slower                                                |
| thrift                     | 747 us                                                                 | 894 us: 1.20x slower                                                 |
| shortest_path              | 445 ms                                                                 | 534 ms: 1.20x slower                                                 |
| meteor_contest             | 99.9 ms                                                                | 121 ms: 1.21x slower                                                 |
| bench_mp_pool              | 12.4 ms                                                                | 15.0 ms: 1.22x slower                                                |
| connected_components       | 401 ms                                                                 | 488 ms: 1.22x slower                                                 |
| sqlglot_v2_parse           | 1.20 ms                                                                | 1.46 ms: 1.22x slower                                                |
| typing_runtime_protocols   | 153 us                                                                 | 187 us: 1.22x slower                                                 |
| crypto_pyaes               | 68.9 ms                                                                | 85.8 ms: 1.24x slower                                                |
| richards                   | 41.4 ms                                                                | 51.8 ms: 1.25x slower                                                |
| richards_super             | 47.4 ms                                                                | 59.6 ms: 1.26x slower                                                |
| python_startup             | 12.4 ms                                                                | 15.7 ms: 1.26x slower                                                |
| genshi_text                | 20.7 ms                                                                | 26.5 ms: 1.28x slower                                                |
| scimark_monte_carlo        | 61.3 ms                                                                | 79.2 ms: 1.29x slower                                                |
| python_startup_no_site     | 7.26 ms                                                                | 9.54 ms: 1.31x slower                                                |
| mako                       | 11.7 ms                                                                | 15.6 ms: 1.33x slower                                                |
| nbody                      | 90.6 ms                                                                | 122 ms: 1.35x slower                                                 |
| coverage                   | 80.6 ms                                                                | 111 ms: 1.37x slower                                                 |
| bench_thread_pool          | 999 us                                                                 | 3.06 ms: 3.06x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.11x slower                                                         |

Benchmark hidden because not significant (2): float, async_tree_memoization

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.20x