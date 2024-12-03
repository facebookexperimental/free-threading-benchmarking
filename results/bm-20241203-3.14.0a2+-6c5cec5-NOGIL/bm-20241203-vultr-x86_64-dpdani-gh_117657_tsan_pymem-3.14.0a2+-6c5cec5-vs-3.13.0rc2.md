# Results vs. 3.13.0rc2

- fork: dpdani
- ref: gh_117657_tsan_pymem
- machine: linux-x86_64
- commit hash: 6c5cec5
- commit date: 2024-12-03
- overall geometric mean: 1.278x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 376 ms: 1.45x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.20 sec: 1.22x slower                                                 |
| html5lib       | 67.0 ms                                                      | 99.2 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                        | 1.38x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 861 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 621 ms: 1.03x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 653 ms: 1.02x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 488 ms: 1.06x slower                                                   |
| async_tree_none_tg         | 336 ms                                                       | 364 ms: 1.08x slower                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 460 ms: 1.11x slower                                                   |
| async_tree_none            | 354 ms                                                       | 397 ms: 1.12x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 28.1 ms: 1.19x slower                                                  |
| async_generators           | 377 ms                                                       | 465 ms: 1.23x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                   |
| float          | 77.5 ms                                                      | 143 ms: 1.84x slower                                                   |
| Geometric mean | (ref)                                                        | 1.33x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 26.0 ms: 1.15x slower                                                  |
| regex_compile  | 132 ms                                                       | 191 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                        | 1.12x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 94.4 ms: 1.01x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.19x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.74 sec: 1.37x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.5 ms: 1.37x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 81.9 ms: 1.38x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 379 us: 1.80x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 556 us: 1.89x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.30x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 66.0 ms: 1.35x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 33.2 ms: 1.54x slower                                                  |
| django_template | 34.1 ms                                                      | 55.4 ms: 1.62x slower                                                  |
| mako            | 11.3 ms                                                      | 19.6 ms: 1.73x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.56x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 861 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 621 ms: 1.03x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 653 ms: 1.02x faster                                                   |
| deepcopy                   | 355 us                                                       | 351 us: 1.01x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 94.4 ms: 1.01x faster                                                  |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.33 us: 1.06x slower                                                  |
| async_tree_memoization     | 461 ms                                                       | 488 ms: 1.06x slower                                                   |
| pathlib                    | 19.2 ms                                                      | 20.6 ms: 1.07x slower                                                  |
| async_tree_none_tg         | 336 ms                                                       | 364 ms: 1.08x slower                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 460 ms: 1.11x slower                                                   |
| async_tree_none            | 354 ms                                                       | 397 ms: 1.12x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 3.53 ms: 1.12x slower                                                  |
| deepcopy_memo              | 39.1 us                                                      | 44.2 us: 1.13x slower                                                  |
| scimark_fft                | 349 ms                                                       | 398 ms: 1.14x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 26.0 ms: 1.15x slower                                                  |
| telco                      | 7.82 ms                                                      | 9.03 ms: 1.15x slower                                                  |
| spectral_norm              | 111 ms                                                       | 129 ms: 1.16x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.19x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 28.1 ms: 1.19x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.72 us: 1.20x slower                                                  |
| coverage                   | 83.0 ms                                                      | 100 ms: 1.21x slower                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 5.40 sec: 1.22x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.73 ms: 1.22x slower                                                  |
| docutils                   | 2.62 sec                                                     | 3.20 sec: 1.22x slower                                                 |
| async_generators           | 377 ms                                                       | 465 ms: 1.23x slower                                                   |
| pylint                     | 317 ms                                                       | 394 ms: 1.24x slower                                                   |
| mdp                        | 2.36 sec                                                     | 3.02 sec: 1.28x slower                                                 |
| meteor_contest             | 102 ms                                                       | 133 ms: 1.31x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 98.5 ms: 1.32x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 104 ms: 1.32x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 208 us: 1.35x slower                                                   |
| generators                 | 28.8 ms                                                      | 38.9 ms: 1.35x slower                                                  |
| fannkuch                   | 370 ms                                                       | 500 ms: 1.35x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 66.0 ms: 1.35x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.74 sec: 1.37x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 92.8 ms: 1.37x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 14.5 ms: 1.37x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 81.9 ms: 1.38x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.87 ms: 1.39x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 149 ms: 1.41x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 74.4 ms: 1.41x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 1.05 sec: 1.43x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.60 sec: 1.43x slower                                                 |
| regex_compile              | 132 ms                                                       | 191 ms: 1.44x slower                                                   |
| 2to3                       | 260 ms                                                       | 376 ms: 1.45x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 2.19 sec: 1.46x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 99.2 ms: 1.48x slower                                                  |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                   |
| thrift                     | 778 us                                                       | 1.20 ms: 1.54x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 33.2 ms: 1.54x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 30.7 ms: 1.55x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                  |
| django_template            | 34.1 ms                                                      | 55.4 ms: 1.62x slower                                                  |
| pyflate                    | 449 ms                                                       | 731 ms: 1.63x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 193 ms: 1.71x slower                                                   |
| mako                       | 11.3 ms                                                      | 19.6 ms: 1.73x slower                                                  |
| logging_format             | 6.84 us                                                      | 12.1 us: 1.76x slower                                                  |
| comprehensions             | 16.5 us                                                      | 29.1 us: 1.77x slower                                                  |
| logging_simple             | 6.16 us                                                      | 10.9 us: 1.77x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 10.7 ms: 1.78x slower                                                  |
| sympy_str                  | 275 ms                                                       | 493 ms: 1.80x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 379 us: 1.80x slower                                                   |
| scimark_sor                | 134 ms                                                       | 243 ms: 1.80x slower                                                   |
| richards                   | 45.2 ms                                                      | 82.7 ms: 1.83x slower                                                  |
| float                      | 77.5 ms                                                      | 143 ms: 1.84x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 123 ms: 1.88x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 556 us: 1.89x slower                                                   |
| richards_super             | 51.6 ms                                                      | 99.1 ms: 1.92x slower                                                  |
| chaos                      | 57.3 ms                                                      | 112 ms: 1.95x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 3.06 ms: 1.96x slower                                                  |
| logging_silent             | 103 ns                                                       | 202 ns: 1.97x slower                                                   |
| go                         | 141 ms                                                       | 281 ms: 2.00x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 2.65 ms: 2.12x slower                                                  |
| sympy_expand               | 457 ms                                                       | 984 ms: 2.15x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 357 ms: 2.30x slower                                                   |
| raytrace                   | 253 ms                                                       | 602 ms: 2.38x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 8.84 ms: 2.83x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.38 ms: 3.67x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 110 ms: 9.99x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.44x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_io
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241203-3.14.0a2+-6c5cec5-NOGIL/bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.278x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.32x