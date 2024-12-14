# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: b1ed3ee
- commit date: 2024-12-13
- overall geometric mean: 1.181x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 323 ms: 1.27x slower                                                  |
| docutils       | 2.55 sec                                                               | 2.87 sec: 1.13x slower                                                |
| sphinx         | 993 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                  |
| async_tree_none_tg         | 257 ms                                                                 | 266 ms: 1.03x slower                                                  |
| async_tree_io              | 631 ms                                                                 | 653 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 512 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 544 ms: 1.08x slower                                                  |
| async_tree_memoization_tg  | 310 ms                                                                 | 337 ms: 1.09x slower                                                  |
| async_tree_none            | 280 ms                                                                 | 306 ms: 1.09x slower                                                  |
| async_tree_memoization     | 335 ms                                                                 | 375 ms: 1.12x slower                                                  |
| coroutines                 | 21.7 ms                                                                | 24.6 ms: 1.14x slower                                                 |
| async_generators           | 359 ms                                                                 | 415 ms: 1.16x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| float          | 76.5 ms                                                                | 103 ms: 1.34x slower                                                  |
| nbody          | 90.0 ms                                                                | 130 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.24x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 25.0 ms                                                                | 23.2 ms: 1.08x faster                                                 |
| regex_dna      | 179 ms                                                                 | 176 ms: 1.02x faster                                                  |
| regex_effbot   | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                 |
| regex_compile  | 126 ms                                                                 | 157 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.4 ms                                                                | 87.7 ms: 1.03x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| json_loads           | 26.2 us                                                                | 28.1 us: 1.07x slower                                                 |
| xml_etree_generate   | 82.9 ms                                                                | 95.5 ms: 1.15x slower                                                 |
| pickle_pure_python   | 321 us                                                                 | 370 us: 1.15x slower                                                  |
| json_dumps           | 11.3 ms                                                                | 13.2 ms: 1.16x slower                                                 |
| unpickle_pure_python | 211 us                                                                 | 254 us: 1.20x slower                                                  |
| xml_etree_process    | 58.1 ms                                                                | 71.6 ms: 1.23x slower                                                 |
| tomli_loads          | 1.97 sec                                                               | 2.52 sec: 1.28x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| python_startup_no_site | 7.51 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.1 ms                                                                | 44.0 ms: 1.22x slower                                                 |
| genshi_xml      | 49.6 ms                                                                | 60.8 ms: 1.23x slower                                                 |
| genshi_text     | 21.5 ms                                                                | 27.7 ms: 1.29x slower                                                 |
| mako            | 11.6 ms                                                                | 15.6 ms: 1.35x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.02 ms                                                                | 3.16 ms: 1.27x faster                                                 |
| regex_v8                   | 25.0 ms                                                                | 23.2 ms: 1.08x faster                                                 |
| create_gc_cycles           | 1.85 ms                                                                | 1.78 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 90.4 ms                                                                | 87.7 ms: 1.03x faster                                                 |
| pidigits                   | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| regex_dna                  | 179 ms                                                                 | 176 ms: 1.02x faster                                                  |
| regex_effbot               | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.19 us                                                                | 2.16 us: 1.01x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                  |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| async_tree_none_tg         | 257 ms                                                                 | 266 ms: 1.03x slower                                                  |
| async_tree_io              | 631 ms                                                                 | 653 ms: 1.04x slower                                                  |
| json                       | 4.75 ms                                                                | 4.95 ms: 1.04x slower                                                 |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 512 ms: 1.05x slower                                                  |
| pathlib                    | 18.2 ms                                                                | 19.4 ms: 1.07x slower                                                 |
| logging_silent             | 106 ns                                                                 | 114 ns: 1.07x slower                                                  |
| json_loads                 | 26.2 us                                                                | 28.1 us: 1.07x slower                                                 |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 544 ms: 1.08x slower                                                  |
| async_tree_memoization_tg  | 310 ms                                                                 | 337 ms: 1.09x slower                                                  |
| async_tree_none            | 280 ms                                                                 | 306 ms: 1.09x slower                                                  |
| spectral_norm              | 101 ms                                                                 | 110 ms: 1.10x slower                                                  |
| mdp                        | 2.46 sec                                                               | 2.72 sec: 1.11x slower                                                |
| async_tree_memoization     | 335 ms                                                                 | 375 ms: 1.12x slower                                                  |
| dulwich_log                | 75.7 ms                                                                | 85.2 ms: 1.13x slower                                                 |
| k_core                     | 2.06 sec                                                               | 2.32 sec: 1.13x slower                                                |
| docutils                   | 2.55 sec                                                               | 2.87 sec: 1.13x slower                                                |
| sphinx                     | 993 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| generators                 | 27.1 ms                                                                | 30.7 ms: 1.13x slower                                                 |
| coroutines                 | 21.7 ms                                                                | 24.6 ms: 1.14x slower                                                 |
| bpe_tokeniser              | 4.21 sec                                                               | 4.78 sec: 1.14x slower                                                |
| xml_etree_generate         | 82.9 ms                                                                | 95.5 ms: 1.15x slower                                                 |
| pickle_pure_python         | 321 us                                                                 | 370 us: 1.15x slower                                                  |
| sqlglot_normalize          | 104 ms                                                                 | 119 ms: 1.15x slower                                                  |
| async_generators           | 359 ms                                                                 | 415 ms: 1.16x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.19 ms: 1.16x slower                                                 |
| json_dumps                 | 11.3 ms                                                                | 13.2 ms: 1.16x slower                                                 |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| sqlglot_optimize           | 52.1 ms                                                                | 61.0 ms: 1.17x slower                                                 |
| scimark_fft                | 318 ms                                                                 | 373 ms: 1.17x slower                                                  |
| pprint_safe_repr           | 712 ms                                                                 | 844 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.75 sec: 1.19x slower                                                |
| bench_mp_pool              | 88.8 ms                                                                | 106 ms: 1.19x slower                                                  |
| telco                      | 7.10 ms                                                                | 8.52 ms: 1.20x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.35 sec: 1.20x slower                                                |
| unpickle_pure_python       | 211 us                                                                 | 254 us: 1.20x slower                                                  |
| nqueens                    | 80.6 ms                                                                | 97.2 ms: 1.21x slower                                                 |
| deepcopy                   | 253 us                                                                 | 307 us: 1.21x slower                                                  |
| django_template            | 36.1 ms                                                                | 44.0 ms: 1.22x slower                                                 |
| genshi_xml                 | 49.6 ms                                                                | 60.8 ms: 1.23x slower                                                 |
| pyflate                    | 423 ms                                                                 | 519 ms: 1.23x slower                                                  |
| comprehensions             | 17.2 us                                                                | 21.2 us: 1.23x slower                                                 |
| xml_etree_process          | 58.1 ms                                                                | 71.6 ms: 1.23x slower                                                 |
| connected_components       | 398 ms                                                                 | 492 ms: 1.24x slower                                                  |
| subparsers                 | 22.0 ms                                                                | 27.3 ms: 1.24x slower                                                 |
| regex_compile              | 126 ms                                                                 | 157 ms: 1.24x slower                                                  |
| coverage                   | 79.0 ms                                                                | 98.4 ms: 1.25x slower                                                 |
| pylint                     | 281 ms                                                                 | 349 ms: 1.25x slower                                                  |
| shortest_path              | 438 ms                                                                 | 546 ms: 1.25x slower                                                  |
| deepcopy_reduce            | 2.58 us                                                                | 3.25 us: 1.26x slower                                                 |
| 2to3                       | 255 ms                                                                 | 323 ms: 1.27x slower                                                  |
| deepcopy_memo              | 29.8 us                                                                | 38.0 us: 1.28x slower                                                 |
| typing_runtime_protocols   | 154 us                                                                 | 197 us: 1.28x slower                                                  |
| tomli_loads                | 1.97 sec                                                               | 2.52 sec: 1.28x slower                                                |
| genshi_text                | 21.5 ms                                                                | 27.7 ms: 1.29x slower                                                 |
| crypto_pyaes               | 67.0 ms                                                                | 86.7 ms: 1.29x slower                                                 |
| fannkuch                   | 378 ms                                                                 | 490 ms: 1.30x slower                                                  |
| meteor_contest             | 98.2 ms                                                                | 129 ms: 1.31x slower                                                  |
| hexiom                     | 5.86 ms                                                                | 7.73 ms: 1.32x slower                                                 |
| sqlalchemy_imperative      | 19.0 ms                                                                | 25.0 ms: 1.32x slower                                                 |
| thrift                     | 758 us                                                                 | 1.02 ms: 1.34x slower                                                 |
| float                      | 76.5 ms                                                                | 103 ms: 1.34x slower                                                  |
| mako                       | 11.6 ms                                                                | 15.6 ms: 1.35x slower                                                 |
| scimark_sparse_mat_mult    | 4.22 ms                                                                | 5.68 ms: 1.35x slower                                                 |
| logging_format             | 6.83 us                                                                | 9.20 us: 1.35x slower                                                 |
| chaos                      | 58.6 ms                                                                | 79.1 ms: 1.35x slower                                                 |
| logging_simple             | 6.02 us                                                                | 8.14 us: 1.35x slower                                                 |
| python_startup_no_site     | 7.51 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| scimark_sor                | 127 ms                                                                 | 178 ms: 1.40x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                                | 2.18 ms: 1.40x slower                                                 |
| go                         | 117 ms                                                                 | 165 ms: 1.42x slower                                                  |
| sqlalchemy_declarative     | 126 ms                                                                 | 181 ms: 1.43x slower                                                  |
| richards                   | 45.1 ms                                                                | 64.9 ms: 1.44x slower                                                 |
| raytrace                   | 258 ms                                                                 | 372 ms: 1.44x slower                                                  |
| sympy_integrate            | 19.9 ms                                                                | 28.6 ms: 1.44x slower                                                 |
| nbody                      | 90.0 ms                                                                | 130 ms: 1.45x slower                                                  |
| richards_super             | 50.9 ms                                                                | 74.8 ms: 1.47x slower                                                 |
| scimark_lu                 | 110 ms                                                                 | 163 ms: 1.48x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.85 ms: 1.49x slower                                                 |
| scimark_monte_carlo        | 62.8 ms                                                                | 94.6 ms: 1.51x slower                                                 |
| sympy_str                  | 273 ms                                                                 | 458 ms: 1.68x slower                                                  |
| deltablue                  | 3.16 ms                                                                | 5.36 ms: 1.70x slower                                                 |
| sympy_expand               | 459 ms                                                                 | 928 ms: 2.02x slower                                                  |
| sympy_sum                  | 153 ms                                                                 | 340 ms: 2.23x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.34 ms: 3.24x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.23x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io_tg
Ignored benchmarks (1) of results/bm-20241213-3.14.0a2+-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee.json: html5lib

- Geometric mean (including insignificant results): 1.181x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.20x