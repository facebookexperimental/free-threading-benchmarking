# Results vs. 3.12.6

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 260 ms: 1.01x faster                                         |
| docutils       | 2.64 sec                                               | 2.62 sec: 1.01x faster                                       |
| html5lib       | 63.6 ms                                                | 67.0 ms: 1.05x slower                                        |
| tornado_http   | 119 ms                                                 | 114 ms: 1.04x faster                                         |
| Geometric mean | (ref)                                                  | 1.01x faster                                                 |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 414 ms: 1.35x faster                                         |
| async_tree_none_tg         | 446 ms                                                 | 336 ms: 1.33x faster                                         |
| async_tree_none            | 464 ms                                                 | 354 ms: 1.31x faster                                         |
| async_tree_io              | 1.08 sec                                               | 876 ms: 1.24x faster                                         |
| async_tree_io_tg           | 1.11 sec                                               | 913 ms: 1.21x faster                                         |
| async_tree_memoization     | 555 ms                                                 | 461 ms: 1.20x faster                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 638 ms: 1.13x faster                                         |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 666 ms: 1.07x faster                                         |
| asyncio_tcp                | 519 ms                                                 | 505 ms: 1.03x faster                                         |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                         |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                        |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                         |
| Geometric mean             | (ref)                                                  | 1.14x faster                                                 |

