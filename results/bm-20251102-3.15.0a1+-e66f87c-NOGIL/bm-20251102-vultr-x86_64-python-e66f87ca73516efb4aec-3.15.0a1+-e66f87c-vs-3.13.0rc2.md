# Results vs. 3.13.0rc2

- fork: python
- ref: e66f87ca73516efb4aec
- machine: linux-x86_64
- commit hash: e66f87c
- commit date: 2025-11-02
- overall geometric mean: 1.052x slower
- HPT reliability: 96.28%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 281 ms: 1.08x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 521 ms: 1.75x faster                                                   |
| async_tree_io              | 876 ms                                                       | 543 ms: 1.61x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 227 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 283 ms: 1.46x faster                                                   |
| async_tree_none            | 354 ms                                                       | 255 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 196 ms: 1.11x faster                                                   |
| float          | 77.5 ms                                                      | 70.1 ms: 1.10x faster                                                  |
| nbody          | 85.1 ms                                                      | 125 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.1 ms: 1.08x faster                                                  |
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                                  |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.6 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.02x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.02 sec: 1.00x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 235 us: 1.12x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 338 us: 1.15x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 68.7 ms: 1.16x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.7 us: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.58 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.2 ms: 1.18x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 58.1 ms: 1.19x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 26.2 ms: 1.22x slower                                                  |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.32 sec: 1.78x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 521 ms: 1.75x faster                                                   |
| gc_traversal               | 3.14 ms                                                      | 1.92 ms: 1.64x faster                                                  |
| async_tree_io              | 876 ms                                                       | 543 ms: 1.61x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 227 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 283 ms: 1.46x faster                                                   |
| async_tree_none            | 354 ms                                                       | 255 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                   |
| deepcopy                   | 355 us                                                       | 277 us: 1.28x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.9 us: 1.26x faster                                                  |
| go                         | 141 ms                                                       | 122 ms: 1.16x faster                                                   |
| pidigits                   | 217 ms                                                       | 196 ms: 1.11x faster                                                   |
| float                      | 77.5 ms                                                      | 70.1 ms: 1.10x faster                                                  |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.09x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.6 ms: 1.08x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.1 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.07x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.01 us: 1.04x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 72.6 ms: 1.03x faster                                                  |
| scimark_fft                | 349 ms                                                       | 342 ms: 1.02x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 133 ms: 1.02x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.42 sec: 1.01x faster                                                 |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.02 sec: 1.00x slower                                                 |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                  |
| logging_silent             | 103 ns                                                       | 106 ns: 1.03x slower                                                   |
| pyflate                    | 449 ms                                                       | 466 ms: 1.04x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 775 ms: 1.05x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.06x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.40 ms: 1.07x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.60 sec: 1.07x slower                                                 |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                   |
| 2to3                       | 260 ms                                                       | 281 ms: 1.08x slower                                                   |
| json                       | 4.93 ms                                                      | 5.35 ms: 1.08x slower                                                  |
| generators                 | 28.8 ms                                                      | 31.3 ms: 1.09x slower                                                  |
| comprehensions             | 16.5 us                                                      | 18.0 us: 1.09x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 21.8 ms: 1.10x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 87.1 ms: 1.11x slower                                                  |
| chaos                      | 57.3 ms                                                      | 63.6 ms: 1.11x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.84 us: 1.11x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.49 ms: 1.11x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 235 us: 1.12x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                  |
| sympy_str                  | 275 ms                                                       | 309 ms: 1.13x slower                                                   |
| sympy_expand               | 457 ms                                                       | 516 ms: 1.13x slower                                                   |
| logging_format             | 6.84 us                                                      | 7.79 us: 1.14x slower                                                  |
| richards                   | 45.2 ms                                                      | 51.7 ms: 1.14x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.40 ms: 1.15x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 338 us: 1.15x slower                                                   |
| thrift                     | 778 us                                                       | 894 us: 1.15x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 179 ms: 1.15x slower                                                   |
| richards_super             | 51.6 ms                                                      | 59.5 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 68.7 ms: 1.16x slower                                                  |
| meteor_contest             | 102 ms                                                       | 118 ms: 1.16x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 131 ms: 1.16x slower                                                   |
| json_loads                 | 27.0 us                                                      | 31.7 us: 1.17x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.67 ms: 1.18x slower                                                  |
| django_template            | 34.1 ms                                                      | 40.2 ms: 1.18x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 58.1 ms: 1.19x slower                                                  |
| raytrace                   | 253 ms                                                       | 301 ms: 1.19x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 186 us: 1.20x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 26.2 ms: 1.22x slower                                                  |
| fannkuch                   | 370 ms                                                       | 453 ms: 1.23x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 80.1 ms: 1.23x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 86.6 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.58 ms: 1.30x slower                                                  |
| coverage                   | 83.0 ms                                                      | 110 ms: 1.33x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 15.1 ms: 1.37x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                  |
| nbody                      | 85.1 ms                                                      | 125 ms: 1.47x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.05 ms: 3.32x slower                                                  |
| telco                      | 7.82 ms                                                      | 176 ms: 22.44x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (3): pylint, async_generators, html5lib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.052x slower

# HPT report

- Reliability score: 96.28% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x