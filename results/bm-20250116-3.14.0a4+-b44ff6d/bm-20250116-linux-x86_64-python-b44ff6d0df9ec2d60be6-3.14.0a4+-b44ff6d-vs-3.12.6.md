# Results vs. 3.12.6

- fork: python
- ref: b44ff6d0df9ec2d60be6
- machine: linux-x86_64
- commit hash: b44ff6d
- commit date: 2025-01-16
- overall geometric mean: 1.081x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.60 sec: 1.11x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 939 ms: 2.06x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 921 ms: 2.01x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 492 ms: 1.99x faster                                                   |
| async_tree_none            | 741 ms                                                 | 375 ms: 1.98x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 474 ms: 1.96x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 392 ms: 1.80x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 727 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 731 ms: 1.47x faster                                                   |
| async_generators           | 589 ms                                                 | 544 ms: 1.08x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 784 ms: 1.05x slower                                                   |
| coroutines                 | 29.5 ms                                                | 31.8 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 101 ms: 1.22x faster                                                   |
| pidigits       | 250 ms                                                 | 229 ms: 1.09x faster                                                   |
| nbody          | 119 ms                                                 | 129 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.23 ms: 1.21x faster                                                  |
| regex_v8       | 32.5 ms                                                | 30.6 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 206 ms: 1.17x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.64 sec: 1.09x faster                                                 |
| xml_etree_generate  | 127 ms                                                 | 119 ms: 1.07x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 162 ms: 1.05x faster                                                   |
| xml_etree_process   | 83.7 ms                                                | 88.6 ms: 1.06x slower                                                  |
| json_dumps          | 14.3 ms                                                | 16.3 ms: 1.14x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (3): json_loads, pickle_pure_python, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 16.7 ms: 1.06x faster                                                  |
| python_startup         | 23.7 ms                                                | 28.2 ms: 1.19x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 49.3 ms: 1.10x slower                                                  |
| mako            | 15.7 ms                                                | 17.7 ms: 1.13x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 939 ms: 2.06x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 921 ms: 2.01x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 492 ms: 1.99x faster                                                   |
| async_tree_none            | 741 ms                                                 | 375 ms: 1.98x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 474 ms: 1.96x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 392 ms: 1.80x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 727 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 731 ms: 1.47x faster                                                   |
| deepcopy                   | 468 us                                                 | 353 us: 1.32x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 41.9 us: 1.25x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 175 ms: 1.25x faster                                                   |
| float                      | 123 ms                                                 | 101 ms: 1.22x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.23 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.39 us: 1.19x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.03 us: 1.18x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 206 ms: 1.17x faster                                                   |
| scimark_fft                | 500 ms                                                 | 434 ms: 1.15x faster                                                   |
| pylint                     | 465 ms                                                 | 408 ms: 1.14x faster                                                   |
| pathlib                    | 31.6 ms                                                | 27.8 ms: 1.13x faster                                                  |
| sqlglot_normalize          | 157 ms                                                 | 139 ms: 1.13x faster                                                   |
| comprehensions             | 27.1 us                                                | 24.0 us: 1.13x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 85.6 ms: 1.13x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.54 sec: 1.12x faster                                                 |
| sqlalchemy_imperative      | 24.7 ms                                                | 22.1 ms: 1.12x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.61 sec: 1.11x faster                                                 |
| docutils                   | 4.00 sec                                               | 3.60 sec: 1.11x faster                                                 |
| crypto_pyaes               | 107 ms                                                 | 96.8 ms: 1.11x faster                                                  |
| pyflate                    | 727 ms                                                 | 662 ms: 1.10x faster                                                   |
| spectral_norm              | 156 ms                                                 | 142 ms: 1.10x faster                                                   |
| pidigits                   | 250 ms                                                 | 229 ms: 1.09x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.64 sec: 1.09x faster                                                 |
| fannkuch                   | 540 ms                                                 | 499 ms: 1.08x faster                                                   |
| async_generators           | 589 ms                                                 | 544 ms: 1.08x faster                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.16 ms: 1.08x faster                                                  |
| hexiom                     | 8.27 ms                                                | 7.73 ms: 1.07x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 119 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.28 ms: 1.07x faster                                                  |
| regex_v8                   | 32.5 ms                                                | 30.6 ms: 1.06x faster                                                  |
| raytrace                   | 408 ms                                                 | 386 ms: 1.06x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 16.7 ms: 1.06x faster                                                  |
| go                         | 172 ms                                                 | 164 ms: 1.05x faster                                                   |
| generators                 | 41.1 ms                                                | 39.1 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 6.26 sec: 1.05x faster                                                 |
| pprint_pformat             | 1.98 sec                                               | 1.89 sec: 1.05x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 162 ms: 1.05x faster                                                   |
| typing_runtime_protocols   | 224 us                                                 | 215 us: 1.04x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 4.06 us: 1.05x slower                                                  |
| asyncio_websockets         | 748 ms                                                 | 784 ms: 1.05x slower                                                   |
| scimark_sor                | 167 ms                                                 | 175 ms: 1.05x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 88.6 ms: 1.06x slower                                                  |
| sympy_expand               | 582 ms                                                 | 618 ms: 1.06x slower                                                   |
| coroutines                 | 29.5 ms                                                | 31.8 ms: 1.08x slower                                                  |
| nbody                      | 119 ms                                                 | 129 ms: 1.08x slower                                                   |
| logging_format             | 9.59 us                                                | 10.4 us: 1.08x slower                                                  |
| sympy_str                  | 385 ms                                                 | 419 ms: 1.09x slower                                                   |
| django_template            | 44.9 ms                                                | 49.3 ms: 1.10x slower                                                  |
| telco                      | 9.59 ms                                                | 10.8 ms: 1.12x slower                                                  |
| mako                       | 15.7 ms                                                | 17.7 ms: 1.13x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 3.92 ms: 1.13x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.3 ms: 1.14x slower                                                  |
| json                       | 6.85 ms                                                | 7.84 ms: 1.14x slower                                                  |
| coverage                   | 95.4 ms                                                | 113 ms: 1.19x slower                                                   |
| python_startup             | 23.7 ms                                                | 28.2 ms: 1.19x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 9.29 ms: 1.58x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 4.11 ms: 2.12x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 100 ms: 4.84x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (24): regex_compile, sqlglot_parse, nqueens, json_loads, regex_dna, pprint_safe_repr, html5lib, sqlglot_optimize, chaos, scimark_lu, sympy_sum, pickle_pure_python, logging_silent, thrift, deltablue, dulwich_log, genshi_xml, sympy_integrate, richards, genshi_text, meteor_contest, unpickle_pure_python, richards_super, 2to3
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.081x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x