Benchmark hidden because not significant (1): asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 85.1 ms: 1.05x faster                                        |
| float          | 80.8 ms                                                | 77.5 ms: 1.04x faster                                        |
| pidigits       | 184 ms                                                 | 217 ms: 1.18x slower                                         |
| Geometric mean | (ref)                                                  | 1.02x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 132 ms: 1.08x faster                                         |
| regex_effbot   | 3.17 ms                                                | 3.08 ms: 1.03x faster                                        |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                         |
| regex_v8       | 20.6 ms                                                | 22.7 ms: 1.10x slower                                        |
| Geometric mean | (ref)                                                  | 1.02x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 2.01 sec: 1.05x faster                                       |
| unpickle_pure_python | 221 us                                                 | 210 us: 1.05x faster                                         |
| pickle_pure_python   | 308 us                                                 | 294 us: 1.04x faster                                         |
| xml_etree_iterparse  | 96.7 ms                                                | 94.9 ms: 1.02x faster                                        |
| xml_etree_parse      | 139 ms                                                 | 136 ms: 1.02x faster                                         |
| xml_etree_generate   | 85.2 ms                                                | 85.4 ms: 1.00x slower                                        |
| xml_etree_process    | 59.0 ms                                                | 59.3 ms: 1.01x slower                                        |
| unpickle_list        | 4.67 us                                                | 4.71 us: 1.01x slower                                        |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.02x slower                                        |
| json_loads           | 26.5 us                                                | 27.0 us: 1.02x slower                                        |
| pickle_dict          | 31.8 us                                                | 32.5 us: 1.02x slower                                        |
| pickle_list          | 4.77 us                                                | 4.93 us: 1.03x slower                                        |
| pickle               | 10.9 us                                                | 11.3 us: 1.04x slower                                        |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                 |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.39 ms: 1.03x slower                                        |
| python_startup         | 9.93 ms                                                | 11.0 ms: 1.11x slower                                        |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                        |
| genshi_xml      | 50.2 ms                                                | 48.8 ms: 1.03x faster                                        |
| django_template | 34.7 ms                                                | 34.1 ms: 1.02x faster                                        |
| mako            | 11.0 ms                                                | 11.3 ms: 1.03x slower                                        |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 414 ms: 1.35x faster                                         |
| async_tree_none_tg         | 446 ms                                                 | 336 ms: 1.33x faster                                         |
| async_tree_none            | 464 ms                                                 | 354 ms: 1.31x faster                                         |
| async_tree_io              | 1.08 sec                                               | 876 ms: 1.24x faster                                         |
| async_tree_io_tg           | 1.11 sec                                               | 913 ms: 1.21x faster                                         |
| comprehensions             | 19.8 us                                                | 16.5 us: 1.21x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 461 ms: 1.20x faster                                         |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                         |
| unpack_sequence            | 52.1 ns                                                | 44.8 ns: 1.16x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 638 ms: 1.13x faster                                         |
| crypto_pyaes               | 76.6 ms                                                | 67.9 ms: 1.13x faster                                        |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                        |
| generators                 | 32.2 ms                                                | 28.8 ms: 1.12x faster                                        |
| deltablue                  | 3.45 ms                                                | 3.12 ms: 1.10x faster                                        |
| gc_traversal               | 3.46 ms                                                | 3.14 ms: 1.10x faster                                        |
| chaos                      | 62.8 ms                                                | 57.3 ms: 1.10x faster                                        |
| sqlglot_parse              | 1.36 ms                                                | 1.25 ms: 1.09x faster                                        |
| regex_compile              | 142 ms                                                 | 132 ms: 1.08x faster                                         |
| logging_simple             | 6.63 us                                                | 6.16 us: 1.08x faster                                        |
| logging_format             | 7.35 us                                                | 6.84 us: 1.07x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 666 ms: 1.07x faster                                         |
| sqlglot_transpile          | 1.67 ms                                                | 1.56 ms: 1.07x faster                                        |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.07x faster                                         |
| bpe_tokeniser              | 4.74 sec                                               | 4.45 sec: 1.07x faster                                       |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                         |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                         |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                        |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.06x faster                                         |
| dulwich_log                | 78.9 ms                                                | 74.8 ms: 1.05x faster                                        |
| tomli_loads                | 2.11 sec                                               | 2.01 sec: 1.05x faster                                       |
| unpickle_pure_python       | 221 us                                                 | 210 us: 1.05x faster                                         |
| nbody                      | 89.3 ms                                                | 85.1 ms: 1.05x faster                                        |
| scimark_monte_carlo        | 68.4 ms                                                | 65.4 ms: 1.05x faster                                        |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                       |
| tornado_http               | 119 ms                                                 | 114 ms: 1.04x faster                                         |
| pickle_pure_python         | 308 us                                                 | 294 us: 1.04x faster                                         |
| float                      | 80.8 ms                                                | 77.5 ms: 1.04x faster                                        |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                        |
| dask                       | 413 ms                                                 | 400 ms: 1.03x faster                                         |
| deepcopy_memo              | 40.3 us                                                | 39.1 us: 1.03x faster                                        |
| hexiom                     | 6.17 ms                                                | 5.99 ms: 1.03x faster                                        |
| genshi_xml                 | 50.2 ms                                                | 48.8 ms: 1.03x faster                                        |
| mdp                        | 2.42 sec                                               | 2.36 sec: 1.03x faster                                       |
| regex_effbot               | 3.17 ms                                                | 3.08 ms: 1.03x faster                                        |
| asyncio_tcp                | 519 ms                                                 | 505 ms: 1.03x faster                                         |
| bench_thread_pool          | 941 us                                                 | 919 us: 1.02x faster                                         |
| sympy_expand               | 468 ms                                                 | 457 ms: 1.02x faster                                         |
| json                       | 5.02 ms                                                | 4.93 ms: 1.02x faster                                        |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                         |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.02x faster                                         |
| xml_etree_iterparse        | 96.7 ms                                                | 94.9 ms: 1.02x faster                                        |
| nqueens                    | 80.1 ms                                                | 78.6 ms: 1.02x faster                                        |
| xml_etree_parse            | 139 ms                                                 | 136 ms: 1.02x faster                                         |
| thrift                     | 791 us                                                 | 778 us: 1.02x faster                                         |
| django_template            | 34.7 ms                                                | 34.1 ms: 1.02x faster                                        |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                        |
| richards                   | 45.9 ms                                                | 45.2 ms: 1.02x faster                                        |
| pprint_pformat             | 1.52 sec                                               | 1.50 sec: 1.02x faster                                       |
| 2to3                       | 264 ms                                                 | 260 ms: 1.01x faster                                         |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                         |
| sqlglot_optimize           | 53.3 ms                                                | 52.7 ms: 1.01x faster                                        |
| docutils                   | 2.64 sec                                               | 2.62 sec: 1.01x faster                                       |
| sqlglot_normalize          | 107 ms                                                 | 106 ms: 1.01x faster                                         |
| pprint_safe_repr           | 743 ms                                                 | 738 ms: 1.01x faster                                         |
| fannkuch                   | 372 ms                                                 | 370 ms: 1.01x faster                                         |
| xml_etree_generate         | 85.2 ms                                                | 85.4 ms: 1.00x slower                                        |
| xml_etree_process          | 59.0 ms                                                | 59.3 ms: 1.01x slower                                        |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                         |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                         |
| unpickle_list              | 4.67 us                                                | 4.71 us: 1.01x slower                                        |
| deepcopy                   | 352 us                                                 | 355 us: 1.01x slower                                         |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                         |
| deepcopy_reduce            | 3.08 us                                                | 3.11 us: 1.01x slower                                        |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.02x slower                                        |
| json_loads                 | 26.5 us                                                | 27.0 us: 1.02x slower                                        |
| bench_mp_pool              | 10.8 ms                                                | 11.0 ms: 1.02x slower                                        |
| aiohttp                    | 1.04 ms                                                | 1.07 ms: 1.02x slower                                        |
| scimark_fft                | 342 ms                                                 | 349 ms: 1.02x slower                                         |
| pickle_dict                | 31.8 us                                                | 32.5 us: 1.02x slower                                        |
| gunicorn                   | 1.08 ms                                                | 1.11 ms: 1.02x slower                                        |
| mako                       | 11.0 ms                                                | 11.3 ms: 1.03x slower                                        |
| python_startup_no_site     | 7.16 ms                                                | 7.39 ms: 1.03x slower                                        |
| pickle_list                | 4.77 us                                                | 4.93 us: 1.03x slower                                        |
| pickle                     | 10.9 us                                                | 11.3 us: 1.04x slower                                        |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.04x slower                                         |
| html5lib                   | 63.6 ms                                                | 67.0 ms: 1.05x slower                                        |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.71 ms: 1.07x slower                                        |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                         |
| regex_v8                   | 20.6 ms                                                | 22.7 ms: 1.10x slower                                        |
| python_startup             | 9.93 ms                                                | 11.0 ms: 1.11x slower                                        |
| coverage                   | 71.4 ms                                                | 83.0 ms: 1.16x slower                                        |
| pidigits                   | 184 ms                                                 | 217 ms: 1.18x slower                                         |
| flaskblogging              | 3.03 ms                                                | 3.58 ms: 1.18x slower                                        |
| telco                      | 6.53 ms                                                | 7.82 ms: 1.20x slower                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                        |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                 |

Benchmark hidden because not significant (7): chameleon, richards_super, pylint, pyflate, asyncio_tcp_ssl, sqlite_synth, unpickle
Ignored benchmarks (3) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x