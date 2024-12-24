# Results vs. 3.13.0rc2

- fork: python
- ref: 30efede33ca1fe32debb
- machine: linux-x86_64
- commit hash: 30efede
- commit date: 2024-12-24
- overall geometric mean: 1.049x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 256 ms: 1.01x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                   |
| async_tree_io              | 876 ms                                                       | 634 ms: 1.38x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 335 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 496 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.31x faster                                                   |
| async_tree_none            | 354 ms                                                       | 279 ms: 1.27x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                  |
| async_generators           | 377 ms                                                       | 353 ms: 1.07x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 76.2 ms: 1.02x faster                                                  |
| nbody          | 85.1 ms                                                      | 90.4 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                  |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 26.3 us: 1.03x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 83.4 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.02x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 311 us: 1.06x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.1 ms: 1.01x slower                                                  |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                   |
| deepcopy                   | 355 us                                                       | 254 us: 1.40x faster                                                   |
| async_tree_io              | 876 ms                                                       | 634 ms: 1.38x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 335 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 496 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.31x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.2 us: 1.29x faster                                                  |
| async_tree_none            | 354 ms                                                       | 279 ms: 1.27x faster                                                   |
| go                         | 141 ms                                                       | 116 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                  |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| scimark_sor                | 134 ms                                                       | 115 ms: 1.17x faster                                                   |
| spectral_norm              | 111 ms                                                       | 95.8 ms: 1.16x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                  |
| pylint                     | 317 ms                                                       | 281 ms: 1.13x faster                                                   |
| scimark_fft                | 349 ms                                                       | 319 ms: 1.09x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                  |
| async_generators           | 377 ms                                                       | 353 ms: 1.07x faster                                                   |
| pyflate                    | 449 ms                                                       | 420 ms: 1.07x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                   |
| thrift                     | 778 us                                                       | 730 us: 1.07x faster                                                   |
| richards_super             | 51.6 ms                                                      | 48.5 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.5 ms: 1.06x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.36 ms: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.46 ms: 1.06x faster                                                  |
| coverage                   | 83.0 ms                                                      | 78.9 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 705 ms: 1.05x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.7 ms: 1.04x faster                                                  |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.28 sec: 1.04x faster                                                 |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.1 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.62 us: 1.03x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.97 us: 1.03x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                   |
| json_loads                 | 27.0 us                                                      | 26.3 us: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.4 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| json                       | 4.93 ms                                                      | 4.82 ms: 1.02x faster                                                  |
| fannkuch                   | 370 ms                                                       | 362 ms: 1.02x faster                                                   |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.02x faster                                                   |
| float                      | 77.5 ms                                                      | 76.2 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.90 ms: 1.02x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| 2to3                       | 260 ms                                                       | 256 ms: 1.01x faster                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 52.1 ms: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 77.7 ms: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 273 ms: 1.01x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 67.5 ms: 1.01x faster                                                  |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.00x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| chaos                      | 57.3 ms                                                      | 57.6 ms: 1.01x slower                                                  |
| sympy_expand               | 457 ms                                                       | 460 ms: 1.01x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 49.1 ms: 1.01x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.15 ms: 1.01x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.5 ms: 1.01x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.58 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.02x slower                                                   |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.27 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.02x slower                                                   |
| raytrace                   | 253 ms                                                       | 260 ms: 1.03x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.0 us: 1.03x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.46 sec: 1.05x slower                                                 |
| logging_silent             | 103 ns                                                       | 107 ns: 1.05x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 311 us: 1.06x slower                                                   |
| nbody                      | 85.1 ms                                                      | 90.4 ms: 1.06x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.32 ms: 1.37x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 89.7 ms: 8.16x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (3): sqlite_synth, sympy_integrate, pycparser
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x