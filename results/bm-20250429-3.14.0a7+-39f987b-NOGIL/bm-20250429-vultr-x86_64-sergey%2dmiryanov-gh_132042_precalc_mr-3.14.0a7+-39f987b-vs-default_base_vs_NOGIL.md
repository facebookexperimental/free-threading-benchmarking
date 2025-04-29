# Results vs. default_base_vs_NOGIL

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.081x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 279 ms: 1.12x slower                                                              |
| docutils       | 2.53 sec                                                               | 2.70 sec: 1.07x slower                                                            |
| sphinx         | 977 ms                                                                 | 1.07 sec: 1.09x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 603 ms                                                                 | 526 ms: 1.14x faster                                                              |
| async_tree_none_tg         | 253 ms                                                                 | 227 ms: 1.11x faster                                                              |
| async_tree_io              | 606 ms                                                                 | 550 ms: 1.10x faster                                                              |
| async_tree_memoization_tg  | 311 ms                                                                 | 285 ms: 1.09x faster                                                              |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 478 ms: 1.05x faster                                                              |
| async_tree_none            | 270 ms                                                                 | 258 ms: 1.05x faster                                                              |
| async_tree_cpu_io_mixed    | 513 ms                                                                 | 503 ms: 1.02x faster                                                              |
| async_tree_memoization     | 307 ms                                                                 | 311 ms: 1.01x slower                                                              |
| async_generators           | 332 ms                                                                 | 368 ms: 1.11x slower                                                              |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                                      |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 69.5 ms                                                                | 66.8 ms: 1.04x faster                                                             |
| pidigits       | 190 ms                                                                 | 199 ms: 1.04x slower                                                              |
| nbody          | 86.7 ms                                                                | 110 ms: 1.27x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_v8       | 22.1 ms                                                                | 20.3 ms: 1.09x faster                                                             |
| regex_dna      | 183 ms                                                                 | 177 ms: 1.04x faster                                                              |
| regex_effbot   | 2.80 ms                                                                | 2.78 ms: 1.01x faster                                                             |
| regex_compile  | 123 ms                                                                 | 144 ms: 1.17x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.1 ms                                                                | 87.6 ms: 1.05x faster                                                             |
| xml_etree_parse      | 131 ms                                                                 | 129 ms: 1.02x faster                                                              |
| pickle_pure_python   | 303 us                                                                 | 327 us: 1.08x slower                                                              |
| unpickle_pure_python | 209 us                                                                 | 226 us: 1.08x slower                                                              |
| json_loads           | 27.6 us                                                                | 30.1 us: 1.09x slower                                                             |
| json_dumps           | 11.5 ms                                                                | 12.7 ms: 1.11x slower                                                             |
| xml_etree_generate   | 82.2 ms                                                                | 92.7 ms: 1.13x slower                                                             |
| tomli_loads          | 1.85 sec                                                               | 2.09 sec: 1.13x slower                                                            |
| xml_etree_process    | 57.8 ms                                                                | 66.1 ms: 1.14x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                | 15.4 ms: 1.03x slower                                                             |
| python_startup_no_site | 7.29 ms                                                                | 9.19 ms: 1.26x slower                                                             |
| Geometric mean         | (ref)                                                                  | 1.14x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_xml      | 48.2 ms                                                                | 55.1 ms: 1.14x slower                                                             |
| django_template | 33.8 ms                                                                | 39.7 ms: 1.17x slower                                                             |
| genshi_text     | 20.7 ms                                                                | 26.0 ms: 1.25x slower                                                             |
| mako            | 12.0 ms                                                                | 15.4 ms: 1.28x slower                                                             |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| gc_traversal               | 4.57 ms                                                                | 1.78 ms: 2.57x faster                                                             |
| create_gc_cycles           | 1.84 ms                                                                | 1.36 ms: 1.36x faster                                                             |
| async_tree_io_tg           | 603 ms                                                                 | 526 ms: 1.14x faster                                                              |
| async_tree_none_tg         | 253 ms                                                                 | 227 ms: 1.11x faster                                                              |
| async_tree_io              | 606 ms                                                                 | 550 ms: 1.10x faster                                                              |
| sqlite_synth               | 2.21 us                                                                | 2.02 us: 1.10x faster                                                             |
| async_tree_memoization_tg  | 311 ms                                                                 | 285 ms: 1.09x faster                                                              |
| regex_v8                   | 22.1 ms                                                                | 20.3 ms: 1.09x faster                                                             |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 478 ms: 1.05x faster                                                              |
| xml_etree_iterparse        | 92.1 ms                                                                | 87.6 ms: 1.05x faster                                                             |
| async_tree_none            | 270 ms                                                                 | 258 ms: 1.05x faster                                                              |
| float                      | 69.5 ms                                                                | 66.8 ms: 1.04x faster                                                             |
| regex_dna                  | 183 ms                                                                 | 177 ms: 1.04x faster                                                              |
| async_tree_cpu_io_mixed    | 513 ms                                                                 | 503 ms: 1.02x faster                                                              |
| xml_etree_parse            | 131 ms                                                                 | 129 ms: 1.02x faster                                                              |
| regex_effbot               | 2.80 ms                                                                | 2.78 ms: 1.01x faster                                                             |
| async_tree_memoization     | 307 ms                                                                 | 311 ms: 1.01x slower                                                              |
| pycparser                  | 1.10 sec                                                               | 1.13 sec: 1.02x slower                                                            |
| json                       | 4.96 ms                                                                | 5.08 ms: 1.03x slower                                                             |
| python_startup             | 14.9 ms                                                                | 15.4 ms: 1.03x slower                                                             |
| dulwich_log                | 67.5 ms                                                                | 70.5 ms: 1.04x slower                                                             |
| pidigits                   | 190 ms                                                                 | 199 ms: 1.04x slower                                                              |
| scimark_fft                | 319 ms                                                                 | 338 ms: 1.06x slower                                                              |
| scimark_sparse_mat_mult    | 4.63 ms                                                                | 4.90 ms: 1.06x slower                                                             |
| bpe_tokeniser              | 4.12 sec                                                               | 4.37 sec: 1.06x slower                                                            |
| bench_mp_pool              | 88.4 ms                                                                | 94.1 ms: 1.06x slower                                                             |
| docutils                   | 2.53 sec                                                               | 2.70 sec: 1.07x slower                                                            |
| pickle_pure_python         | 303 us                                                                 | 327 us: 1.08x slower                                                              |
| unpickle_pure_python       | 209 us                                                                 | 226 us: 1.08x slower                                                              |
| scimark_sor                | 109 ms                                                                 | 118 ms: 1.09x slower                                                              |
| logging_silent             | 96.6 ns                                                                | 105 ns: 1.09x slower                                                              |
| spectral_norm              | 95.4 ms                                                                | 104 ms: 1.09x slower                                                              |
| deltablue                  | 3.24 ms                                                                | 3.53 ms: 1.09x slower                                                             |
| json_loads                 | 27.6 us                                                                | 30.1 us: 1.09x slower                                                             |
| sphinx                     | 977 ms                                                                 | 1.07 sec: 1.09x slower                                                            |
| pylint                     | 278 ms                                                                 | 305 ms: 1.10x slower                                                              |
| many_optionals             | 1.00 ms                                                                | 1.10 ms: 1.10x slower                                                             |
| generators                 | 28.0 ms                                                                | 30.8 ms: 1.10x slower                                                             |
| k_core                     | 2.03 sec                                                               | 2.23 sec: 1.10x slower                                                            |
| json_dumps                 | 11.5 ms                                                                | 12.7 ms: 1.11x slower                                                             |
| async_generators           | 332 ms                                                                 | 368 ms: 1.11x slower                                                              |
| nqueens                    | 76.4 ms                                                                | 85.4 ms: 1.12x slower                                                             |
| pprint_safe_repr           | 691 ms                                                                 | 774 ms: 1.12x slower                                                              |
| 2to3                       | 248 ms                                                                 | 279 ms: 1.12x slower                                                              |
| pyflate                    | 405 ms                                                                 | 455 ms: 1.12x slower                                                              |
| xml_etree_generate         | 82.2 ms                                                                | 92.7 ms: 1.13x slower                                                             |
| subparsers                 | 21.9 ms                                                                | 24.7 ms: 1.13x slower                                                             |
| tomli_loads                | 1.85 sec                                                               | 2.09 sec: 1.13x slower                                                            |
| chaos                      | 53.3 ms                                                                | 60.6 ms: 1.14x slower                                                             |
| pprint_pformat             | 1.41 sec                                                               | 1.60 sec: 1.14x slower                                                            |
| genshi_xml                 | 48.2 ms                                                                | 55.1 ms: 1.14x slower                                                             |
| xml_etree_process          | 57.8 ms                                                                | 66.1 ms: 1.14x slower                                                             |
| deepcopy_reduce            | 2.60 us                                                                | 2.99 us: 1.15x slower                                                             |
| sqlglot_v2_normalize       | 98.9 ms                                                                | 114 ms: 1.15x slower                                                              |
| go                         | 108 ms                                                                 | 125 ms: 1.15x slower                                                              |
| mdp                        | 1.13 sec                                                               | 1.30 sec: 1.16x slower                                                            |
| sqlglot_v2_optimize        | 49.9 ms                                                                | 57.7 ms: 1.16x slower                                                             |
| scimark_lu                 | 111 ms                                                                 | 129 ms: 1.16x slower                                                              |
| hexiom                     | 5.76 ms                                                                | 6.71 ms: 1.16x slower                                                             |
| comprehensions             | 16.7 us                                                                | 19.4 us: 1.17x slower                                                             |
| raytrace                   | 246 ms                                                                 | 288 ms: 1.17x slower                                                              |
| regex_compile              | 123 ms                                                                 | 144 ms: 1.17x slower                                                              |
| django_template            | 33.8 ms                                                                | 39.7 ms: 1.17x slower                                                             |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.77 ms: 1.17x slower                                                             |
| sqlalchemy_declarative     | 130 ms                                                                 | 153 ms: 1.17x slower                                                              |
| telco                      | 7.11 ms                                                                | 8.36 ms: 1.18x slower                                                             |
| sympy_sum                  | 151 ms                                                                 | 178 ms: 1.18x slower                                                              |
| sympy_expand               | 449 ms                                                                 | 530 ms: 1.18x slower                                                              |
| deepcopy                   | 247 us                                                                 | 291 us: 1.18x slower                                                              |
| sympy_str                  | 266 ms                                                                 | 315 ms: 1.18x slower                                                              |
| sympy_integrate            | 18.7 ms                                                                | 22.1 ms: 1.18x slower                                                             |
| scimark_monte_carlo        | 62.0 ms                                                                | 73.4 ms: 1.18x slower                                                             |
| sqlalchemy_imperative      | 19.7 ms                                                                | 23.4 ms: 1.19x slower                                                             |
| fannkuch                   | 380 ms                                                                 | 454 ms: 1.20x slower                                                              |
| deepcopy_memo              | 28.8 us                                                                | 34.5 us: 1.20x slower                                                             |
| crypto_pyaes               | 68.9 ms                                                                | 82.6 ms: 1.20x slower                                                             |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.46 ms: 1.20x slower                                                             |
| connected_components       | 396 ms                                                                 | 482 ms: 1.22x slower                                                              |
| shortest_path              | 434 ms                                                                 | 530 ms: 1.22x slower                                                              |
| logging_simple             | 5.85 us                                                                | 7.14 us: 1.22x slower                                                             |
| richards                   | 40.4 ms                                                                | 49.5 ms: 1.23x slower                                                             |
| logging_format             | 6.54 us                                                                | 8.07 us: 1.24x slower                                                             |
| typing_runtime_protocols   | 154 us                                                                 | 191 us: 1.24x slower                                                              |
| richards_super             | 46.1 ms                                                                | 57.4 ms: 1.24x slower                                                             |
| genshi_text                | 20.7 ms                                                                | 26.0 ms: 1.25x slower                                                             |
| python_startup_no_site     | 7.29 ms                                                                | 9.19 ms: 1.26x slower                                                             |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.26x slower                                                              |
| nbody                      | 86.7 ms                                                                | 110 ms: 1.27x slower                                                              |
| mako                       | 12.0 ms                                                                | 15.4 ms: 1.28x slower                                                             |
| coverage                   | 81.1 ms                                                                | 109 ms: 1.34x slower                                                              |
| bench_thread_pool          | 1.04 ms                                                                | 3.13 ms: 3.00x slower                                                             |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                                      |

Benchmark hidden because not significant (3): coroutines, pathlib, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250429-3.14.0a7+-39f987b-NOGIL/bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: html5lib

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x