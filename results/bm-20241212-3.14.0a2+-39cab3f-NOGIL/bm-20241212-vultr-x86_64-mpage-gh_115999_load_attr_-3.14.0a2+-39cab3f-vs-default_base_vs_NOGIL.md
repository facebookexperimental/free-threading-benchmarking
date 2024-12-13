# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 39cab3f
- commit date: 2024-12-12
- overall geometric mean: 1.200x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 342 ms: 1.35x slower                                                  |
| docutils       | 2.54 sec                                                               | 2.87 sec: 1.13x slower                                                |
| sphinx         | 985 ms                                                                 | 1.13 sec: 1.15x slower                                                |
| Geometric mean | (ref)                                                                  | 1.20x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| async_tree_io_tg           | 617 ms                                                                 | 637 ms: 1.03x slower                                                  |
| async_tree_io              | 631 ms                                                                 | 662 ms: 1.05x slower                                                  |
| async_tree_none_tg         | 258 ms                                                                 | 272 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 524 ms: 1.08x slower                                                  |
| async_tree_cpu_io_mixed    | 504 ms                                                                 | 550 ms: 1.09x slower                                                  |
| async_tree_none            | 280 ms                                                                 | 309 ms: 1.11x slower                                                  |
| async_tree_memoization     | 337 ms                                                                 | 377 ms: 1.12x slower                                                  |
| async_tree_memoization_tg  | 309 ms                                                                 | 346 ms: 1.12x slower                                                  |
| coroutines                 | 21.3 ms                                                                | 24.6 ms: 1.16x slower                                                 |
| async_generators           | 359 ms                                                                 | 423 ms: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 184 ms: 1.01x faster                                                  |
| float          | 76.2 ms                                                                | 109 ms: 1.43x slower                                                  |
| nbody          | 90.7 ms                                                                | 132 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.5 ms                                                                | 24.0 ms: 1.02x slower                                                 |
| regex_effbot   | 2.78 ms                                                                | 2.85 ms: 1.02x slower                                                 |
| regex_dna      | 172 ms                                                                 | 178 ms: 1.04x slower                                                  |
| regex_compile  | 128 ms                                                                 | 161 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.1 ms                                                                | 88.2 ms: 1.02x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 131 ms: 1.03x slower                                                  |
| json_loads           | 26.6 us                                                                | 28.0 us: 1.05x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 13.2 ms: 1.16x slower                                                 |
| xml_etree_generate   | 83.3 ms                                                                | 97.1 ms: 1.17x slower                                                 |
| pickle_pure_python   | 315 us                                                                 | 370 us: 1.18x slower                                                  |
| unpickle_pure_python | 211 us                                                                 | 257 us: 1.22x slower                                                  |
| tomli_loads          | 2.08 sec                                                               | 2.60 sec: 1.25x slower                                                |
| xml_etree_process    | 58.0 ms                                                                | 77.4 ms: 1.33x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 23.6 ms: 1.62x slower                                                 |
| python_startup_no_site | 7.47 ms                                                                | 14.2 ms: 1.90x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.75x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.5 ms                                                                | 61.1 ms: 1.21x slower                                                 |
| django_template | 35.4 ms                                                                | 44.3 ms: 1.25x slower                                                 |
| genshi_text     | 22.0 ms                                                                | 27.9 ms: 1.27x slower                                                 |
| mako            | 11.5 ms                                                                | 15.6 ms: 1.36x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.97 ms                                                                | 3.27 ms: 1.22x faster                                                 |
| sqlite_synth               | 2.20 us                                                                | 2.13 us: 1.03x faster                                                 |
| create_gc_cycles           | 1.82 ms                                                                | 1.78 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 90.1 ms                                                                | 88.2 ms: 1.02x faster                                                 |
| pidigits                   | 186 ms                                                                 | 184 ms: 1.01x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| json                       | 4.82 ms                                                                | 4.93 ms: 1.02x slower                                                 |
| regex_v8                   | 23.5 ms                                                                | 24.0 ms: 1.02x slower                                                 |
| regex_effbot               | 2.78 ms                                                                | 2.85 ms: 1.02x slower                                                 |
| xml_etree_parse            | 128 ms                                                                 | 131 ms: 1.03x slower                                                  |
| async_tree_io_tg           | 617 ms                                                                 | 637 ms: 1.03x slower                                                  |
| regex_dna                  | 172 ms                                                                 | 178 ms: 1.04x slower                                                  |
| async_tree_io              | 631 ms                                                                 | 662 ms: 1.05x slower                                                  |
| async_tree_none_tg         | 258 ms                                                                 | 272 ms: 1.05x slower                                                  |
| json_loads                 | 26.6 us                                                                | 28.0 us: 1.05x slower                                                 |
| pathlib                    | 18.1 ms                                                                | 19.4 ms: 1.07x slower                                                 |
| logging_silent             | 104 ns                                                                 | 112 ns: 1.08x slower                                                  |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 524 ms: 1.08x slower                                                  |
| async_tree_cpu_io_mixed    | 504 ms                                                                 | 550 ms: 1.09x slower                                                  |
| async_tree_none            | 280 ms                                                                 | 309 ms: 1.11x slower                                                  |
| async_tree_memoization     | 337 ms                                                                 | 377 ms: 1.12x slower                                                  |
| async_tree_memoization_tg  | 309 ms                                                                 | 346 ms: 1.12x slower                                                  |
| docutils                   | 2.54 sec                                                               | 2.87 sec: 1.13x slower                                                |
| bpe_tokeniser              | 4.22 sec                                                               | 4.81 sec: 1.14x slower                                                |
| spectral_norm              | 106 ms                                                                 | 121 ms: 1.14x slower                                                  |
| sphinx                     | 985 ms                                                                 | 1.13 sec: 1.15x slower                                                |
| dulwich_log                | 74.6 ms                                                                | 85.8 ms: 1.15x slower                                                 |
| k_core                     | 2.06 sec                                                               | 2.39 sec: 1.16x slower                                                |
| coroutines                 | 21.3 ms                                                                | 24.6 ms: 1.16x slower                                                 |
| many_optionals             | 1.03 ms                                                                | 1.19 ms: 1.16x slower                                                 |
| json_dumps                 | 11.3 ms                                                                | 13.2 ms: 1.16x slower                                                 |
| xml_etree_generate         | 83.3 ms                                                                | 97.1 ms: 1.17x slower                                                 |
| generators                 | 26.6 ms                                                                | 31.2 ms: 1.17x slower                                                 |
| pickle_pure_python         | 315 us                                                                 | 370 us: 1.18x slower                                                  |
| async_generators           | 359 ms                                                                 | 423 ms: 1.18x slower                                                  |
| sqlglot_normalize          | 103 ms                                                                 | 122 ms: 1.19x slower                                                  |
| mdp                        | 2.33 sec                                                               | 2.77 sec: 1.19x slower                                                |
| pycparser                  | 1.11 sec                                                               | 1.34 sec: 1.20x slower                                                |
| telco                      | 7.25 ms                                                                | 8.74 ms: 1.21x slower                                                 |
| subparsers                 | 22.4 ms                                                                | 27.1 ms: 1.21x slower                                                 |
| genshi_xml                 | 50.5 ms                                                                | 61.1 ms: 1.21x slower                                                 |
| sqlglot_optimize           | 51.9 ms                                                                | 63.1 ms: 1.21x slower                                                 |
| scimark_fft                | 327 ms                                                                 | 397 ms: 1.22x slower                                                  |
| unpickle_pure_python       | 211 us                                                                 | 257 us: 1.22x slower                                                  |
| comprehensions             | 17.2 us                                                                | 21.0 us: 1.22x slower                                                 |
| shortest_path              | 440 ms                                                                 | 541 ms: 1.23x slower                                                  |
| deepcopy                   | 255 us                                                                 | 315 us: 1.23x slower                                                  |
| connected_components       | 398 ms                                                                 | 493 ms: 1.24x slower                                                  |
| nqueens                    | 78.6 ms                                                                | 98.1 ms: 1.25x slower                                                 |
| django_template            | 35.4 ms                                                                | 44.3 ms: 1.25x slower                                                 |
| coverage                   | 78.6 ms                                                                | 98.3 ms: 1.25x slower                                                 |
| tomli_loads                | 2.08 sec                                                               | 2.60 sec: 1.25x slower                                                |
| pprint_safe_repr           | 705 ms                                                                 | 882 ms: 1.25x slower                                                  |
| pyflate                    | 435 ms                                                                 | 547 ms: 1.26x slower                                                  |
| regex_compile              | 128 ms                                                                 | 161 ms: 1.26x slower                                                  |
| pprint_pformat             | 1.45 sec                                                               | 1.83 sec: 1.26x slower                                                |
| pylint                     | 278 ms                                                                 | 352 ms: 1.27x slower                                                  |
| genshi_text                | 22.0 ms                                                                | 27.9 ms: 1.27x slower                                                 |
| deepcopy_memo              | 30.1 us                                                                | 38.5 us: 1.28x slower                                                 |
| meteor_contest             | 102 ms                                                                 | 130 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.6 ms                                                                | 86.6 ms: 1.28x slower                                                 |
| scimark_sparse_mat_mult    | 4.40 ms                                                                | 5.70 ms: 1.30x slower                                                 |
| sqlalchemy_imperative      | 18.9 ms                                                                | 24.5 ms: 1.30x slower                                                 |
| deepcopy_reduce            | 2.59 us                                                                | 3.36 us: 1.30x slower                                                 |
| bench_mp_pool              | 88.9 ms                                                                | 116 ms: 1.30x slower                                                  |
| typing_runtime_protocols   | 157 us                                                                 | 206 us: 1.31x slower                                                  |
| fannkuch                   | 374 ms                                                                 | 498 ms: 1.33x slower                                                  |
| xml_etree_process          | 58.0 ms                                                                | 77.4 ms: 1.33x slower                                                 |
| 2to3                       | 254 ms                                                                 | 342 ms: 1.35x slower                                                  |
| hexiom                     | 5.77 ms                                                                | 7.84 ms: 1.36x slower                                                 |
| mako                       | 11.5 ms                                                                | 15.6 ms: 1.36x slower                                                 |
| logging_simple             | 5.95 us                                                                | 8.23 us: 1.38x slower                                                 |
| logging_format             | 6.78 us                                                                | 9.40 us: 1.39x slower                                                 |
| scimark_sor                | 130 ms                                                                 | 181 ms: 1.39x slower                                                  |
| chaos                      | 57.5 ms                                                                | 80.4 ms: 1.40x slower                                                 |
| sqlalchemy_declarative     | 127 ms                                                                 | 178 ms: 1.41x slower                                                  |
| sqlglot_transpile          | 1.57 ms                                                                | 2.21 ms: 1.41x slower                                                 |
| thrift                     | 742 us                                                                 | 1.05 ms: 1.42x slower                                                 |
| float                      | 76.2 ms                                                                | 109 ms: 1.43x slower                                                  |
| go                         | 119 ms                                                                 | 170 ms: 1.43x slower                                                  |
| richards                   | 44.9 ms                                                                | 65.3 ms: 1.45x slower                                                 |
| nbody                      | 90.7 ms                                                                | 132 ms: 1.45x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 28.7 ms: 1.46x slower                                                 |
| richards_super             | 50.9 ms                                                                | 74.7 ms: 1.47x slower                                                 |
| raytrace                   | 258 ms                                                                 | 381 ms: 1.48x slower                                                  |
| sqlglot_parse              | 1.26 ms                                                                | 1.89 ms: 1.50x slower                                                 |
| scimark_monte_carlo        | 63.3 ms                                                                | 95.6 ms: 1.51x slower                                                 |
| scimark_lu                 | 108 ms                                                                 | 164 ms: 1.52x slower                                                  |
| python_startup             | 14.6 ms                                                                | 23.6 ms: 1.62x slower                                                 |
| deltablue                  | 3.21 ms                                                                | 5.43 ms: 1.69x slower                                                 |
| sympy_str                  | 268 ms                                                                 | 460 ms: 1.72x slower                                                  |
| python_startup_no_site     | 7.47 ms                                                                | 14.2 ms: 1.90x slower                                                 |
| sympy_expand               | 455 ms                                                                 | 933 ms: 2.05x slower                                                  |
| sympy_sum                  | 151 ms                                                                 | 343 ms: 2.26x slower                                                  |
| bench_thread_pool          | 1.02 ms                                                                | 3.43 ms: 3.35x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.26x slower                                                          |
Ignored benchmarks (1) of results/bm-20241212-3.14.0a2+-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f.json: html5lib

- Geometric mean (including insignificant results): 1.200x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.20x