# Results vs. base

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.32x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                                                                  | 403 ms: 1.55x slower                                                                                          |
| chameleon      | 6.79 ms                                                                                                 | 12.2 ms: 1.79x slower                                                                                         |
| docutils       | 2.62 sec                                                                                                | 3.30 sec: 1.26x slower                                                                                        |
| html5lib       | 67.0 ms                                                                                                 | 105 ms: 1.57x slower                                                                                          |
| tornado_http   | 114 ms                                                                                                  | 157 ms: 1.38x slower                                                                                          |
| Geometric mean | (ref)                                                                                                   | 1.50x slower                                                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 638 ms                                                                                                  | 665 ms: 1.04x slower                                                                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                                                                  | 704 ms: 1.06x slower                                                                                          |
| async_tree_io              | 876 ms                                                                                                  | 952 ms: 1.09x slower                                                                                          |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                | 1.70 sec: 1.12x slower                                                                                        |
| asyncio_tcp                | 505 ms                                                                                                  | 574 ms: 1.14x slower                                                                                          |
| async_tree_memoization     | 461 ms                                                                                                  | 539 ms: 1.17x slower                                                                                          |
| async_tree_none_tg         | 336 ms                                                                                                  | 406 ms: 1.21x slower                                                                                          |
| async_tree_memoization_tg  | 414 ms                                                                                                  | 501 ms: 1.21x slower                                                                                          |
| async_tree_none            | 354 ms                                                                                                  | 447 ms: 1.26x slower                                                                                          |
| async_generators           | 377 ms                                                                                                  | 484 ms: 1.28x slower                                                                                          |
| coroutines                 | 23.6 ms                                                                                                 | 31.9 ms: 1.35x slower                                                                                         |
| Geometric mean             | (ref)                                                                                                   | 1.14x slower                                                                                                  |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                                                  | 186 ms: 1.17x faster                                                                                          |
| float          | 77.5 ms                                                                                                 | 152 ms: 1.96x slower                                                                                          |
| nbody          | 85.1 ms                                                                                                 | 218 ms: 2.56x slower                                                                                          |
| Geometric mean | (ref)                                                                                                   | 1.63x slower                                                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                                                                 | 3.04 ms: 1.01x faster                                                                                         |
| regex_dna      | 180 ms                                                                                                  | 184 ms: 1.02x slower                                                                                          |
| regex_v8       | 22.7 ms                                                                                                 | 24.1 ms: 1.06x slower                                                                                         |
| regex_compile  | 132 ms                                                                                                  | 226 ms: 1.71x slower                                                                                          |
| Geometric mean | (ref)                                                                                                   | 1.16x slower                                                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| pickle               | 11.3 us                                                                                                 | 10.6 us: 1.07x faster                                                                                         |
| pickle_list          | 4.93 us                                                                                                 | 4.72 us: 1.04x faster                                                                                         |
| xml_etree_parse      | 136 ms                                                                                                  | 131 ms: 1.04x faster                                                                                          |
| pickle_dict          | 32.5 us                                                                                                 | 32.2 us: 1.01x faster                                                                                         |
| unpickle             | 14.3 us                                                                                                 | 15.4 us: 1.08x slower                                                                                         |
| unpickle_list        | 4.71 us                                                                                                 | 5.26 us: 1.12x slower                                                                                         |
| xml_etree_iterparse  | 94.9 ms                                                                                                 | 106 ms: 1.12x slower                                                                                          |
| json_loads           | 27.0 us                                                                                                 | 30.2 us: 1.12x slower                                                                                         |
| json_dumps           | 10.5 ms                                                                                                 | 13.6 ms: 1.29x slower                                                                                         |
| xml_etree_generate   | 85.4 ms                                                                                                 | 111 ms: 1.30x slower                                                                                          |
| xml_etree_process    | 59.3 ms                                                                                                 | 92.0 ms: 1.55x slower                                                                                         |
| tomli_loads          | 2.01 sec                                                                                                | 3.24 sec: 1.62x slower                                                                                        |
| unpickle_pure_python | 210 us                                                                                                  | 407 us: 1.94x slower                                                                                          |
| pickle_pure_python   | 294 us                                                                                                  | 585 us: 1.99x slower                                                                                          |
| Geometric mean       | (ref)                                                                                                   | 1.24x slower                                                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|------------------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                                                                 | 9.64 ms: 1.30x slower                                                                                         |
| python_startup         | 11.0 ms                                                                                                 | 14.8 ms: 1.35x slower                                                                                         |
| Geometric mean         | (ref)                                                                                                   | 1.33x slower                                                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|-----------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                                                                 | 79.2 ms: 1.62x slower                                                                                         |
| mako            | 11.3 ms                                                                                                 | 19.7 ms: 1.73x slower                                                                                         |
| genshi_text     | 21.5 ms                                                                                                 | 39.3 ms: 1.83x slower                                                                                         |
| django_template | 34.1 ms                                                                                                 | 63.0 ms: 1.85x slower                                                                                         |
| Geometric mean  | (ref)                                                                                                   | 1.76x slower                                                                                                  |

