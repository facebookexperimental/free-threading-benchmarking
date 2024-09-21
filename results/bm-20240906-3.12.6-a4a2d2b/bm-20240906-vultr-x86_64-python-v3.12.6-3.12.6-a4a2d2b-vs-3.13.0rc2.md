# Results vs. 3.13.0rc2

- fork: python
- ref: v3.12.6
- machine: linux-x86_64
- commit hash: a4a2d2b
- commit date: 2024-09-06
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 264 ms: 1.01x slower                                   |
| docutils       | 2.62 sec                                                     | 2.64 sec: 1.01x slower                                 |
| html5lib       | 67.0 ms                                                      | 63.6 ms: 1.05x faster                                  |
| tornado_http   | 114 ms                                                       | 119 ms: 1.04x slower                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                           |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.02x slower                                  |
| async_generators           | 377 ms                                                       | 384 ms: 1.02x slower                                   |
| asyncio_tcp                | 505 ms                                                       | 519 ms: 1.03x slower                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 715 ms: 1.07x slower                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 723 ms: 1.13x slower                                   |
| async_tree_memoization     | 461 ms                                                       | 555 ms: 1.20x slower                                   |
| async_tree_io_tg           | 913 ms                                                       | 1.11 sec: 1.21x slower                                 |
| async_tree_io              | 876 ms                                                       | 1.08 sec: 1.24x slower                                 |
| async_tree_none            | 354 ms                                                       | 464 ms: 1.31x slower                                   |
| async_tree_none_tg         | 336 ms                                                       | 446 ms: 1.33x slower                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 560 ms: 1.35x slower                                   |
| Geometric mean             | (ref)                                                        | 1.14x slower                                           |

