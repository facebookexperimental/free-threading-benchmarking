# Results vs. 3.12.6

- fork: python
- ref: 5c89adf385aaaca97c2e
- machine: linux-x86_64
- commit hash: 5c89adf
- commit date: 2024-12-09
- overall geometric mean: 1.164x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 616 ms: 1.35x slower                                                   |
| docutils       | 4.00 sec                                               | 4.37 sec: 1.09x slower                                                 |
| html5lib       | 88.9 ms                                                | 129 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                  | 1.29x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.05 sec: 1.84x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.08 sec: 1.71x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 609 ms: 1.53x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 464 ms: 1.52x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 657 ms: 1.49x faster                                                   |
| async_tree_none            | 741 ms                                                 | 530 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 823 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 842 ms: 1.28x faster                                                   |
| async_generators           | 589 ms                                                 | 654 ms: 1.11x slower                                                   |
| coroutines                 | 29.5 ms                                                | 33.6 ms: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 229 ms: 1.09x faster                                                   |
| float          | 123 ms                                                 | 169 ms: 1.37x slower                                                   |
| nbody          | 119 ms                                                 | 176 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.40 ms: 1.17x faster                                                  |
| regex_dna      | 278 ms                                                 | 296 ms: 1.06x slower                                                   |
| regex_compile  | 187 ms                                                 | 225 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 147 ms: 1.15x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 216 ms: 1.12x faster                                                   |
| xml_etree_process    | 83.7 ms                                                | 101 ms: 1.21x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.50 sec: 1.21x slower                                                 |
| json_dumps           | 14.3 ms                                                | 17.8 ms: 1.25x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 411 us: 1.37x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 626 us: 1.44x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                  |
| python_startup         | 23.7 ms                                                | 32.3 ms: 1.36x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 91.5 ms: 1.35x slower                                                  |
| genshi_text     | 30.2 ms                                                | 42.8 ms: 1.42x slower                                                  |
| django_template | 44.9 ms                                                | 63.7 ms: 1.42x slower                                                  |
| mako            | 15.7 ms                                                | 26.9 ms: 1.71x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.47x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.05 sec: 1.84x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.08 sec: 1.71x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 609 ms: 1.53x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 464 ms: 1.52x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 657 ms: 1.49x faster                                                   |
| async_tree_none            | 741 ms                                                 | 530 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 823 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 842 ms: 1.28x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.40 ms: 1.17x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 147 ms: 1.15x faster                                                   |
| deepcopy                   | 468 us                                                 | 417 us: 1.12x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 216 ms: 1.12x faster                                                   |
| pidigits                   | 250 ms                                                 | 229 ms: 1.09x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.67 us: 1.06x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 6.22 ms: 1.06x slower                                                  |
| regex_dna                  | 278 ms                                                 | 296 ms: 1.06x slower                                                   |
| pycparser                  | 1.79 sec                                               | 1.92 sec: 1.07x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.37 sec: 1.09x slower                                                 |
| async_generators           | 589 ms                                                 | 654 ms: 1.11x slower                                                   |
| sqlglot_normalize          | 157 ms                                                 | 177 ms: 1.13x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                  |
| pylint                     | 465 ms                                                 | 526 ms: 1.13x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.50 sec: 1.13x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 7.47 sec: 1.13x slower                                                 |
| spectral_norm              | 156 ms                                                 | 177 ms: 1.14x slower                                                   |
| coroutines                 | 29.5 ms                                                | 33.6 ms: 1.14x slower                                                  |
| scimark_fft                | 500 ms                                                 | 570 ms: 1.14x slower                                                   |
| comprehensions             | 27.1 us                                                | 31.0 us: 1.14x slower                                                  |
| nqueens                    | 117 ms                                                 | 134 ms: 1.15x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 125 ms: 1.16x slower                                                   |
| meteor_contest             | 146 ms                                                 | 171 ms: 1.17x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 4.73 us: 1.17x slower                                                  |
| dulwich_log                | 100 ms                                                 | 118 ms: 1.18x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 90.7 ms: 1.19x slower                                                  |
| telco                      | 9.59 ms                                                | 11.5 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.09 ms: 1.21x slower                                                  |
| regex_compile              | 187 ms                                                 | 225 ms: 1.21x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 101 ms: 1.21x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.50 sec: 1.21x slower                                                 |
| typing_runtime_protocols   | 224 us                                                 | 273 us: 1.22x slower                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 266 ms: 1.22x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 17.8 ms: 1.25x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.35 ms: 1.25x slower                                                  |
| generators                 | 41.1 ms                                                | 51.8 ms: 1.26x slower                                                  |
| fannkuch                   | 540 ms                                                 | 682 ms: 1.26x slower                                                   |
| pyflate                    | 727 ms                                                 | 929 ms: 1.28x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 39.0 ms: 1.31x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.29 sec: 1.34x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.67 sec: 1.35x slower                                                 |
| 2to3                       | 456 ms                                                 | 616 ms: 1.35x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 91.5 ms: 1.35x slower                                                  |
| python_startup             | 23.7 ms                                                | 32.3 ms: 1.36x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 411 us: 1.37x slower                                                   |
| float                      | 123 ms                                                 | 169 ms: 1.37x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.47 ms: 1.38x slower                                                  |
| logging_simple             | 9.45 us                                                | 13.1 us: 1.38x slower                                                  |
| richards_super             | 72.8 ms                                                | 103 ms: 1.41x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 215 ms: 1.42x slower                                                   |
| genshi_text                | 30.2 ms                                                | 42.8 ms: 1.42x slower                                                  |
| django_template            | 44.9 ms                                                | 63.7 ms: 1.42x slower                                                  |
| coverage                   | 95.4 ms                                                | 137 ms: 1.44x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 626 us: 1.44x slower                                                   |
| html5lib                   | 88.9 ms                                                | 129 ms: 1.45x slower                                                   |
| nbody                      | 119 ms                                                 | 176 ms: 1.47x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 142 ms: 1.48x slower                                                   |
| logging_format             | 9.59 us                                                | 14.3 us: 1.50x slower                                                  |
| richards                   | 60.3 ms                                                | 90.6 ms: 1.50x slower                                                  |
| sympy_str                  | 385 ms                                                 | 589 ms: 1.53x slower                                                   |
| chaos                      | 84.9 ms                                                | 130 ms: 1.54x slower                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 38.1 ms: 1.54x slower                                                  |
| raytrace                   | 408 ms                                                 | 634 ms: 1.55x slower                                                   |
| hexiom                     | 8.27 ms                                                | 13.9 ms: 1.68x slower                                                  |
| mako                       | 15.7 ms                                                | 26.9 ms: 1.71x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.38 ms: 1.74x slower                                                  |
| logging_silent             | 139 ns                                                 | 250 ns: 1.79x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 4.19 ms: 1.80x slower                                                  |
| scimark_sor                | 167 ms                                                 | 302 ms: 1.81x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 3.25 ms: 1.82x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 413 ms: 1.86x slower                                                   |
| go                         | 172 ms                                                 | 322 ms: 1.87x slower                                                   |
| sympy_expand               | 582 ms                                                 | 1.10 sec: 1.89x slower                                                 |
| deltablue                  | 4.27 ms                                                | 10.3 ms: 2.41x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 98.3 ms: 4.75x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.22x slower                                                           |

Benchmark hidden because not significant (7): deepcopy_memo, json, asyncio_websockets, json_loads, pathlib, xml_etree_generate, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.164x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.34x