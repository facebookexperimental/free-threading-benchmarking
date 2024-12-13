# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 39cab3f
- commit date: 2024-12-12
- overall geometric mean: 1.106x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 367 ms                                                                 | 342 ms: 1.07x faster                                                  |
| docutils       | 3.09 sec                                                               | 2.87 sec: 1.08x faster                                                |
| html5lib       | 97.9 ms                                                                | 78.3 ms: 1.25x faster                                                 |
| sphinx         | 1.19 sec                                                               | 1.13 sec: 1.05x faster                                                |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 354 ms                                                                 | 272 ms: 1.30x faster                                                  |
| async_tree_io_tg           | 829 ms                                                                 | 637 ms: 1.30x faster                                                  |
| async_tree_memoization_tg  | 444 ms                                                                 | 346 ms: 1.28x faster                                                  |
| async_tree_io              | 842 ms                                                                 | 662 ms: 1.27x faster                                                  |
| async_tree_none            | 384 ms                                                                 | 309 ms: 1.24x faster                                                  |
| async_tree_memoization     | 465 ms                                                                 | 377 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 611 ms                                                                 | 524 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed    | 630 ms                                                                 | 550 ms: 1.15x faster                                                  |
| async_generators           | 454 ms                                                                 | 423 ms: 1.07x faster                                                  |
| coroutines                 | 25.3 ms                                                                | 24.6 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.18x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 140 ms                                                                 | 109 ms: 1.28x faster                                                  |
| pidigits       | 184 ms                                                                 | 184 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 179 ms                                                                 | 161 ms: 1.11x faster                                                  |
| regex_v8       | 25.2 ms                                                                | 24.0 ms: 1.05x faster                                                 |
| regex_dna      | 186 ms                                                                 | 178 ms: 1.05x faster                                                  |
| regex_effbot   | 2.77 ms                                                                | 2.85 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 506 us                                                                 | 370 us: 1.37x faster                                                  |
| unpickle_pure_python | 336 us                                                                 | 257 us: 1.31x faster                                                  |
| json_dumps           | 14.1 ms                                                                | 13.2 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 90.4 ms                                                                | 88.2 ms: 1.03x faster                                                 |
| tomli_loads          | 2.67 sec                                                               | 2.60 sec: 1.03x faster                                                |
| json_loads           | 28.4 us                                                                | 28.0 us: 1.02x faster                                                 |
| xml_etree_process    | 78.6 ms                                                                | 77.4 ms: 1.02x faster                                                 |
| xml_etree_generate   | 98.4 ms                                                                | 97.1 ms: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.4 ms                                                                | 23.6 ms: 1.36x slower                                                 |
| python_startup_no_site | 10.2 ms                                                                | 14.2 ms: 1.39x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 17.8 ms                                                                | 15.6 ms: 1.14x faster                                                 |
| django_template | 50.3 ms                                                                | 44.3 ms: 1.14x faster                                                 |
| genshi_text     | 31.6 ms                                                                | 27.9 ms: 1.13x faster                                                 |
| genshi_xml      | 63.0 ms                                                                | 61.1 ms: 1.03x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.11x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| logging_silent             | 179 ns                                                                 | 112 ns: 1.60x faster                                                  |
| go                         | 267 ms                                                                 | 170 ms: 1.57x faster                                                  |
| deltablue                  | 8.00 ms                                                                | 5.43 ms: 1.47x faster                                                 |
| raytrace                   | 547 ms                                                                 | 381 ms: 1.44x faster                                                  |
| sqlglot_parse              | 2.63 ms                                                                | 1.89 ms: 1.39x faster                                                 |
| pickle_pure_python         | 506 us                                                                 | 370 us: 1.37x faster                                                  |
| sqlglot_transpile          | 2.99 ms                                                                | 2.21 ms: 1.35x faster                                                 |
| unpickle_pure_python       | 336 us                                                                 | 257 us: 1.31x faster                                                  |
| async_tree_none_tg         | 354 ms                                                                 | 272 ms: 1.30x faster                                                  |
| async_tree_io_tg           | 829 ms                                                                 | 637 ms: 1.30x faster                                                  |
| scimark_sor                | 236 ms                                                                 | 181 ms: 1.30x faster                                                  |
| logging_simple             | 10.7 us                                                                | 8.23 us: 1.30x faster                                                 |
| comprehensions             | 27.0 us                                                                | 21.0 us: 1.29x faster                                                 |
| chaos                      | 103 ms                                                                 | 80.4 ms: 1.28x faster                                                 |
| float                      | 140 ms                                                                 | 109 ms: 1.28x faster                                                  |
| async_tree_memoization_tg  | 444 ms                                                                 | 346 ms: 1.28x faster                                                  |
| async_tree_io              | 842 ms                                                                 | 662 ms: 1.27x faster                                                  |
| hexiom                     | 9.94 ms                                                                | 7.84 ms: 1.27x faster                                                 |
| logging_format             | 11.9 us                                                                | 9.40 us: 1.26x faster                                                 |
| pyflate                    | 685 ms                                                                 | 547 ms: 1.25x faster                                                  |
| html5lib                   | 97.9 ms                                                                | 78.3 ms: 1.25x faster                                                 |
| async_tree_none            | 384 ms                                                                 | 309 ms: 1.24x faster                                                  |
| scimark_monte_carlo        | 118 ms                                                                 | 95.6 ms: 1.24x faster                                                 |
| async_tree_memoization     | 465 ms                                                                 | 377 ms: 1.23x faster                                                  |
| generators                 | 38.0 ms                                                                | 31.2 ms: 1.22x faster                                                 |
| sqlalchemy_imperative      | 29.5 ms                                                                | 24.5 ms: 1.20x faster                                                 |
| richards                   | 76.5 ms                                                                | 65.3 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 611 ms                                                                 | 524 ms: 1.17x faster                                                  |
| pycparser                  | 1.55 sec                                                               | 1.34 sec: 1.16x faster                                                |
| subparsers                 | 31.3 ms                                                                | 27.1 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 630 ms                                                                 | 550 ms: 1.15x faster                                                  |
| richards_super             | 85.4 ms                                                                | 74.7 ms: 1.14x faster                                                 |
| scimark_lu                 | 187 ms                                                                 | 164 ms: 1.14x faster                                                  |
| mako                       | 17.8 ms                                                                | 15.6 ms: 1.14x faster                                                 |
| sqlalchemy_declarative     | 203 ms                                                                 | 178 ms: 1.14x faster                                                  |
| django_template            | 50.3 ms                                                                | 44.3 ms: 1.14x faster                                                 |
| genshi_text                | 31.6 ms                                                                | 27.9 ms: 1.13x faster                                                 |
| dulwich_log                | 95.6 ms                                                                | 85.8 ms: 1.11x faster                                                 |
| regex_compile              | 179 ms                                                                 | 161 ms: 1.11x faster                                                  |
| pprint_safe_repr           | 975 ms                                                                 | 882 ms: 1.11x faster                                                  |
| pprint_pformat             | 2.02 sec                                                               | 1.83 sec: 1.11x faster                                                |
| thrift                     | 1.16 ms                                                                | 1.05 ms: 1.10x faster                                                 |
| sqlglot_normalize          | 134 ms                                                                 | 122 ms: 1.10x faster                                                  |
| sqlglot_optimize           | 69.1 ms                                                                | 63.1 ms: 1.10x faster                                                 |
| many_optionals             | 1.29 ms                                                                | 1.19 ms: 1.08x faster                                                 |
| pylint                     | 381 ms                                                                 | 352 ms: 1.08x faster                                                  |
| docutils                   | 3.09 sec                                                               | 2.87 sec: 1.08x faster                                                |
| async_generators           | 454 ms                                                                 | 423 ms: 1.07x faster                                                  |
| 2to3                       | 367 ms                                                                 | 342 ms: 1.07x faster                                                  |
| json_dumps                 | 14.1 ms                                                                | 13.2 ms: 1.07x faster                                                 |
| sqlite_synth               | 2.26 us                                                                | 2.13 us: 1.06x faster                                                 |
| crypto_pyaes               | 91.3 ms                                                                | 86.6 ms: 1.05x faster                                                 |
| sphinx                     | 1.19 sec                                                               | 1.13 sec: 1.05x faster                                                |
| regex_v8                   | 25.2 ms                                                                | 24.0 ms: 1.05x faster                                                 |
| regex_dna                  | 186 ms                                                                 | 178 ms: 1.05x faster                                                  |
| deepcopy_memo              | 40.1 us                                                                | 38.5 us: 1.04x faster                                                 |
| bpe_tokeniser              | 4.99 sec                                                               | 4.81 sec: 1.04x faster                                                |
| deepcopy_reduce            | 3.48 us                                                                | 3.36 us: 1.04x faster                                                 |
| sympy_str                  | 477 ms                                                                 | 460 ms: 1.04x faster                                                  |
| pathlib                    | 20.0 ms                                                                | 19.4 ms: 1.03x faster                                                 |
| deepcopy                   | 325 us                                                                 | 315 us: 1.03x faster                                                  |
| genshi_xml                 | 63.0 ms                                                                | 61.1 ms: 1.03x faster                                                 |
| sympy_integrate            | 29.6 ms                                                                | 28.7 ms: 1.03x faster                                                 |
| json                       | 5.06 ms                                                                | 4.93 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 90.4 ms                                                                | 88.2 ms: 1.03x faster                                                 |
| tomli_loads                | 2.67 sec                                                               | 2.60 sec: 1.03x faster                                                |
| coroutines                 | 25.3 ms                                                                | 24.6 ms: 1.02x faster                                                 |
| sympy_sum                  | 350 ms                                                                 | 343 ms: 1.02x faster                                                  |
| sympy_expand               | 954 ms                                                                 | 933 ms: 1.02x faster                                                  |
| coverage                   | 100 ms                                                                 | 98.3 ms: 1.02x faster                                                 |
| shortest_path              | 550 ms                                                                 | 541 ms: 1.02x faster                                                  |
| json_loads                 | 28.4 us                                                                | 28.0 us: 1.02x faster                                                 |
| xml_etree_process          | 78.6 ms                                                                | 77.4 ms: 1.02x faster                                                 |
| k_core                     | 2.42 sec                                                               | 2.39 sec: 1.01x faster                                                |
| xml_etree_generate         | 98.4 ms                                                                | 97.1 ms: 1.01x faster                                                 |
| connected_components       | 498 ms                                                                 | 493 ms: 1.01x faster                                                  |
| fannkuch                   | 499 ms                                                                 | 498 ms: 1.00x faster                                                  |
| pidigits                   | 184 ms                                                                 | 184 ms: 1.00x slower                                                  |
| mdp                        | 2.77 sec                                                               | 2.77 sec: 1.00x slower                                                |
| telco                      | 8.68 ms                                                                | 8.74 ms: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 5.64 ms                                                                | 5.70 ms: 1.01x slower                                                 |
| typing_runtime_protocols   | 203 us                                                                 | 206 us: 1.01x slower                                                  |
| scimark_fft                | 392 ms                                                                 | 397 ms: 1.01x slower                                                  |
| spectral_norm              | 118 ms                                                                 | 121 ms: 1.03x slower                                                  |
| regex_effbot               | 2.77 ms                                                                | 2.85 ms: 1.03x slower                                                 |
| bench_mp_pool              | 109 ms                                                                 | 116 ms: 1.06x slower                                                  |
| python_startup             | 17.4 ms                                                                | 23.6 ms: 1.36x slower                                                 |
| python_startup_no_site     | 10.2 ms                                                                | 14.2 ms: 1.39x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.11x faster                                                          |

Benchmark hidden because not significant (8): asyncio_websockets, meteor_contest, create_gc_cycles, nbody, nqueens, xml_etree_parse, gc_traversal, bench_thread_pool

- Geometric mean (including insignificant results): 1.106x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.00x