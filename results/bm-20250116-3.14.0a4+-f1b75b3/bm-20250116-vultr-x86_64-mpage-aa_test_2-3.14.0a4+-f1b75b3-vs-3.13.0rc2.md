# Results vs. 3.13.0rc2

- fork: mpage
- ref: aa_test_2
- machine: linux-x86_64
- commit hash: f1b75b3
- commit date: 2025-01-16
- overall geometric mean: 1.046x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 256 ms: 1.01x faster                                       |
| docutils       | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                     |
| Geometric mean | (ref)                                                        | 1.01x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.50x faster                                       |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 328 ms: 1.41x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.34x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 476 ms: 1.34x faster                                       |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.31x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                       |
| async_generators           | 377 ms                                                       | 326 ms: 1.16x faster                                       |
| coroutines                 | 23.6 ms                                                      | 22.0 ms: 1.07x faster                                      |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                       |
| Geometric mean             | (ref)                                                        | 1.28x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 196 ms: 1.11x faster                                       |
| float          | 77.5 ms                                                      | 72.7 ms: 1.06x faster                                      |
| nbody          | 85.1 ms                                                      | 90.1 ms: 1.06x slower                                      |
| Geometric mean | (ref)                                                        | 1.04x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                      |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                       |
| regex_compile  | 132 ms                                                       | 128 ms: 1.03x faster                                       |
| regex_v8       | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                        | 1.04x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                       |
| tomli_loads          | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                      |
| xml_etree_generate   | 85.4 ms                                                      | 85.0 ms: 1.00x faster                                      |
| xml_etree_process    | 59.3 ms                                                      | 59.7 ms: 1.01x slower                                      |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.02x slower                                       |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                      |
| pickle_pure_python   | 294 us                                                       | 321 us: 1.09x slower                                       |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                      |
| Geometric mean       | (ref)                                                        | 1.01x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                      |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                      |
| Geometric mean         | (ref)                                                        | 1.16x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.4 ms: 1.01x slower                                      |
| django_template | 34.1 ms                                                      | 35.9 ms: 1.05x slower                                      |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                      |
| Geometric mean  | (ref)                                                        | 1.03x slower                                               |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.50x faster                                       |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 328 ms: 1.41x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                       |
| deepcopy                   | 355 us                                                       | 262 us: 1.36x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.34x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 476 ms: 1.34x faster                                       |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.31x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                       |
| deepcopy_memo              | 39.1 us                                                      | 31.2 us: 1.25x faster                                      |
| spectral_norm              | 111 ms                                                       | 91.1 ms: 1.22x faster                                      |
| go                         | 141 ms                                                       | 117 ms: 1.21x faster                                       |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.17x faster                                      |
| async_generators           | 377 ms                                                       | 326 ms: 1.16x faster                                       |
| scimark_sor                | 134 ms                                                       | 116 ms: 1.16x faster                                       |
| regex_effbot               | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                      |
| pylint                     | 317 ms                                                       | 282 ms: 1.13x faster                                       |
| scimark_fft                | 349 ms                                                       | 312 ms: 1.12x faster                                       |
| pidigits                   | 217 ms                                                       | 196 ms: 1.11x faster                                       |
| telco                      | 7.82 ms                                                      | 7.17 ms: 1.09x faster                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.35 ms: 1.08x faster                                      |
| coroutines                 | 23.6 ms                                                      | 22.0 ms: 1.07x faster                                      |
| pyflate                    | 449 ms                                                       | 420 ms: 1.07x faster                                       |
| float                      | 77.5 ms                                                      | 72.7 ms: 1.06x faster                                      |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                       |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                     |
| richards_super             | 51.6 ms                                                      | 49.1 ms: 1.05x faster                                      |
| thrift                     | 778 us                                                       | 740 us: 1.05x faster                                       |
| richards                   | 45.2 ms                                                      | 43.0 ms: 1.05x faster                                      |
| coverage                   | 83.0 ms                                                      | 79.3 ms: 1.05x faster                                      |
| tomli_loads                | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                      |
| pprint_safe_repr           | 738 ms                                                       | 712 ms: 1.04x faster                                       |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                       |
| regex_compile              | 132 ms                                                       | 128 ms: 1.03x faster                                       |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                     |
| hexiom                     | 5.99 ms                                                      | 5.81 ms: 1.03x faster                                      |
| generators                 | 28.8 ms                                                      | 28.1 ms: 1.02x faster                                      |
| meteor_contest             | 102 ms                                                       | 99.9 ms: 1.02x faster                                      |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.02x faster                                       |
| 2to3                       | 260 ms                                                       | 256 ms: 1.01x faster                                       |
| mdp                        | 2.36 sec                                                     | 2.32 sec: 1.01x faster                                     |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                      |
| docutils                   | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                     |
| crypto_pyaes               | 67.9 ms                                                      | 67.1 ms: 1.01x faster                                      |
| chaos                      | 57.3 ms                                                      | 56.7 ms: 1.01x faster                                      |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                       |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.8 ms: 1.01x faster                                      |
| sqlglot_optimize           | 52.7 ms                                                      | 52.4 ms: 1.01x faster                                      |
| xml_etree_generate         | 85.4 ms                                                      | 85.0 ms: 1.00x faster                                      |
| sqlglot_normalize          | 106 ms                                                       | 105 ms: 1.00x faster                                       |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                       |
| sqlglot_transpile          | 1.56 ms                                                      | 1.57 ms: 1.00x slower                                      |
| sympy_expand               | 457 ms                                                       | 460 ms: 1.01x slower                                       |
| xml_etree_process          | 59.3 ms                                                      | 59.7 ms: 1.01x slower                                      |
| sympy_integrate            | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                      |
| python_startup_no_site     | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                      |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                       |
| sqlglot_parse              | 1.25 ms                                                      | 1.26 ms: 1.01x slower                                      |
| genshi_xml                 | 48.8 ms                                                      | 49.4 ms: 1.01x slower                                      |
| logging_simple             | 6.16 us                                                      | 6.24 us: 1.01x slower                                      |
| comprehensions             | 16.5 us                                                      | 16.7 us: 1.02x slower                                      |
| deltablue                  | 3.12 ms                                                      | 3.18 ms: 1.02x slower                                      |
| dulwich_log                | 74.8 ms                                                      | 76.3 ms: 1.02x slower                                      |
| fannkuch                   | 370 ms                                                       | 377 ms: 1.02x slower                                       |
| logging_format             | 6.84 us                                                      | 6.99 us: 1.02x slower                                      |
| json                       | 4.93 ms                                                      | 5.04 ms: 1.02x slower                                      |
| unpickle_pure_python       | 210 us                                                       | 215 us: 1.02x slower                                       |
| regex_v8                   | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                      |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                      |
| logging_silent             | 103 ns                                                       | 107 ns: 1.05x slower                                       |
| django_template            | 34.1 ms                                                      | 35.9 ms: 1.05x slower                                      |
| raytrace                   | 253 ms                                                       | 267 ms: 1.06x slower                                       |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                      |
| nbody                      | 85.1 ms                                                      | 90.1 ms: 1.06x slower                                      |
| pickle_pure_python         | 294 us                                                       | 321 us: 1.09x slower                                       |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                      |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.13x slower                                      |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                      |
| gc_traversal               | 3.14 ms                                                      | 4.78 ms: 1.52x slower                                      |
| bench_mp_pool              | 11.0 ms                                                      | 88.7 ms: 8.07x slower                                      |
| Geometric mean             | (ref)                                                        | 1.02x faster                                               |

Benchmark hidden because not significant (4): sympy_str, pycparser, genshi_text, nqueens
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250116-3.14.0a4+-f1b75b3/bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.046x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x