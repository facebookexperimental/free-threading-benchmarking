# Results vs. 3.12.6

- fork: python
- ref: 30efede33ca1fe32debb
- machine: linux-x86_64
- commit hash: 30efede
- commit date: 2024-12-24
- overall geometric mean: 1.093x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.78 sec: 1.06x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 905 ms: 2.14x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 927 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 473 ms: 1.97x faster                                                   |
| async_tree_none            | 741 ms                                                 | 390 ms: 1.90x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 524 ms: 1.86x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 383 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 697 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 686 ms: 1.57x faster                                                   |
| async_generators           | 589 ms                                                 | 561 ms: 1.05x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.6 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.56x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 115 ms: 1.07x faster                                                   |
| pidigits       | 250 ms                                                 | 241 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 129 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.26 ms: 1.20x faster                                                  |
| regex_compile  | 187 ms                                                 | 176 ms: 1.06x faster                                                   |
| regex_dna      | 278 ms                                                 | 267 ms: 1.04x faster                                                   |
| regex_v8       | 32.5 ms                                                | 35.0 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 207 ms: 1.16x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.61 sec: 1.11x faster                                                 |
| xml_etree_generate  | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| json_loads          | 37.9 us                                                | 35.9 us: 1.05x faster                                                  |
| json_dumps          | 14.3 ms                                                | 16.0 ms: 1.12x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (3): unpickle_pure_python, pickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.8 ms: 1.19x faster                                                  |
| python_startup         | 23.7 ms                                                | 26.0 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 48.1 ms: 1.07x slower                                                  |
| mako            | 15.7 ms                                                | 16.9 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 905 ms: 2.14x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 927 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 473 ms: 1.97x faster                                                   |
| async_tree_none            | 741 ms                                                 | 390 ms: 1.90x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 524 ms: 1.86x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 383 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 697 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 686 ms: 1.57x faster                                                   |
| deepcopy                   | 468 us                                                 | 343 us: 1.36x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 39.5 us: 1.33x faster                                                  |
| logging_simple             | 9.45 us                                                | 7.60 us: 1.24x faster                                                  |
| comprehensions             | 27.1 us                                                | 22.3 us: 1.22x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 179 ms: 1.21x faster                                                   |
| sqlglot_normalize          | 157 ms                                                 | 130 ms: 1.20x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.26 ms: 1.20x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 14.8 ms: 1.19x faster                                                  |
| raytrace                   | 408 ms                                                 | 345 ms: 1.18x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 207 ms: 1.16x faster                                                   |
| pylint                     | 465 ms                                                 | 401 ms: 1.16x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 94.0 ms: 1.14x faster                                                  |
| richards_super             | 72.8 ms                                                | 63.9 ms: 1.14x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.61 sec: 1.12x faster                                                 |
| scimark_fft                | 500 ms                                                 | 449 ms: 1.11x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.13 ms: 1.11x faster                                                  |
| pathlib                    | 31.6 ms                                                | 28.5 ms: 1.11x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.61 sec: 1.11x faster                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.12 ms: 1.10x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 6.01 sec: 1.10x faster                                                 |
| sympy_sum                  | 222 ms                                                 | 203 ms: 1.09x faster                                                   |
| logging_format             | 9.59 us                                                | 8.76 us: 1.09x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.70 us: 1.09x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.64 sec: 1.09x faster                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 88.6 ms: 1.09x faster                                                  |
| scimark_sor                | 167 ms                                                 | 153 ms: 1.09x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 22.7 ms: 1.09x faster                                                  |
| spectral_norm              | 156 ms                                                 | 144 ms: 1.08x faster                                                   |
| nqueens                    | 117 ms                                                 | 109 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.27 ms: 1.07x faster                                                  |
| float                      | 123 ms                                                 | 115 ms: 1.07x faster                                                   |
| pyflate                    | 727 ms                                                 | 684 ms: 1.06x faster                                                   |
| regex_compile              | 187 ms                                                 | 176 ms: 1.06x faster                                                   |
| sqlglot_parse              | 1.79 ms                                                | 1.68 ms: 1.06x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.78 sec: 1.06x faster                                                 |
| json_loads                 | 37.9 us                                                | 35.9 us: 1.05x faster                                                  |
| fannkuch                   | 540 ms                                                 | 514 ms: 1.05x faster                                                   |
| async_generators           | 589 ms                                                 | 561 ms: 1.05x faster                                                   |
| regex_dna                  | 278 ms                                                 | 267 ms: 1.04x faster                                                   |
| generators                 | 41.1 ms                                                | 39.6 ms: 1.04x faster                                                  |
| pidigits                   | 250 ms                                                 | 241 ms: 1.04x faster                                                   |
| pprint_safe_repr           | 967 ms                                                 | 936 ms: 1.03x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.92 sec: 1.03x faster                                                 |
| coroutines                 | 29.5 ms                                                | 30.6 ms: 1.04x slower                                                  |
| sympy_expand               | 582 ms                                                 | 609 ms: 1.05x slower                                                   |
| deltablue                  | 4.27 ms                                                | 4.51 ms: 1.06x slower                                                  |
| django_template            | 44.9 ms                                                | 48.1 ms: 1.07x slower                                                  |
| mako                       | 15.7 ms                                                | 16.9 ms: 1.07x slower                                                  |
| hexiom                     | 8.27 ms                                                | 8.87 ms: 1.07x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 35.0 ms: 1.08x slower                                                  |
| telco                      | 9.59 ms                                                | 10.3 ms: 1.08x slower                                                  |
| nbody                      | 119 ms                                                 | 129 ms: 1.08x slower                                                   |
| python_startup             | 23.7 ms                                                | 26.0 ms: 1.10x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.0 ms: 1.12x slower                                                  |
| coverage                   | 95.4 ms                                                | 110 ms: 1.15x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 9.27 ms: 1.58x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.90 ms: 2.01x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 94.0 ms: 4.54x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (22): sympy_integrate, thrift, json, scimark_lu, unpickle_pure_python, sqlite_synth, go, dulwich_log, richards, typing_runtime_protocols, 2to3, sympy_str, logging_silent, chaos, asyncio_websockets, pickle_pure_python, xml_etree_process, genshi_xml, meteor_contest, html5lib, genshi_text, sqlglot_optimize
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.093x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x