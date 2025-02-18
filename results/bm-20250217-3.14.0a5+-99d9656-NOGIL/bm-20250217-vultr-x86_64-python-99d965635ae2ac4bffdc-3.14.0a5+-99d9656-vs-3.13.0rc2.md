# Results vs. 3.13.0rc2

- fork: python
- ref: 99d965635ae2ac4bffdc
- machine: linux-x86_64
- commit hash: 99d9656
- commit date: 2025-02-17
- overall geometric mean: 1.080x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 302 ms: 1.17x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.06x slower                                                 |
| html5lib       | 68.6 ms                                                                | 72.1 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 582 ms: 1.55x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 609 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 352 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 321 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 505 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 537 ms: 1.24x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 288 ms: 1.23x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.23x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 208 ms: 1.04x faster                                                   |
| float          | 76.7 ms                                                                | 75.5 ms: 1.02x faster                                                  |
| nbody          | 85.3 ms                                                                | 129 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                  |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                  |
| regex_compile  | 131 ms                                                                 | 154 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                                | 96.0 ms: 1.12x slower                                                  |
| json_loads           | 27.3 us                                                                | 31.2 us: 1.14x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 70.2 ms: 1.19x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 252 us: 1.21x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 361 us: 1.24x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.60 ms: 1.29x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                                  |
| django_template | 34.2 ms                                                                | 42.0 ms: 1.23x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                                  |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.73 ms: 1.91x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 582 ms: 1.55x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 609 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 352 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 321 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 505 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 537 ms: 1.24x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 288 ms: 1.23x faster                                                   |
| deepcopy                   | 357 us                                                                 | 307 us: 1.16x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| pidigits                   | 216 ms                                                                 | 208 ms: 1.04x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                   |
| float                      | 76.7 ms                                                                | 75.5 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 38.3 us: 1.01x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.02x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.03x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.04x slower                                                   |
| html5lib                   | 68.6 ms                                                                | 72.1 ms: 1.05x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.69 sec: 1.05x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.06x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.07x slower                                                 |
| json                       | 4.98 ms                                                                | 5.38 ms: 1.08x slower                                                  |
| pyflate                    | 449 ms                                                                 | 496 ms: 1.10x slower                                                   |
| dulwich_log                | 74.5 ms                                                                | 82.4 ms: 1.11x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.60 sec: 1.11x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.63 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 96.0 ms: 1.12x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 814 ms: 1.13x slower                                                   |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.14x slower                                                   |
| generators                 | 28.5 ms                                                                | 32.5 ms: 1.14x slower                                                  |
| json_loads                 | 27.3 us                                                                | 31.2 us: 1.14x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 403 ms: 1.16x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.69 sec: 1.16x slower                                                 |
| 2to3                       | 259 ms                                                                 | 302 ms: 1.17x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 115 ns: 1.17x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 61.5 ms: 1.17x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.18 us: 1.17x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                                 |
| regex_compile              | 131 ms                                                                 | 154 ms: 1.17x slower                                                   |
| thrift                     | 772 us                                                                 | 906 us: 1.17x slower                                                   |
| logging_format             | 6.92 us                                                                | 8.18 us: 1.18x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 70.2 ms: 1.19x slower                                                  |
| coverage                   | 82.5 ms                                                                | 98.1 ms: 1.19x slower                                                  |
| comprehensions             | 16.6 us                                                                | 19.9 us: 1.20x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.20x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 547 ms: 1.21x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 252 us: 1.21x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.76 ms: 1.21x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 24.0 ms: 1.22x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.90 ms: 1.22x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 335 ms: 1.22x slower                                                   |
| django_template            | 34.2 ms                                                                | 42.0 ms: 1.23x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 361 us: 1.24x slower                                                   |
| hexiom                     | 5.95 ms                                                                | 7.39 ms: 1.24x slower                                                  |
| richards                   | 44.4 ms                                                                | 55.3 ms: 1.25x slower                                                  |
| chaos                      | 56.3 ms                                                                | 70.3 ms: 1.25x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 97.4 ms: 1.25x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.58 ms: 1.26x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.3 ms: 1.27x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.92 ms: 1.27x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 143 ms: 1.27x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                   |
| genshi_text                | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                                   |
| richards_super             | 50.4 ms                                                                | 64.3 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.60 ms: 1.29x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 88.4 ms: 1.30x slower                                                  |
| raytrace                   | 250 ms                                                                 | 326 ms: 1.31x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 494 ms: 1.31x slower                                                   |
| python_startup             | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                  |
| nbody                      | 85.3 ms                                                                | 129 ms: 1.51x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.31 ms: 3.58x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 95.0 ms: 8.64x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (5): pylint, deepcopy_reduce, scimark_sor, async_generators, go
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.080x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x