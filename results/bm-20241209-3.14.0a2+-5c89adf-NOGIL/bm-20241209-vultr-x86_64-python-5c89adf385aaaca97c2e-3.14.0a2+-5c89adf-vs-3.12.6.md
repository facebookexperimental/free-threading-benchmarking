# Results vs. 3.12.6

- fork: python
- ref: 5c89adf385aaaca97c2e
- machine: linux-x86_64
- commit hash: 5c89adf
- commit date: 2024-12-09
- overall geometric mean: 1.227x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 369 ms: 1.40x slower                                                   |
| docutils       | 2.64 sec                                               | 3.08 sec: 1.17x slower                                                 |
| html5lib       | 63.6 ms                                                | 97.0 ms: 1.52x slower                                                  |
| Geometric mean | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 829 ms: 1.34x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 853 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 449 ms: 1.25x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 359 ms: 1.24x faster                                                   |
| async_tree_none            | 464 ms                                                 | 388 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 614 ms: 1.18x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 475 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 642 ms: 1.11x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                  |
| async_generators           | 384 ms                                                 | 457 ms: 1.19x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| float          | 80.8 ms                                                | 140 ms: 1.73x slower                                                   |
| Geometric mean | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.3 ms: 1.18x slower                                                  |
| regex_compile  | 142 ms                                                 | 181 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 98.2 ms: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.66 sec: 1.26x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 78.7 ms: 1.33x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 336 us: 1.52x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 515 us: 1.67x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.8 ms: 1.27x slower                                                  |
| genshi_text     | 22.8 ms                                                | 31.7 ms: 1.39x slower                                                  |
| django_template | 34.7 ms                                                | 52.1 ms: 1.50x slower                                                  |
| mako            | 11.0 ms                                                | 17.8 ms: 1.61x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.44x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 829 ms: 1.34x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 853 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 449 ms: 1.25x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 359 ms: 1.24x faster                                                   |
| async_tree_none            | 464 ms                                                 | 388 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 614 ms: 1.18x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 475 ms: 1.17x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 642 ms: 1.11x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.27 ms: 1.06x faster                                                  |
| deepcopy                   | 352 us                                                 | 333 us: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.14 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.30 us: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 5.01 sec: 1.06x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| spectral_norm              | 110 ms                                                 | 125 ms: 1.14x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 98.2 ms: 1.15x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.80 sec: 1.16x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.56 us: 1.16x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.08 sec: 1.17x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.3 ms: 1.18x slower                                                  |
| async_generators           | 384 ms                                                 | 457 ms: 1.19x slower                                                   |
| scimark_fft                | 342 ms                                                 | 408 ms: 1.20x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 92.0 ms: 1.20x slower                                                  |
| pylint                     | 319 ms                                                 | 383 ms: 1.20x slower                                                   |
| generators                 | 32.2 ms                                                | 39.1 ms: 1.21x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 96.1 ms: 1.22x slower                                                  |
| nqueens                    | 80.1 ms                                                | 97.7 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.23x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.66 sec: 1.26x slower                                                 |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                                   |
| regex_compile              | 142 ms                                                 | 181 ms: 1.27x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 63.8 ms: 1.27x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 138 ms: 1.30x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 69.3 ms: 1.30x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 981 ms: 1.32x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.55 sec: 1.32x slower                                                 |
| telco                      | 6.53 ms                                                | 8.65 ms: 1.33x slower                                                  |
| fannkuch                   | 372 ms                                                 | 494 ms: 1.33x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.03 sec: 1.33x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 78.7 ms: 1.33x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.91 ms: 1.35x slower                                                  |
| comprehensions             | 19.8 us                                                | 27.2 us: 1.37x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                  |
| coverage                   | 71.4 ms                                                | 98.1 ms: 1.37x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 30.0 ms: 1.38x slower                                                  |
| genshi_text                | 22.8 ms                                                | 31.7 ms: 1.39x slower                                                  |
| 2to3                       | 264 ms                                                 | 369 ms: 1.40x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 205 ms: 1.43x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 29.6 ms: 1.44x slower                                                  |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| thrift                     | 791 us                                                 | 1.17 ms: 1.48x slower                                                  |
| django_template            | 34.7 ms                                                | 52.1 ms: 1.50x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 336 us: 1.52x slower                                                   |
| html5lib                   | 63.6 ms                                                | 97.0 ms: 1.52x slower                                                  |
| pyflate                    | 448 ms                                                 | 695 ms: 1.55x slower                                                   |
| hexiom                     | 6.17 ms                                                | 9.85 ms: 1.60x slower                                                  |
| mako                       | 11.0 ms                                                | 17.8 ms: 1.61x slower                                                  |
| logging_format             | 7.35 us                                                | 12.0 us: 1.63x slower                                                  |
| logging_simple             | 6.63 us                                                | 10.8 us: 1.63x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 186 ms: 1.63x slower                                                   |
| sympy_str                  | 292 ms                                                 | 476 ms: 1.63x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.79 ms: 1.64x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 515 us: 1.67x slower                                                   |
| chaos                      | 62.8 ms                                                | 107 ms: 1.70x slower                                                   |
| richards_super             | 51.9 ms                                                | 88.7 ms: 1.71x slower                                                  |
| richards                   | 45.9 ms                                                | 78.8 ms: 1.72x slower                                                  |
| logging_silent             | 109 ns                                                 | 188 ns: 1.72x slower                                                   |
| float                      | 80.8 ms                                                | 140 ms: 1.73x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 3.00 ms: 1.79x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 126 ms: 1.84x slower                                                   |
| scimark_sor                | 130 ms                                                 | 239 ms: 1.84x slower                                                   |
| raytrace                   | 299 ms                                                 | 565 ms: 1.89x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.59 ms: 1.91x slower                                                  |
| go                         | 139 ms                                                 | 278 ms: 2.00x slower                                                   |
| sympy_expand               | 468 ms                                                 | 957 ms: 2.05x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 350 ms: 2.11x slower                                                   |
| deltablue                  | 3.45 ms                                                | 8.28 ms: 2.40x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.43 ms: 3.65x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.09x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.34x slower                                                           |

Benchmark hidden because not significant (1): deepcopy_memo
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.227x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.33x