Benchmark hidden because not significant (1): asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                   |
| float          | 77.5 ms                                                      | 80.8 ms: 1.04x slower                                  |
| nbody          | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.6 ms: 1.10x faster                                  |
| regex_dna      | 180 ms                                                       | 168 ms: 1.07x faster                                   |
| regex_effbot   | 3.08 ms                                                      | 3.17 ms: 1.03x slower                                  |
| regex_compile  | 132 ms                                                       | 142 ms: 1.08x slower                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| pickle               | 11.3 us                                                      | 10.9 us: 1.04x faster                                  |
| pickle_list          | 4.93 us                                                      | 4.77 us: 1.03x faster                                  |
| pickle_dict          | 32.5 us                                                      | 31.8 us: 1.02x faster                                  |
| json_loads           | 27.0 us                                                      | 26.5 us: 1.02x faster                                  |
| json_dumps           | 10.5 ms                                                      | 10.4 ms: 1.02x faster                                  |
| unpickle_list        | 4.71 us                                                      | 4.67 us: 1.01x faster                                  |
| xml_etree_process    | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                  |
| xml_etree_generate   | 85.4 ms                                                      | 85.2 ms: 1.00x faster                                  |
| xml_etree_parse      | 136 ms                                                       | 139 ms: 1.02x slower                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.7 ms: 1.02x slower                                  |
| pickle_pure_python   | 294 us                                                       | 308 us: 1.04x slower                                   |
| unpickle_pure_python | 210 us                                                       | 221 us: 1.05x slower                                   |
| tomli_loads          | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                 |
| Geometric mean       | (ref)                                                        | 1.00x slower                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 11.0 ms                                                      | 9.93 ms: 1.11x faster                                  |
| python_startup_no_site | 7.39 ms                                                      | 7.16 ms: 1.03x faster                                  |
| Geometric mean         | (ref)                                                        | 1.07x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.0 ms: 1.03x faster                                  |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                  |
| genshi_xml      | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                  |
| genshi_text     | 21.5 ms                                                      | 22.8 ms: 1.06x slower                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| create_gc_cycles           | 1.34 ms                                                      | 1.09 ms: 1.23x faster                                  |
| telco                      | 7.82 ms                                                      | 6.53 ms: 1.20x faster                                  |
| flaskblogging              | 3.58 ms                                                      | 3.03 ms: 1.18x faster                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                   |
| coverage                   | 83.0 ms                                                      | 71.4 ms: 1.16x faster                                  |
| python_startup             | 11.0 ms                                                      | 9.93 ms: 1.11x faster                                  |
| regex_v8                   | 22.7 ms                                                      | 20.6 ms: 1.10x faster                                  |
| regex_dna                  | 180 ms                                                       | 168 ms: 1.07x faster                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.39 ms: 1.07x faster                                  |
| html5lib                   | 67.0 ms                                                      | 63.6 ms: 1.05x faster                                  |
| scimark_sor                | 134 ms                                                       | 130 ms: 1.04x faster                                   |
| pickle                     | 11.3 us                                                      | 10.9 us: 1.04x faster                                  |
| pickle_list                | 4.93 us                                                      | 4.77 us: 1.03x faster                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.16 ms: 1.03x faster                                  |
| mako                       | 11.3 ms                                                      | 11.0 ms: 1.03x faster                                  |
| gunicorn                   | 1.11 ms                                                      | 1.08 ms: 1.02x faster                                  |
| pickle_dict                | 32.5 us                                                      | 31.8 us: 1.02x faster                                  |
| scimark_fft                | 349 ms                                                       | 342 ms: 1.02x faster                                   |
| aiohttp                    | 1.07 ms                                                      | 1.04 ms: 1.02x faster                                  |
| bench_mp_pool              | 11.0 ms                                                      | 10.8 ms: 1.02x faster                                  |
| json_loads                 | 27.0 us                                                      | 26.5 us: 1.02x faster                                  |
| json_dumps                 | 10.5 ms                                                      | 10.4 ms: 1.02x faster                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.08 us: 1.01x faster                                  |
| go                         | 141 ms                                                       | 139 ms: 1.01x faster                                   |
| deepcopy                   | 355 us                                                       | 352 us: 1.01x faster                                   |
| unpickle_list              | 4.71 us                                                      | 4.67 us: 1.01x faster                                  |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                   |
| xml_etree_process          | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                  |
| xml_etree_generate         | 85.4 ms                                                      | 85.2 ms: 1.00x faster                                  |
| fannkuch                   | 370 ms                                                       | 372 ms: 1.01x slower                                   |
| pprint_safe_repr           | 738 ms                                                       | 743 ms: 1.01x slower                                   |
| sqlglot_normalize          | 106 ms                                                       | 107 ms: 1.01x slower                                   |
| docutils                   | 2.62 sec                                                     | 2.64 sec: 1.01x slower                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 53.3 ms: 1.01x slower                                  |
| scimark_lu                 | 113 ms                                                       | 114 ms: 1.01x slower                                   |
| 2to3                       | 260 ms                                                       | 264 ms: 1.01x slower                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.52 sec: 1.02x slower                                 |
| richards                   | 45.2 ms                                                      | 45.9 ms: 1.02x slower                                  |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.02x slower                                  |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                  |
| thrift                     | 778 us                                                       | 791 us: 1.02x slower                                   |
| xml_etree_parse            | 136 ms                                                       | 139 ms: 1.02x slower                                   |
| nqueens                    | 78.6 ms                                                      | 80.1 ms: 1.02x slower                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 96.7 ms: 1.02x slower                                  |
| meteor_contest             | 102 ms                                                       | 104 ms: 1.02x slower                                   |
| async_generators           | 377 ms                                                       | 384 ms: 1.02x slower                                   |
| json                       | 4.93 ms                                                      | 5.02 ms: 1.02x slower                                  |
| sympy_expand               | 457 ms                                                       | 468 ms: 1.02x slower                                   |
| bench_thread_pool          | 919 us                                                       | 941 us: 1.02x slower                                   |
| asyncio_tcp                | 505 ms                                                       | 519 ms: 1.03x slower                                   |
| regex_effbot               | 3.08 ms                                                      | 3.17 ms: 1.03x slower                                  |
| mdp                        | 2.36 sec                                                     | 2.42 sec: 1.03x slower                                 |
| genshi_xml                 | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                  |
| hexiom                     | 5.99 ms                                                      | 6.17 ms: 1.03x slower                                  |
| deepcopy_memo              | 39.1 us                                                      | 40.3 us: 1.03x slower                                  |
| dask                       | 400 ms                                                       | 413 ms: 1.03x slower                                   |
| sympy_integrate            | 19.8 ms                                                      | 20.5 ms: 1.04x slower                                  |
| float                      | 77.5 ms                                                      | 80.8 ms: 1.04x slower                                  |
| pickle_pure_python         | 294 us                                                       | 308 us: 1.04x slower                                   |
| tornado_http               | 114 ms                                                       | 119 ms: 1.04x slower                                   |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 68.4 ms: 1.05x slower                                  |
| nbody                      | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                  |
| unpickle_pure_python       | 210 us                                                       | 221 us: 1.05x slower                                   |
| tomli_loads                | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                 |
| dulwich_log                | 74.8 ms                                                      | 78.9 ms: 1.05x slower                                  |
| typing_runtime_protocols   | 155 us                                                       | 163 us: 1.06x slower                                   |
| genshi_text                | 21.5 ms                                                      | 22.8 ms: 1.06x slower                                  |
| sympy_str                  | 275 ms                                                       | 292 ms: 1.06x slower                                   |
| logging_silent             | 103 ns                                                       | 109 ns: 1.06x slower                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.74 sec: 1.07x slower                                 |
| sympy_sum                  | 156 ms                                                       | 166 ms: 1.07x slower                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 1.67 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 715 ms: 1.07x slower                                   |
| logging_format             | 6.84 us                                                      | 7.35 us: 1.07x slower                                  |
| logging_simple             | 6.16 us                                                      | 6.63 us: 1.08x slower                                  |
| regex_compile              | 132 ms                                                       | 142 ms: 1.08x slower                                   |
| sqlglot_parse              | 1.25 ms                                                      | 1.36 ms: 1.09x slower                                  |
| chaos                      | 57.3 ms                                                      | 62.8 ms: 1.10x slower                                  |
| gc_traversal               | 3.14 ms                                                      | 3.46 ms: 1.10x slower                                  |
| deltablue                  | 3.12 ms                                                      | 3.45 ms: 1.10x slower                                  |
| generators                 | 28.8 ms                                                      | 32.2 ms: 1.12x slower                                  |
| pathlib                    | 19.2 ms                                                      | 21.5 ms: 1.12x slower                                  |
| crypto_pyaes               | 67.9 ms                                                      | 76.6 ms: 1.13x slower                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 723 ms: 1.13x slower                                   |
| unpack_sequence            | 44.8 ns                                                      | 52.1 ns: 1.16x slower                                  |
| raytrace                   | 253 ms                                                       | 299 ms: 1.18x slower                                   |
| async_tree_memoization     | 461 ms                                                       | 555 ms: 1.20x slower                                   |
| comprehensions             | 16.5 us                                                      | 19.8 us: 1.21x slower                                  |
| async_tree_io_tg           | 913 ms                                                       | 1.11 sec: 1.21x slower                                 |
| async_tree_io              | 876 ms                                                       | 1.08 sec: 1.24x slower                                 |
| async_tree_none            | 354 ms                                                       | 464 ms: 1.31x slower                                   |
| async_tree_none_tg         | 336 ms                                                       | 446 ms: 1.33x slower                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 560 ms: 1.35x slower                                   |
| Geometric mean             | (ref)                                                        | 1.03x slower                                           |

Benchmark hidden because not significant (7): unpickle, sqlite_synth, asyncio_tcp_ssl, pyflate, pylint, richards_super, chameleon
Ignored benchmarks (3) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.99x