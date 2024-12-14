# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: b1ed3ee
- commit date: 2024-12-13
- overall geometric mean: 1.144x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 323 ms: 1.25x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.87 sec: 1.10x slower                                                |
| html5lib       | 67.0 ms                                                      | 80.4 ms: 1.20x slower                                                 |
| Geometric mean | (ref)                                                        | 1.18x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 618 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 653 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 266 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 512 ms: 1.25x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 375 ms: 1.23x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 337 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 544 ms: 1.22x faster                                                  |
| async_tree_none            | 354 ms                                                       | 306 ms: 1.16x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                 |
| async_generators           | 377 ms                                                       | 415 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.17x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| float          | 77.5 ms                                                      | 103 ms: 1.33x slower                                                  |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                  |
| Geometric mean | (ref)                                                        | 1.19x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                 |
| regex_dna      | 180 ms                                                       | 176 ms: 1.03x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                 |
| regex_compile  | 132 ms                                                       | 157 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.7 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 95.5 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 71.6 ms: 1.21x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 254 us: 1.21x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 13.2 ms: 1.25x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 370 us: 1.26x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.52 sec: 1.26x slower                                                |
| Geometric mean       | (ref)                                                        | 1.13x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.8 ms: 1.25x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 27.7 ms: 1.28x slower                                                 |
| django_template | 34.1 ms                                                      | 44.0 ms: 1.29x slower                                                 |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 618 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 653 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 266 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 512 ms: 1.25x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 375 ms: 1.23x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 337 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 544 ms: 1.22x faster                                                  |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| deepcopy                   | 355 us                                                       | 307 us: 1.16x faster                                                  |
| async_tree_none            | 354 ms                                                       | 306 ms: 1.16x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.7 ms: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 38.0 us: 1.03x faster                                                 |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.03x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.16 us: 1.02x faster                                                 |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.16 ms: 1.01x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.4 ms: 1.01x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.25 us: 1.04x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                 |
| generators                 | 28.8 ms                                                      | 30.7 ms: 1.06x slower                                                 |
| scimark_fft                | 349 ms                                                       | 373 ms: 1.07x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.78 sec: 1.08x slower                                                |
| telco                      | 7.82 ms                                                      | 8.52 ms: 1.09x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.87 sec: 1.10x slower                                                |
| async_generators           | 377 ms                                                       | 415 ms: 1.10x slower                                                  |
| pylint                     | 317 ms                                                       | 349 ms: 1.10x slower                                                  |
| logging_silent             | 103 ns                                                       | 114 ns: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 95.5 ms: 1.12x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 119 ms: 1.13x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 85.2 ms: 1.14x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 844 ms: 1.14x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.72 sec: 1.16x slower                                                |
| sqlglot_optimize           | 52.7 ms                                                      | 61.0 ms: 1.16x slower                                                 |
| pyflate                    | 449 ms                                                       | 519 ms: 1.16x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.75 sec: 1.17x slower                                                |
| go                         | 141 ms                                                       | 165 ms: 1.17x slower                                                  |
| coverage                   | 83.0 ms                                                      | 98.4 ms: 1.19x slower                                                 |
| regex_compile              | 132 ms                                                       | 157 ms: 1.19x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 80.4 ms: 1.20x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.68 ms: 1.21x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 71.6 ms: 1.21x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 254 us: 1.21x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.35 sec: 1.21x slower                                                |
| nqueens                    | 78.6 ms                                                      | 97.2 ms: 1.24x slower                                                 |
| 2to3                       | 260 ms                                                       | 323 ms: 1.25x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 60.8 ms: 1.25x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 13.2 ms: 1.25x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 370 us: 1.26x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.52 sec: 1.26x slower                                                |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 197 us: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 86.7 ms: 1.28x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 27.7 ms: 1.28x slower                                                 |
| comprehensions             | 16.5 us                                                      | 21.2 us: 1.29x slower                                                 |
| django_template            | 34.1 ms                                                      | 44.0 ms: 1.29x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.73 ms: 1.29x slower                                                 |
| thrift                     | 778 us                                                       | 1.02 ms: 1.31x slower                                                 |
| logging_simple             | 6.16 us                                                      | 8.14 us: 1.32x slower                                                 |
| scimark_sor                | 134 ms                                                       | 178 ms: 1.32x slower                                                  |
| fannkuch                   | 370 ms                                                       | 490 ms: 1.33x slower                                                  |
| float                      | 77.5 ms                                                      | 103 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.78 ms: 1.33x slower                                                 |
| logging_format             | 6.84 us                                                      | 9.20 us: 1.34x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                 |
| chaos                      | 57.3 ms                                                      | 79.1 ms: 1.38x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 2.18 ms: 1.40x slower                                                 |
| richards                   | 45.2 ms                                                      | 64.9 ms: 1.43x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 28.6 ms: 1.44x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 94.6 ms: 1.45x slower                                                 |
| richards_super             | 51.6 ms                                                      | 74.8 ms: 1.45x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 163 ms: 1.45x slower                                                  |
| raytrace                   | 253 ms                                                       | 372 ms: 1.47x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.85 ms: 1.48x slower                                                 |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                 |
| sympy_str                  | 275 ms                                                       | 458 ms: 1.67x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 5.36 ms: 1.71x slower                                                 |
| sympy_expand               | 457 ms                                                       | 928 ms: 2.03x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 340 ms: 2.19x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.34 ms: 3.64x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 106 ms: 9.64x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.21x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, json
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.144x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.33x