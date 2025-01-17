# Results vs. 3.12.6

- fork: python
- ref: b44ff6d0df9ec2d60be6
- machine: linux-x86_64
- commit hash: b44ff6d
- commit date: 2025-01-16
- overall geometric mean: 1.090x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 252 ms: 1.05x faster                                                   |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 616 ms: 1.80x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 329 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 534 ms: 1.34x faster                                                   |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.3 ms: 1.12x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.2 ms: 1.12x faster                                                  |
| nbody          | 89.3 ms                                                | 86.5 ms: 1.03x faster                                                  |
| pidigits       | 184 ms                                                 | 207 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                  |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| regex_dna      | 168 ms                                                 | 170 ms: 1.01x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads         | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| xml_etree_parse     | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| xml_etree_iterparse | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                  |
| xml_etree_generate  | 85.2 ms                                                | 84.4 ms: 1.01x faster                                                  |
| xml_etree_process   | 59.0 ms                                                | 59.7 ms: 1.01x slower                                                  |
| pickle_pure_python  | 308 us                                                 | 316 us: 1.03x slower                                                   |
| json_loads          | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| json_dumps          | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                  |
| django_template | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 616 ms: 1.80x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 329 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                                   |
| deepcopy                   | 352 us                                                 | 259 us: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 534 ms: 1.34x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.34x faster                                                  |
| spectral_norm              | 110 ms                                                 | 89.1 ms: 1.24x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                  |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                                  |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.8 us: 1.18x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.62 us: 1.17x faster                                                  |
| generators                 | 32.2 ms                                                | 28.0 ms: 1.15x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.6 ms: 1.15x faster                                                  |
| raytrace                   | 299 ms                                                 | 262 ms: 1.14x faster                                                   |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 67.5 ms: 1.13x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| scimark_sor                | 130 ms                                                 | 115 ms: 1.13x faster                                                   |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.13x faster                                                 |
| coroutines                 | 23.9 ms                                                | 21.3 ms: 1.12x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.4 ms: 1.12x faster                                                  |
| float                      | 80.8 ms                                                | 72.2 ms: 1.12x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.11x faster                                                   |
| scimark_fft                | 342 ms                                                 | 309 ms: 1.11x faster                                                   |
| richards                   | 45.9 ms                                                | 41.7 ms: 1.10x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.16 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 414 ms: 1.08x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.25 ms: 1.08x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.1 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.55 ms: 1.08x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.7 ms: 1.07x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.18 us: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.75 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                  |
| thrift                     | 791 us                                                 | 745 us: 1.06x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 700 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.06x faster                                                 |
| logging_format             | 7.35 us                                                | 6.96 us: 1.06x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| 2to3                       | 264 ms                                                 | 252 ms: 1.05x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 75.6 ms: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.3 ms: 1.04x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                   |
| nbody                      | 89.3 ms                                                | 86.5 ms: 1.03x faster                                                  |
| nqueens                    | 80.1 ms                                                | 77.5 ms: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.27 ms: 1.03x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.02x faster                                                 |
| fannkuch                   | 372 ms                                                 | 363 ms: 1.02x faster                                                   |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                   |
| sympy_expand               | 468 ms                                                 | 459 ms: 1.02x faster                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 52.5 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 107 ms                                                 | 105 ms: 1.01x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.17 us: 1.01x faster                                                  |
| json                       | 5.02 ms                                                | 4.97 ms: 1.01x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 84.4 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 59.7 ms: 1.01x slower                                                  |
| regex_dna                  | 168 ms                                                 | 170 ms: 1.01x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.47 sec: 1.02x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 316 us: 1.03x slower                                                   |
| django_template            | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.1 ms: 1.11x slower                                                  |
| telco                      | 6.53 ms                                                | 7.24 ms: 1.11x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                  |
| pidigits                   | 184 ms                                                 | 207 ms: 1.12x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.45 ms: 1.29x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.6 ms: 8.21x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): unpickle_pure_python
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x