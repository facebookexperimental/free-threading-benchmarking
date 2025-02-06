# Results vs. 3.12.6

- fork: python
- ref: cdcacec79f7a216c3c98
- machine: linux-x86_64
- commit hash: cdcacec
- commit date: 2025-02-05
- overall geometric mean: 1.034x slower
- HPT reliability: 99.92%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 554 ms: 1.21x slower                                                   |
| html5lib       | 88.9 ms                                                | 93.9 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 825 ms: 2.34x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 854 ms: 2.16x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 343 ms: 2.05x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 457 ms: 2.03x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 514 ms: 1.90x faster                                                   |
| async_tree_none            | 741 ms                                                 | 428 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 654 ms: 1.68x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 730 ms: 1.48x faster                                                   |
| async_generators           | 589 ms                                                 | 564 ms: 1.04x faster                                                   |
| coroutines                 | 29.5 ms                                                | 32.3 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.59x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 107 ms: 1.15x faster                                                   |
| nbody          | 119 ms                                                 | 202 ms: 1.69x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 187 ms                                                 | 197 ms: 1.06x slower                                                   |
| regex_v8       | 32.5 ms                                                | 34.4 ms: 1.06x slower                                                  |
| regex_dna      | 278 ms                                                 | 312 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 144 ms: 1.17x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 213 ms: 1.13x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.99 sec: 1.04x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 327 us: 1.09x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 491 us: 1.13x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 98.1 ms: 1.17x slower                                                  |
| json_loads           | 37.9 us                                                | 45.6 us: 1.20x slower                                                  |
| json_dumps           | 14.3 ms                                                | 17.7 ms: 1.23x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.0 ms: 1.14x slower                                                  |
| python_startup         | 23.7 ms                                                | 32.4 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 52.7 ms: 1.17x slower                                                  |
| genshi_text     | 30.2 ms                                                | 36.8 ms: 1.22x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 82.6 ms: 1.22x slower                                                  |
| mako            | 15.7 ms                                                | 25.2 ms: 1.60x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 825 ms: 2.34x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 854 ms: 2.16x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 343 ms: 2.05x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 457 ms: 2.03x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 514 ms: 1.90x faster                                                   |
| async_tree_none            | 741 ms                                                 | 428 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 654 ms: 1.68x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.76 ms: 1.56x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 730 ms: 1.48x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 144 ms: 1.17x faster                                                   |
| float                      | 123 ms                                                 | 107 ms: 1.15x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 213 ms: 1.13x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.60 sec: 1.12x faster                                                 |
| deepcopy_memo              | 52.4 us                                                | 47.8 us: 1.10x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.59 us: 1.08x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 203 ms: 1.07x faster                                                   |
| deepcopy                   | 468 us                                                 | 439 us: 1.07x faster                                                   |
| spectral_norm              | 156 ms                                                 | 148 ms: 1.05x faster                                                   |
| async_generators           | 589 ms                                                 | 564 ms: 1.04x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.99 sec: 1.04x slower                                                 |
| html5lib                   | 88.9 ms                                                | 93.9 ms: 1.06x slower                                                  |
| regex_compile              | 187 ms                                                 | 197 ms: 1.06x slower                                                   |
| regex_v8                   | 32.5 ms                                                | 34.4 ms: 1.06x slower                                                  |
| mdp                        | 3.97 sec                                               | 4.23 sec: 1.06x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 238 ms: 1.07x slower                                                   |
| scimark_fft                | 500 ms                                                 | 543 ms: 1.09x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 327 us: 1.09x slower                                                   |
| coroutines                 | 29.5 ms                                                | 32.3 ms: 1.09x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.27 sec: 1.10x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 32.9 ms: 1.11x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 84.4 ms: 1.11x slower                                                  |
| generators                 | 41.1 ms                                                | 45.9 ms: 1.11x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.21 sec: 1.12x slower                                                 |
| regex_dna                  | 278 ms                                                 | 312 ms: 1.12x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 121 ms: 1.12x slower                                                   |
| go                         | 172 ms                                                 | 194 ms: 1.12x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 491 us: 1.13x slower                                                   |
| logging_simple             | 9.45 us                                                | 10.7 us: 1.14x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 20.0 ms: 1.14x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.67 ms: 1.14x slower                                                  |
| json                       | 6.85 ms                                                | 7.83 ms: 1.14x slower                                                  |
| richards_super             | 72.8 ms                                                | 83.6 ms: 1.15x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.11 sec: 1.15x slower                                                 |
| sympy_str                  | 385 ms                                                 | 445 ms: 1.16x slower                                                   |
| logging_format             | 9.59 us                                                | 11.1 us: 1.16x slower                                                  |
| raytrace                   | 408 ms                                                 | 474 ms: 1.16x slower                                                   |
| fannkuch                   | 540 ms                                                 | 632 ms: 1.17x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 98.1 ms: 1.17x slower                                                  |
| django_template            | 44.9 ms                                                | 52.7 ms: 1.17x slower                                                  |
| scimark_sor                | 167 ms                                                 | 196 ms: 1.17x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.26 ms: 1.19x slower                                                  |
| nqueens                    | 117 ms                                                 | 140 ms: 1.20x slower                                                   |
| richards                   | 60.3 ms                                                | 72.7 ms: 1.20x slower                                                  |
| json_loads                 | 37.9 us                                                | 45.6 us: 1.20x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 116 ms: 1.21x slower                                                   |
| 2to3                       | 456 ms                                                 | 554 ms: 1.21x slower                                                   |
| genshi_text                | 30.2 ms                                                | 36.8 ms: 1.22x slower                                                  |
| telco                      | 9.59 ms                                                | 11.7 ms: 1.22x slower                                                  |
| meteor_contest             | 146 ms                                                 | 178 ms: 1.22x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 82.6 ms: 1.22x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 187 ms: 1.23x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 17.7 ms: 1.23x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.32 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.33 ms: 1.24x slower                                                  |
| sympy_expand               | 582 ms                                                 | 730 ms: 1.26x slower                                                   |
| hexiom                     | 8.27 ms                                                | 10.8 ms: 1.30x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.33 ms: 1.30x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 32.2 ms: 1.30x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 296 us: 1.32x slower                                                   |
| python_startup             | 23.7 ms                                                | 32.4 ms: 1.37x slower                                                  |
| chaos                      | 84.9 ms                                                | 120 ms: 1.42x slower                                                   |
| coverage                   | 95.4 ms                                                | 139 ms: 1.46x slower                                                   |
| deltablue                  | 4.27 ms                                                | 6.28 ms: 1.47x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.97 ms: 1.53x slower                                                  |
| mako                       | 15.7 ms                                                | 25.2 ms: 1.60x slower                                                  |
| nbody                      | 119 ms                                                 | 202 ms: 1.69x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 87.5 ms: 4.23x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (13): dulwich_log, pidigits, pathlib, pylint, docutils, sqlglot_normalize, comprehensions, deepcopy_reduce, asyncio_websockets, xml_etree_generate, logging_silent, regex_effbot, pyflate
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.034x slower

# HPT report

- Reliability score: 99.92% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.35x