All benchmarks:
===============

| Benchmark                  | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                                                                 | 2.54 ms: 1.24x faster                                                                                         |
| create_gc_cycles           | 1.34 ms                                                                                                 | 1.10 ms: 1.22x faster                                                                                         |
| pidigits                   | 217 ms                                                                                                  | 186 ms: 1.17x faster                                                                                          |
| pickle                     | 11.3 us                                                                                                 | 10.6 us: 1.07x faster                                                                                         |
| pickle_list                | 4.93 us                                                                                                 | 4.72 us: 1.04x faster                                                                                         |
| xml_etree_parse            | 136 ms                                                                                                  | 131 ms: 1.04x faster                                                                                          |
| regex_effbot               | 3.08 ms                                                                                                 | 3.04 ms: 1.01x faster                                                                                         |
| pickle_dict                | 32.5 us                                                                                                 | 32.2 us: 1.01x faster                                                                                         |
| regex_dna                  | 180 ms                                                                                                  | 184 ms: 1.02x slower                                                                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                                                                  | 665 ms: 1.04x slower                                                                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                                                                  | 704 ms: 1.06x slower                                                                                          |
| regex_v8                   | 22.7 ms                                                                                                 | 24.1 ms: 1.06x slower                                                                                         |
| unpickle                   | 14.3 us                                                                                                 | 15.4 us: 1.08x slower                                                                                         |
| async_tree_io              | 876 ms                                                                                                  | 952 ms: 1.09x slower                                                                                          |
| sqlite_synth               | 2.21 us                                                                                                 | 2.43 us: 1.10x slower                                                                                         |
| bench_mp_pool              | 11.0 ms                                                                                                 | 12.2 ms: 1.11x slower                                                                                         |
| unpickle_list              | 4.71 us                                                                                                 | 5.26 us: 1.12x slower                                                                                         |
| xml_etree_iterparse        | 94.9 ms                                                                                                 | 106 ms: 1.12x slower                                                                                          |
| json_loads                 | 27.0 us                                                                                                 | 30.2 us: 1.12x slower                                                                                         |
| json                       | 4.93 ms                                                                                                 | 5.52 ms: 1.12x slower                                                                                         |
| asyncio_tcp_ssl            | 1.51 sec                                                                                                | 1.70 sec: 1.12x slower                                                                                        |
| asyncio_tcp                | 505 ms                                                                                                  | 574 ms: 1.14x slower                                                                                          |
| async_tree_memoization     | 461 ms                                                                                                  | 539 ms: 1.17x slower                                                                                          |
| telco                      | 7.82 ms                                                                                                 | 9.38 ms: 1.20x slower                                                                                         |
| async_tree_none_tg         | 336 ms                                                                                                  | 406 ms: 1.21x slower                                                                                          |
| async_tree_memoization_tg  | 414 ms                                                                                                  | 501 ms: 1.21x slower                                                                                          |
| pathlib                    | 19.2 ms                                                                                                 | 24.0 ms: 1.25x slower                                                                                         |
| docutils                   | 2.62 sec                                                                                                | 3.30 sec: 1.26x slower                                                                                        |
| async_tree_none            | 354 ms                                                                                                  | 447 ms: 1.26x slower                                                                                          |
| coverage                   | 83.0 ms                                                                                                 | 105 ms: 1.27x slower                                                                                          |
| scimark_sparse_mat_mult    | 4.71 ms                                                                                                 | 5.99 ms: 1.27x slower                                                                                         |
| async_generators           | 377 ms                                                                                                  | 484 ms: 1.28x slower                                                                                          |
| json_dumps                 | 10.5 ms                                                                                                 | 13.6 ms: 1.29x slower                                                                                         |
| xml_etree_generate         | 85.4 ms                                                                                                 | 111 ms: 1.30x slower                                                                                          |
| python_startup_no_site     | 7.39 ms                                                                                                 | 9.64 ms: 1.30x slower                                                                                         |
| gunicorn                   | 1.11 ms                                                                                                 | 1.45 ms: 1.31x slower                                                                                         |
| pylint                     | 317 ms                                                                                                  | 415 ms: 1.31x slower                                                                                          |
| mdp                        | 2.36 sec                                                                                                | 3.11 sec: 1.32x slower                                                                                        |
| aiohttp                    | 1.07 ms                                                                                                 | 1.41 ms: 1.32x slower                                                                                         |
| python_startup             | 11.0 ms                                                                                                 | 14.8 ms: 1.35x slower                                                                                         |
| coroutines                 | 23.6 ms                                                                                                 | 31.9 ms: 1.35x slower                                                                                         |
| scimark_fft                | 349 ms                                                                                                  | 476 ms: 1.36x slower                                                                                          |
| meteor_contest             | 102 ms                                                                                                  | 139 ms: 1.37x slower                                                                                          |
| dulwich_log                | 74.8 ms                                                                                                 | 103 ms: 1.38x slower                                                                                          |
| tornado_http               | 114 ms                                                                                                  | 157 ms: 1.38x slower                                                                                          |
| generators                 | 28.8 ms                                                                                                 | 40.7 ms: 1.41x slower                                                                                         |
| bpe_tokeniser              | 4.45 sec                                                                                                | 6.36 sec: 1.43x slower                                                                                        |
| nqueens                    | 78.6 ms                                                                                                 | 118 ms: 1.50x slower                                                                                          |
| pycparser                  | 1.12 sec                                                                                                | 1.68 sec: 1.50x slower                                                                                        |
| fannkuch                   | 370 ms                                                                                                  | 556 ms: 1.50x slower                                                                                          |
| xml_etree_process          | 59.3 ms                                                                                                 | 92.0 ms: 1.55x slower                                                                                         |
| 2to3                       | 260 ms                                                                                                  | 403 ms: 1.55x slower                                                                                          |
| html5lib                   | 67.0 ms                                                                                                 | 105 ms: 1.57x slower                                                                                          |
| crypto_pyaes               | 67.9 ms                                                                                                 | 107 ms: 1.58x slower                                                                                          |
| typing_runtime_protocols   | 155 us                                                                                                  | 246 us: 1.59x slower                                                                                          |
| sympy_integrate            | 19.8 ms                                                                                                 | 31.7 ms: 1.60x slower                                                                                         |
| spectral_norm              | 111 ms                                                                                                  | 179 ms: 1.61x slower                                                                                          |
| tomli_loads                | 2.01 sec                                                                                                | 3.24 sec: 1.62x slower                                                                                        |
| thrift                     | 778 us                                                                                                  | 1.26 ms: 1.62x slower                                                                                         |
| genshi_xml                 | 48.8 ms                                                                                                 | 79.2 ms: 1.62x slower                                                                                         |
| deepcopy                   | 355 us                                                                                                  | 579 us: 1.63x slower                                                                                          |
| sqlglot_normalize          | 106 ms                                                                                                  | 177 ms: 1.68x slower                                                                                          |
| deepcopy_reduce            | 3.11 us                                                                                                 | 5.22 us: 1.68x slower                                                                                         |
| deepcopy_memo              | 39.1 us                                                                                                 | 65.7 us: 1.68x slower                                                                                         |
| flaskblogging              | 3.58 ms                                                                                                 | 6.01 ms: 1.68x slower                                                                                         |
| sqlglot_optimize           | 52.7 ms                                                                                                 | 88.7 ms: 1.68x slower                                                                                         |
| pyflate                    | 449 ms                                                                                                  | 764 ms: 1.70x slower                                                                                          |
| regex_compile              | 132 ms                                                                                                  | 226 ms: 1.71x slower                                                                                          |
| mako                       | 11.3 ms                                                                                                 | 19.7 ms: 1.73x slower                                                                                         |
| pprint_safe_repr           | 738 ms                                                                                                  | 1.29 sec: 1.75x slower                                                                                        |
| comprehensions             | 16.5 us                                                                                                 | 29.3 us: 1.78x slower                                                                                         |
| pprint_pformat             | 1.50 sec                                                                                                | 2.67 sec: 1.79x slower                                                                                        |
| chameleon                  | 6.79 ms                                                                                                 | 12.2 ms: 1.79x slower                                                                                         |
| genshi_text                | 21.5 ms                                                                                                 | 39.3 ms: 1.83x slower                                                                                         |
| django_template            | 34.1 ms                                                                                                 | 63.0 ms: 1.85x slower                                                                                         |
| sympy_str                  | 275 ms                                                                                                  | 524 ms: 1.91x slower                                                                                          |
| scimark_monte_carlo        | 65.4 ms                                                                                                 | 126 ms: 1.92x slower                                                                                          |
| scimark_sor                | 134 ms                                                                                                  | 260 ms: 1.93x slower                                                                                          |
| unpickle_pure_python       | 210 us                                                                                                  | 407 us: 1.94x slower                                                                                          |
| logging_format             | 6.84 us                                                                                                 | 13.3 us: 1.95x slower                                                                                         |
| logging_simple             | 6.16 us                                                                                                 | 12.1 us: 1.96x slower                                                                                         |
| float                      | 77.5 ms                                                                                                 | 152 ms: 1.96x slower                                                                                          |
| pickle_pure_python         | 294 us                                                                                                  | 585 us: 1.99x slower                                                                                          |
| richards                   | 45.2 ms                                                                                                 | 90.0 ms: 1.99x slower                                                                                         |
| logging_silent             | 103 ns                                                                                                  | 207 ns: 2.02x slower                                                                                          |
| hexiom                     | 5.99 ms                                                                                                 | 12.2 ms: 2.04x slower                                                                                         |
| richards_super             | 51.6 ms                                                                                                 | 105 ms: 2.04x slower                                                                                          |
| sqlglot_transpile          | 1.56 ms                                                                                                 | 3.25 ms: 2.09x slower                                                                                         |
| scimark_lu                 | 113 ms                                                                                                  | 239 ms: 2.12x slower                                                                                          |
| chaos                      | 57.3 ms                                                                                                 | 126 ms: 2.20x slower                                                                                          |
| sqlglot_parse              | 1.25 ms                                                                                                 | 2.80 ms: 2.24x slower                                                                                         |
| sympy_expand               | 457 ms                                                                                                  | 1.03 sec: 2.26x slower                                                                                        |
| sympy_sum                  | 156 ms                                                                                                  | 372 ms: 2.39x slower                                                                                          |
| raytrace                   | 253 ms                                                                                                  | 622 ms: 2.46x slower                                                                                          |
| go                         | 141 ms                                                                                                  | 358 ms: 2.54x slower                                                                                          |
| nbody                      | 85.1 ms                                                                                                 | 218 ms: 2.56x slower                                                                                          |
| bench_thread_pool          | 919 us                                                                                                  | 2.74 ms: 2.98x slower                                                                                         |
| deltablue                  | 3.12 ms                                                                                                 | 9.99 ms: 3.20x slower                                                                                         |
| unpack_sequence            | 44.8 ns                                                                                                 | 146 ns: 3.27x slower                                                                                          |
| Geometric mean             | (ref)                                                                                                   | 1.49x slower                                                                                                  |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_io_tg
Ignored benchmarks (1) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: dask

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.36x
- 99% likely to have a slowdown of 1.32x

# Memory
- memory change: 1.16x