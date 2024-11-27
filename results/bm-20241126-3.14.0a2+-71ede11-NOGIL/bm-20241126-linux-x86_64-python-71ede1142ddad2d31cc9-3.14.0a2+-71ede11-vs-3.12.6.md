# Results vs. 3.12.6

- fork: python
- ref: 71ede1142ddad2d31cc9
- machine: linux-x86_64
- commit hash: 71ede11
- commit date: 2024-11-26
- overall geometric mean: 1.231x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 647 ms: 1.42x slower                                                   |
| docutils       | 4.00 sec                                               | 4.75 sec: 1.19x slower                                                 |
| html5lib       | 88.9 ms                                                | 136 ms: 1.53x slower                                                   |
| Geometric mean | (ref)                                                  | 1.37x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.13 sec: 1.71x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.15 sec: 1.61x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 641 ms: 1.45x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 684 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 504 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 820 ms: 1.34x faster                                                   |
| async_tree_none            | 741 ms                                                 | 557 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 883 ms: 1.22x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 778 ms: 1.04x slower                                                   |
| async_generators           | 589 ms                                                 | 711 ms: 1.21x slower                                                   |
| coroutines                 | 29.5 ms                                                | 38.7 ms: 1.31x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| float          | 123 ms                                                 | 172 ms: 1.40x slower                                                   |
| nbody          | 119 ms                                                 | 217 ms: 1.83x slower                                                   |
| Geometric mean | (ref)                                                  | 1.34x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.54 ms: 1.13x faster                                                  |
| regex_dna      | 278 ms                                                 | 288 ms: 1.04x slower                                                   |
| regex_v8       | 32.5 ms                                                | 34.4 ms: 1.06x slower                                                  |
| regex_compile  | 187 ms                                                 | 253 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 155 ms: 1.09x faster                                                   |
| xml_etree_generate   | 127 ms                                                 | 150 ms: 1.18x slower                                                   |
| json_dumps           | 14.3 ms                                                | 18.8 ms: 1.31x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 3.91 sec: 1.36x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 133 ms: 1.59x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 479 us: 1.60x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 756 us: 1.74x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.26x slower                                                           |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 23.8 ms: 1.35x slower                                                  |
| python_startup         | 23.7 ms                                                | 37.0 ms: 1.56x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 102 ms: 1.51x slower                                                   |
| genshi_text     | 30.2 ms                                                | 47.4 ms: 1.57x slower                                                  |
| django_template | 44.9 ms                                                | 72.1 ms: 1.60x slower                                                  |
| mako            | 15.7 ms                                                | 32.2 ms: 2.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.67x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.13 sec: 1.71x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.15 sec: 1.61x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 641 ms: 1.45x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 684 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 504 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 820 ms: 1.34x faster                                                   |
| async_tree_none            | 741 ms                                                 | 557 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 883 ms: 1.22x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.54 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 155 ms: 1.09x faster                                                   |
| pidigits                   | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| deepcopy                   | 468 us                                                 | 447 us: 1.05x faster                                                   |
| regex_dna                  | 278 ms                                                 | 288 ms: 1.04x slower                                                   |
| asyncio_websockets         | 748 ms                                                 | 778 ms: 1.04x slower                                                   |
| regex_v8                   | 32.5 ms                                                | 34.4 ms: 1.06x slower                                                  |
| sqlite_synth               | 3.87 us                                                | 4.10 us: 1.06x slower                                                  |
| pycparser                  | 1.79 sec                                               | 1.97 sec: 1.10x slower                                                 |
| gc_traversal               | 5.86 ms                                                | 6.47 ms: 1.10x slower                                                  |
| scimark_fft                | 500 ms                                                 | 556 ms: 1.11x slower                                                   |
| deepcopy_memo              | 52.4 us                                                | 61.1 us: 1.17x slower                                                  |
| xml_etree_generate         | 127 ms                                                 | 150 ms: 1.18x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.69 sec: 1.18x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.75 sec: 1.19x slower                                                 |
| json                       | 6.85 ms                                                | 8.24 ms: 1.20x slower                                                  |
| spectral_norm              | 156 ms                                                 | 188 ms: 1.21x slower                                                   |
| async_generators           | 589 ms                                                 | 711 ms: 1.21x slower                                                   |
| pylint                     | 465 ms                                                 | 563 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.19 ms: 1.22x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 93.3 ms: 1.23x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 197 ms: 1.25x slower                                                   |
| dulwich_log                | 100 ms                                                 | 128 ms: 1.27x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 137 ms: 1.28x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 5.21 us: 1.29x slower                                                  |
| nqueens                    | 117 ms                                                 | 152 ms: 1.30x slower                                                   |
| coroutines                 | 29.5 ms                                                | 38.7 ms: 1.31x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 18.8 ms: 1.31x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 8.88 sec: 1.35x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 23.8 ms: 1.35x slower                                                  |
| regex_compile              | 187 ms                                                 | 253 ms: 1.36x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.91 sec: 1.36x slower                                                 |
| generators                 | 41.1 ms                                                | 56.7 ms: 1.38x slower                                                  |
| meteor_contest             | 146 ms                                                 | 205 ms: 1.40x slower                                                   |
| float                      | 123 ms                                                 | 172 ms: 1.40x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 4.91 ms: 1.41x slower                                                  |
| 2to3                       | 456 ms                                                 | 647 ms: 1.42x slower                                                   |
| pyflate                    | 727 ms                                                 | 1.04 sec: 1.43x slower                                                 |
| fannkuch                   | 540 ms                                                 | 775 ms: 1.43x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 323 us: 1.44x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 42.8 ms: 1.44x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.40 sec: 1.45x slower                                                 |
| coverage                   | 95.4 ms                                                | 140 ms: 1.47x slower                                                   |
| telco                      | 9.59 ms                                                | 14.2 ms: 1.48x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.96 sec: 1.50x slower                                                 |
| thrift                     | 1.06 ms                                                | 1.60 ms: 1.51x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 102 ms: 1.51x slower                                                   |
| comprehensions             | 27.1 us                                                | 41.3 us: 1.52x slower                                                  |
| html5lib                   | 88.9 ms                                                | 136 ms: 1.53x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 149 ms: 1.55x slower                                                   |
| python_startup             | 23.7 ms                                                | 37.0 ms: 1.56x slower                                                  |
| logging_format             | 9.59 us                                                | 15.0 us: 1.56x slower                                                  |
| genshi_text                | 30.2 ms                                                | 47.4 ms: 1.57x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 133 ms: 1.59x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 479 us: 1.60x slower                                                   |
| django_template            | 44.9 ms                                                | 72.1 ms: 1.60x slower                                                  |
| richards_super             | 72.8 ms                                                | 119 ms: 1.64x slower                                                   |
| logging_simple             | 9.45 us                                                | 15.7 us: 1.66x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 254 ms: 1.67x slower                                                   |
| sympy_str                  | 385 ms                                                 | 650 ms: 1.69x slower                                                   |
| logging_silent             | 139 ns                                                 | 241 ns: 1.73x slower                                                   |
| chaos                      | 84.9 ms                                                | 147 ms: 1.73x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 756 us: 1.74x slower                                                   |
| raytrace                   | 408 ms                                                 | 712 ms: 1.75x slower                                                   |
| scimark_sor                | 167 ms                                                 | 301 ms: 1.81x slower                                                   |
| hexiom                     | 8.27 ms                                                | 15.0 ms: 1.81x slower                                                  |
| richards                   | 60.3 ms                                                | 109 ms: 1.81x slower                                                   |
| nbody                      | 119 ms                                                 | 217 ms: 1.83x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                | 3.66 ms: 1.89x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.40 ms: 1.90x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.52 ms: 1.93x slower                                                  |
| go                         | 172 ms                                                 | 342 ms: 1.98x slower                                                   |
| sympy_expand               | 582 ms                                                 | 1.17 sec: 2.01x slower                                                 |
| mako                       | 15.7 ms                                                | 32.2 ms: 2.05x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 470 ms: 2.12x slower                                                   |
| deltablue                  | 4.27 ms                                                | 10.4 ms: 2.44x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 98.2 ms: 4.75x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.34x slower                                                           |

Benchmark hidden because not significant (3): json_loads, xml_etree_parse, pathlib
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.231x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.34x