# Results vs. 3.12.6

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.45x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 403 ms: 1.53x slower                                         |
| chameleon      | 6.88 ms                                                | 12.2 ms: 1.77x slower                                        |
| docutils       | 2.64 sec                                               | 3.30 sec: 1.25x slower                                       |
| html5lib       | 63.6 ms                                                | 105 ms: 1.66x slower                                         |
| tornado_http   | 119 ms                                                 | 157 ms: 1.32x slower                                         |
| Geometric mean | (ref)                                                  | 1.49x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 918 ms: 1.21x faster                                         |
| async_tree_io              | 1.08 sec                                               | 952 ms: 1.14x faster                                         |
| async_tree_memoization_tg  | 560 ms                                                 | 501 ms: 1.12x faster                                         |
| async_tree_none_tg         | 446 ms                                                 | 406 ms: 1.10x faster                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 665 ms: 1.09x faster                                         |
| async_tree_none            | 464 ms                                                 | 447 ms: 1.04x faster                                         |
| async_tree_memoization     | 555 ms                                                 | 539 ms: 1.03x faster                                         |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 704 ms: 1.02x faster                                         |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                         |
| asyncio_tcp                | 519 ms                                                 | 574 ms: 1.11x slower                                         |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.70 sec: 1.13x slower                                       |
| async_generators           | 384 ms                                                 | 484 ms: 1.26x slower                                         |
| coroutines                 | 23.9 ms                                                | 31.9 ms: 1.33x slower                                        |
| Geometric mean             | (ref)                                                  | 1.00x slower                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                         |
| float          | 80.8 ms                                                | 152 ms: 1.88x slower                                         |
| nbody          | 89.3 ms                                                | 218 ms: 2.44x slower                                         |
| Geometric mean | (ref)                                                  | 1.67x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.04 ms: 1.04x faster                                        |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                         |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                        |
| regex_compile  | 142 ms                                                 | 226 ms: 1.58x slower                                         |
| Geometric mean | (ref)                                                  | 1.18x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                         |
| pickle               | 10.9 us                                                | 10.6 us: 1.03x faster                                        |
| pickle_list          | 4.77 us                                                | 4.72 us: 1.01x faster                                        |
| pickle_dict          | 31.8 us                                                | 32.2 us: 1.01x slower                                        |
| xml_etree_iterparse  | 96.7 ms                                                | 106 ms: 1.10x slower                                         |
| unpickle             | 14.1 us                                                | 15.4 us: 1.10x slower                                        |
| unpickle_list        | 4.67 us                                                | 5.26 us: 1.12x slower                                        |
| json_loads           | 26.5 us                                                | 30.2 us: 1.14x slower                                        |
| xml_etree_generate   | 85.2 ms                                                | 111 ms: 1.30x slower                                         |
| json_dumps           | 10.4 ms                                                | 13.6 ms: 1.31x slower                                        |
| tomli_loads          | 2.11 sec                                               | 3.24 sec: 1.54x slower                                       |
| xml_etree_process    | 59.0 ms                                                | 92.0 ms: 1.56x slower                                        |
| unpickle_pure_python | 221 us                                                 | 407 us: 1.85x slower                                         |
| pickle_pure_python   | 308 us                                                 | 585 us: 1.90x slower                                         |
| Geometric mean       | (ref)                                                  | 1.24x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.64 ms: 1.35x slower                                        |
| python_startup         | 9.93 ms                                                | 14.8 ms: 1.49x slower                                        |
| Geometric mean         | (ref)                                                  | 1.42x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 79.2 ms: 1.58x slower                                        |
| genshi_text     | 22.8 ms                                                | 39.3 ms: 1.72x slower                                        |
| mako            | 11.0 ms                                                | 19.7 ms: 1.79x slower                                        |
| django_template | 34.7 ms                                                | 63.0 ms: 1.82x slower                                        |
| Geometric mean  | (ref)                                                  | 1.72x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 2.54 ms: 1.36x faster                                        |
| async_tree_io_tg           | 1.11 sec                                               | 918 ms: 1.21x faster                                         |
| async_tree_io              | 1.08 sec                                               | 952 ms: 1.14x faster                                         |
| async_tree_memoization_tg  | 560 ms                                                 | 501 ms: 1.12x faster                                         |
| async_tree_none_tg         | 446 ms                                                 | 406 ms: 1.10x faster                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 665 ms: 1.09x faster                                         |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                         |
| regex_effbot               | 3.17 ms                                                | 3.04 ms: 1.04x faster                                        |
| async_tree_none            | 464 ms                                                 | 447 ms: 1.04x faster                                         |
| pickle                     | 10.9 us                                                | 10.6 us: 1.03x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 539 ms: 1.03x faster                                         |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 704 ms: 1.02x faster                                         |
| pickle_list                | 4.77 us                                                | 4.72 us: 1.01x faster                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.10 ms: 1.01x slower                                        |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                         |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                         |
| pickle_dict                | 31.8 us                                                | 32.2 us: 1.01x slower                                        |
| xml_etree_iterparse        | 96.7 ms                                                | 106 ms: 1.10x slower                                         |
| unpickle                   | 14.1 us                                                | 15.4 us: 1.10x slower                                        |
| json                       | 5.02 ms                                                | 5.52 ms: 1.10x slower                                        |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                         |
| sqlite_synth               | 2.20 us                                                | 2.43 us: 1.10x slower                                        |
| asyncio_tcp                | 519 ms                                                 | 574 ms: 1.11x slower                                         |
| pathlib                    | 21.5 ms                                                | 24.0 ms: 1.11x slower                                        |
| unpickle_list              | 4.67 us                                                | 5.26 us: 1.12x slower                                        |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.70 sec: 1.13x slower                                       |
| bench_mp_pool              | 10.8 ms                                                | 12.2 ms: 1.13x slower                                        |
| json_loads                 | 26.5 us                                                | 30.2 us: 1.14x slower                                        |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                        |
| docutils                   | 2.64 sec                                               | 3.30 sec: 1.25x slower                                       |
| async_generators           | 384 ms                                                 | 484 ms: 1.26x slower                                         |
| generators                 | 32.2 ms                                                | 40.7 ms: 1.26x slower                                        |
| mdp                        | 2.42 sec                                               | 3.11 sec: 1.29x slower                                       |
| pylint                     | 319 ms                                                 | 415 ms: 1.30x slower                                         |
| xml_etree_generate         | 85.2 ms                                                | 111 ms: 1.30x slower                                         |
| dulwich_log                | 78.9 ms                                                | 103 ms: 1.31x slower                                         |
| json_dumps                 | 10.4 ms                                                | 13.6 ms: 1.31x slower                                        |
| tornado_http               | 119 ms                                                 | 157 ms: 1.32x slower                                         |
| coroutines                 | 23.9 ms                                                | 31.9 ms: 1.33x slower                                        |
| gunicorn                   | 1.08 ms                                                | 1.45 ms: 1.34x slower                                        |
| meteor_contest             | 104 ms                                                 | 139 ms: 1.34x slower                                         |
| bpe_tokeniser              | 4.74 sec                                               | 6.36 sec: 1.34x slower                                       |
| python_startup_no_site     | 7.16 ms                                                | 9.64 ms: 1.35x slower                                        |
| aiohttp                    | 1.04 ms                                                | 1.41 ms: 1.35x slower                                        |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.99 ms: 1.36x slower                                        |
| scimark_fft                | 342 ms                                                 | 476 ms: 1.39x slower                                         |
| crypto_pyaes               | 76.6 ms                                                | 107 ms: 1.40x slower                                         |
| pycparser                  | 1.17 sec                                               | 1.68 sec: 1.44x slower                                       |
| telco                      | 6.53 ms                                                | 9.38 ms: 1.44x slower                                        |
| nqueens                    | 80.1 ms                                                | 118 ms: 1.47x slower                                         |
| coverage                   | 71.4 ms                                                | 105 ms: 1.47x slower                                         |
| comprehensions             | 19.8 us                                                | 29.3 us: 1.48x slower                                        |
| fannkuch                   | 372 ms                                                 | 556 ms: 1.49x slower                                         |
| python_startup             | 9.93 ms                                                | 14.8 ms: 1.49x slower                                        |
| typing_runtime_protocols   | 163 us                                                 | 246 us: 1.51x slower                                         |
| 2to3                       | 264 ms                                                 | 403 ms: 1.53x slower                                         |
| tomli_loads                | 2.11 sec                                               | 3.24 sec: 1.54x slower                                       |
| sympy_integrate            | 20.5 ms                                                | 31.7 ms: 1.54x slower                                        |
| xml_etree_process          | 59.0 ms                                                | 92.0 ms: 1.56x slower                                        |
| genshi_xml                 | 50.2 ms                                                | 79.2 ms: 1.58x slower                                        |
| regex_compile              | 142 ms                                                 | 226 ms: 1.58x slower                                         |
| thrift                     | 791 us                                                 | 1.26 ms: 1.59x slower                                        |
| spectral_norm              | 110 ms                                                 | 179 ms: 1.62x slower                                         |
| deepcopy_memo              | 40.3 us                                                | 65.7 us: 1.63x slower                                        |
| deepcopy                   | 352 us                                                 | 579 us: 1.65x slower                                         |
| html5lib                   | 63.6 ms                                                | 105 ms: 1.66x slower                                         |
| sqlglot_normalize          | 107 ms                                                 | 177 ms: 1.66x slower                                         |
| sqlglot_optimize           | 53.3 ms                                                | 88.7 ms: 1.67x slower                                        |
| deepcopy_reduce            | 3.08 us                                                | 5.22 us: 1.70x slower                                        |
| pyflate                    | 448 ms                                                 | 764 ms: 1.71x slower                                         |
| genshi_text                | 22.8 ms                                                | 39.3 ms: 1.72x slower                                        |
| pprint_safe_repr           | 743 ms                                                 | 1.29 sec: 1.74x slower                                       |
| pprint_pformat             | 1.52 sec                                               | 2.67 sec: 1.76x slower                                       |
| chameleon                  | 6.88 ms                                                | 12.2 ms: 1.77x slower                                        |
| mako                       | 11.0 ms                                                | 19.7 ms: 1.79x slower                                        |
| sympy_str                  | 292 ms                                                 | 524 ms: 1.80x slower                                         |
| logging_format             | 7.35 us                                                | 13.3 us: 1.81x slower                                        |
| django_template            | 34.7 ms                                                | 63.0 ms: 1.82x slower                                        |
| logging_simple             | 6.63 us                                                | 12.1 us: 1.82x slower                                        |
| scimark_monte_carlo        | 68.4 ms                                                | 126 ms: 1.84x slower                                         |
| unpickle_pure_python       | 221 us                                                 | 407 us: 1.85x slower                                         |
| float                      | 80.8 ms                                                | 152 ms: 1.88x slower                                         |
| logging_silent             | 109 ns                                                 | 207 ns: 1.90x slower                                         |
| pickle_pure_python         | 308 us                                                 | 585 us: 1.90x slower                                         |
| sqlglot_transpile          | 1.67 ms                                                | 3.25 ms: 1.95x slower                                        |
| richards                   | 45.9 ms                                                | 90.0 ms: 1.96x slower                                        |
| hexiom                     | 6.17 ms                                                | 12.2 ms: 1.98x slower                                        |
| flaskblogging              | 3.03 ms                                                | 6.01 ms: 1.98x slower                                        |
| scimark_sor                | 130 ms                                                 | 260 ms: 2.01x slower                                         |
| chaos                      | 62.8 ms                                                | 126 ms: 2.01x slower                                         |
| richards_super             | 51.9 ms                                                | 105 ms: 2.03x slower                                         |
| sqlglot_parse              | 1.36 ms                                                | 2.80 ms: 2.07x slower                                        |
| raytrace                   | 299 ms                                                 | 622 ms: 2.08x slower                                         |
| scimark_lu                 | 114 ms                                                 | 239 ms: 2.09x slower                                         |
| sympy_expand               | 468 ms                                                 | 1.03 sec: 2.21x slower                                       |
| sympy_sum                  | 166 ms                                                 | 372 ms: 2.24x slower                                         |
| nbody                      | 89.3 ms                                                | 218 ms: 2.44x slower                                         |
| go                         | 139 ms                                                 | 358 ms: 2.57x slower                                         |
| unpack_sequence            | 52.1 ns                                                | 146 ns: 2.81x slower                                         |
| deltablue                  | 3.45 ms                                                | 9.99 ms: 2.90x slower                                        |
| bench_thread_pool          | 941 us                                                 | 2.74 ms: 2.91x slower                                        |
| Geometric mean             | (ref)                                                  | 1.45x slower                                                 |
Ignored benchmarks (4) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: dask, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.17x