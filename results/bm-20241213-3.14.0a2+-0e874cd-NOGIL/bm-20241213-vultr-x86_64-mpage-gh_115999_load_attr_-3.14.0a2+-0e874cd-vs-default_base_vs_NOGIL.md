# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 0e874cd
- commit date: 2024-12-13
- overall geometric mean: 1.185x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 323 ms: 1.27x slower                                                  |
| docutils       | 2.55 sec                                                               | 2.88 sec: 1.13x slower                                                |
| sphinx         | 993 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                  |
| async_tree_io_tg           | 614 ms                                                                 | 635 ms: 1.03x slower                                                  |
| async_tree_none_tg         | 257 ms                                                                 | 271 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 515 ms: 1.06x slower                                                  |
| async_tree_io              | 631 ms                                                                 | 668 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 548 ms: 1.09x slower                                                  |
| async_tree_none            | 280 ms                                                                 | 311 ms: 1.11x slower                                                  |
| async_tree_memoization_tg  | 310 ms                                                                 | 346 ms: 1.12x slower                                                  |
| async_tree_memoization     | 335 ms                                                                 | 380 ms: 1.13x slower                                                  |
| coroutines                 | 21.7 ms                                                                | 24.8 ms: 1.14x slower                                                 |
| async_generators           | 359 ms                                                                 | 421 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| float          | 76.5 ms                                                                | 104 ms: 1.36x slower                                                  |
| nbody          | 90.0 ms                                                                | 129 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.24x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 25.0 ms                                                                | 23.0 ms: 1.08x faster                                                 |
| regex_effbot   | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                 |
| regex_dna      | 179 ms                                                                 | 177 ms: 1.02x faster                                                  |
| regex_compile  | 126 ms                                                                 | 159 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.4 ms                                                                | 87.8 ms: 1.03x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 130 ms: 1.01x slower                                                  |
| json_loads           | 26.2 us                                                                | 28.1 us: 1.07x slower                                                 |
| xml_etree_generate   | 82.9 ms                                                                | 95.1 ms: 1.15x slower                                                 |
| pickle_pure_python   | 321 us                                                                 | 372 us: 1.16x slower                                                  |
| json_dumps           | 11.3 ms                                                                | 13.1 ms: 1.16x slower                                                 |
| unpickle_pure_python | 211 us                                                                 | 256 us: 1.21x slower                                                  |
| xml_etree_process    | 58.1 ms                                                                | 71.5 ms: 1.23x slower                                                 |
| tomli_loads          | 1.97 sec                                                               | 2.53 sec: 1.29x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| python_startup_no_site | 7.51 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.1 ms                                                                | 43.6 ms: 1.21x slower                                                 |
| genshi_xml      | 49.6 ms                                                                | 61.0 ms: 1.23x slower                                                 |
| genshi_text     | 21.5 ms                                                                | 28.1 ms: 1.31x slower                                                 |
| mako            | 11.6 ms                                                                | 15.6 ms: 1.35x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.02 ms                                                                | 3.19 ms: 1.26x faster                                                 |
| regex_v8                   | 25.0 ms                                                                | 23.0 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.19 us                                                                | 2.11 us: 1.04x faster                                                 |
| xml_etree_iterparse        | 90.4 ms                                                                | 87.8 ms: 1.03x faster                                                 |
| create_gc_cycles           | 1.85 ms                                                                | 1.80 ms: 1.02x faster                                                 |
| pidigits                   | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| regex_effbot               | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                 |
| regex_dna                  | 179 ms                                                                 | 177 ms: 1.02x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                  |
| xml_etree_parse            | 128 ms                                                                 | 130 ms: 1.01x slower                                                  |
| async_tree_io_tg           | 614 ms                                                                 | 635 ms: 1.03x slower                                                  |
| json                       | 4.75 ms                                                                | 4.93 ms: 1.04x slower                                                 |
| async_tree_none_tg         | 257 ms                                                                 | 271 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 515 ms: 1.06x slower                                                  |
| async_tree_io              | 631 ms                                                                 | 668 ms: 1.06x slower                                                  |
| json_loads                 | 26.2 us                                                                | 28.1 us: 1.07x slower                                                 |
| pathlib                    | 18.2 ms                                                                | 19.7 ms: 1.08x slower                                                 |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 548 ms: 1.09x slower                                                  |
| spectral_norm              | 101 ms                                                                 | 109 ms: 1.09x slower                                                  |
| logging_silent             | 106 ns                                                                 | 116 ns: 1.09x slower                                                  |
| async_tree_none            | 280 ms                                                                 | 311 ms: 1.11x slower                                                  |
| async_tree_memoization_tg  | 310 ms                                                                 | 346 ms: 1.12x slower                                                  |
| mdp                        | 2.46 sec                                                               | 2.76 sec: 1.13x slower                                                |
| bpe_tokeniser              | 4.21 sec                                                               | 4.76 sec: 1.13x slower                                                |
| docutils                   | 2.55 sec                                                               | 2.88 sec: 1.13x slower                                                |
| sphinx                     | 993 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| async_tree_memoization     | 335 ms                                                                 | 380 ms: 1.13x slower                                                  |
| dulwich_log                | 75.7 ms                                                                | 86.0 ms: 1.13x slower                                                 |
| k_core                     | 2.06 sec                                                               | 2.34 sec: 1.13x slower                                                |
| coroutines                 | 21.7 ms                                                                | 24.8 ms: 1.14x slower                                                 |
| xml_etree_generate         | 82.9 ms                                                                | 95.1 ms: 1.15x slower                                                 |
| generators                 | 27.1 ms                                                                | 31.2 ms: 1.15x slower                                                 |
| pickle_pure_python         | 321 us                                                                 | 372 us: 1.16x slower                                                  |
| json_dumps                 | 11.3 ms                                                                | 13.1 ms: 1.16x slower                                                 |
| many_optionals             | 1.03 ms                                                                | 1.20 ms: 1.16x slower                                                 |
| sqlglot_normalize          | 104 ms                                                                 | 121 ms: 1.17x slower                                                  |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| async_generators           | 359 ms                                                                 | 421 ms: 1.17x slower                                                  |
| telco                      | 7.10 ms                                                                | 8.36 ms: 1.18x slower                                                 |
| sqlglot_optimize           | 52.1 ms                                                                | 61.8 ms: 1.19x slower                                                 |
| scimark_fft                | 318 ms                                                                 | 379 ms: 1.19x slower                                                  |
| bench_mp_pool              | 88.8 ms                                                                | 106 ms: 1.20x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.35 sec: 1.20x slower                                                |
| django_template            | 36.1 ms                                                                | 43.6 ms: 1.21x slower                                                 |
| unpickle_pure_python       | 211 us                                                                 | 256 us: 1.21x slower                                                  |
| comprehensions             | 17.2 us                                                                | 20.9 us: 1.22x slower                                                 |
| nqueens                    | 80.6 ms                                                                | 98.7 ms: 1.22x slower                                                 |
| pprint_safe_repr           | 712 ms                                                                 | 874 ms: 1.23x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.80 sec: 1.23x slower                                                |
| xml_etree_process          | 58.1 ms                                                                | 71.5 ms: 1.23x slower                                                 |
| genshi_xml                 | 49.6 ms                                                                | 61.0 ms: 1.23x slower                                                 |
| connected_components       | 398 ms                                                                 | 492 ms: 1.24x slower                                                  |
| subparsers                 | 22.0 ms                                                                | 27.3 ms: 1.24x slower                                                 |
| deepcopy                   | 253 us                                                                 | 314 us: 1.24x slower                                                  |
| pylint                     | 281 ms                                                                 | 349 ms: 1.24x slower                                                  |
| shortest_path              | 438 ms                                                                 | 547 ms: 1.25x slower                                                  |
| coverage                   | 79.0 ms                                                                | 98.7 ms: 1.25x slower                                                 |
| pyflate                    | 423 ms                                                                 | 530 ms: 1.26x slower                                                  |
| regex_compile              | 126 ms                                                                 | 159 ms: 1.26x slower                                                  |
| 2to3                       | 255 ms                                                                 | 323 ms: 1.27x slower                                                  |
| crypto_pyaes               | 67.0 ms                                                                | 86.1 ms: 1.29x slower                                                 |
| tomli_loads                | 1.97 sec                                                               | 2.53 sec: 1.29x slower                                                |
| typing_runtime_protocols   | 154 us                                                                 | 199 us: 1.29x slower                                                  |
| deepcopy_memo              | 29.8 us                                                                | 38.6 us: 1.29x slower                                                 |
| sqlalchemy_imperative      | 19.0 ms                                                                | 24.6 ms: 1.30x slower                                                 |
| fannkuch                   | 378 ms                                                                 | 492 ms: 1.30x slower                                                  |
| genshi_text                | 21.5 ms                                                                | 28.1 ms: 1.31x slower                                                 |
| scimark_sparse_mat_mult    | 4.22 ms                                                                | 5.53 ms: 1.31x slower                                                 |
| meteor_contest             | 98.2 ms                                                                | 129 ms: 1.31x slower                                                  |
| deepcopy_reduce            | 2.58 us                                                                | 3.39 us: 1.32x slower                                                 |
| logging_format             | 6.83 us                                                                | 9.10 us: 1.33x slower                                                 |
| logging_simple             | 6.02 us                                                                | 8.09 us: 1.34x slower                                                 |
| hexiom                     | 5.86 ms                                                                | 7.90 ms: 1.35x slower                                                 |
| chaos                      | 58.6 ms                                                                | 79.0 ms: 1.35x slower                                                 |
| mako                       | 11.6 ms                                                                | 15.6 ms: 1.35x slower                                                 |
| float                      | 76.5 ms                                                                | 104 ms: 1.36x slower                                                  |
| python_startup_no_site     | 7.51 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| thrift                     | 758 us                                                                 | 1.04 ms: 1.37x slower                                                 |
| sqlalchemy_declarative     | 126 ms                                                                 | 178 ms: 1.41x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                                | 2.20 ms: 1.41x slower                                                 |
| scimark_sor                | 127 ms                                                                 | 181 ms: 1.42x slower                                                  |
| go                         | 117 ms                                                                 | 167 ms: 1.43x slower                                                  |
| nbody                      | 90.0 ms                                                                | 129 ms: 1.44x slower                                                  |
| richards                   | 45.1 ms                                                                | 65.0 ms: 1.44x slower                                                 |
| sympy_integrate            | 19.9 ms                                                                | 28.7 ms: 1.45x slower                                                 |
| richards_super             | 50.9 ms                                                                | 74.0 ms: 1.46x slower                                                 |
| raytrace                   | 258 ms                                                                 | 376 ms: 1.46x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.88 ms: 1.50x slower                                                 |
| scimark_monte_carlo        | 62.8 ms                                                                | 94.9 ms: 1.51x slower                                                 |
| scimark_lu                 | 110 ms                                                                 | 166 ms: 1.51x slower                                                  |
| sympy_str                  | 273 ms                                                                 | 461 ms: 1.69x slower                                                  |
| deltablue                  | 3.16 ms                                                                | 5.43 ms: 1.72x slower                                                 |
| sympy_expand               | 459 ms                                                                 | 934 ms: 2.04x slower                                                  |
| sympy_sum                  | 153 ms                                                                 | 342 ms: 2.24x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.35 ms: 3.25x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.24x slower                                                          |
Ignored benchmarks (1) of results/bm-20241213-3.14.0a2+-0e874cd-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd.json: html5lib

- Geometric mean (including insignificant results): 1.185x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.20x