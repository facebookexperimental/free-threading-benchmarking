# Results vs. 3.12.6

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.096x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 610 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 263 ms: 1.77x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 319 ms: 1.74x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 481 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                   |
| async_generators           | 384 ms                                                 | 318 ms: 1.21x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                  |
| nbody          | 89.3 ms                                                | 91.2 ms: 1.02x slower                                                  |
| pidigits       | 184 ms                                                 | 207 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                  |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads         | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                 |
| xml_etree_parse     | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| xml_etree_iterparse | 96.7 ms                                                | 90.5 ms: 1.07x faster                                                  |
| xml_etree_generate  | 85.2 ms                                                | 82.7 ms: 1.03x faster                                                  |
| xml_etree_process   | 59.0 ms                                                | 60.3 ms: 1.02x slower                                                  |
| pickle_pure_python  | 308 us                                                 | 317 us: 1.03x slower                                                   |
| json_loads          | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| json_dumps          | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.4 ms: 1.07x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 49.0 ms: 1.02x faster                                                  |
| django_template | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 610 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 263 ms: 1.77x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 319 ms: 1.74x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 481 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                   |
| deepcopy                   | 352 us                                                 | 254 us: 1.39x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.9 us: 1.35x faster                                                  |
| go                         | 139 ms                                                 | 112 ms: 1.24x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                  |
| async_generators           | 384 ms                                                 | 318 ms: 1.21x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.6 us: 1.20x faster                                                  |
| spectral_norm              | 110 ms                                                 | 92.2 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                  |
| generators                 | 32.2 ms                                                | 27.5 ms: 1.17x faster                                                  |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.16x faster                                                   |
| float                      | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.8 ms: 1.15x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 67.0 ms: 1.14x faster                                                  |
| raytrace                   | 299 ms                                                 | 262 ms: 1.14x faster                                                   |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.05 ms: 1.13x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.4 ms: 1.13x faster                                                  |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| scimark_fft                | 342 ms                                                 | 305 ms: 1.12x faster                                                   |
| richards                   | 45.9 ms                                                | 41.0 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 129 ms: 1.10x faster                                                   |
| richards_super             | 51.9 ms                                                | 47.2 ms: 1.10x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.25 ms: 1.09x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 63.2 ms: 1.08x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.70 ms: 1.08x faster                                                  |
| pyflate                    | 448 ms                                                 | 415 ms: 1.08x faster                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.55 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.10 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.5 ms: 1.07x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.4 ms: 1.07x faster                                                  |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                 |
| meteor_contest             | 104 ms                                                 | 97.4 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 703 ms: 1.06x faster                                                   |
| thrift                     | 791 us                                                 | 749 us: 1.06x faster                                                   |
| mdp                        | 2.42 sec                                               | 2.30 sec: 1.05x faster                                                 |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.36 us: 1.04x faster                                                  |
| nqueens                    | 80.1 ms                                                | 76.9 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                   |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 76.5 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 82.7 ms: 1.03x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 49.0 ms: 1.02x faster                                                  |
| logging_format             | 7.35 us                                                | 7.18 us: 1.02x faster                                                  |
| sqlglot_normalize          | 107 ms                                                 | 104 ms: 1.02x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                   |
| sympy_expand               | 468 ms                                                 | 459 ms: 1.02x faster                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 52.4 ms: 1.02x faster                                                  |
| fannkuch                   | 372 ms                                                 | 367 ms: 1.01x faster                                                   |
| json                       | 5.02 ms                                                | 4.98 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.19 us: 1.01x faster                                                  |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| nbody                      | 89.3 ms                                                | 91.2 ms: 1.02x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 60.3 ms: 1.02x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 317 us: 1.03x slower                                                   |
| django_template            | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.07x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.6 ms: 1.11x slower                                                  |
| telco                      | 6.53 ms                                                | 7.28 ms: 1.12x slower                                                  |
| pidigits                   | 184 ms                                                 | 207 ms: 1.12x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.99 ms: 1.15x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 89.7 ms: 8.30x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): unpickle_pure_python
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.11x