# Results vs. 3.12.6

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.077x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 313 ms: 1.19x slower                                                   |
| docutils       | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                 |
| html5lib       | 63.6 ms                                                | 73.8 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 616 ms: 1.76x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 294 ms: 1.58x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 359 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                   |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.9 ms: 1.04x faster                                                  |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| nbody          | 89.3 ms                                                | 140 ms: 1.56x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| regex_compile  | 142 ms                                                 | 157 ms: 1.10x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.0 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.43 sec: 1.15x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 98.7 ms: 1.16x slower                                                  |
| json_loads           | 26.5 us                                                | 31.0 us: 1.17x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 259 us: 1.18x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 70.8 ms: 1.20x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 382 us: 1.24x slower                                                   |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 61.9 ms: 1.23x slower                                                  |
| genshi_text     | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                  |
| django_template | 34.7 ms                                                | 44.1 ms: 1.27x slower                                                  |
| mako            | 11.0 ms                                                | 16.2 ms: 1.47x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 616 ms: 1.76x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 294 ms: 1.58x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 359 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.16 ms: 1.10x faster                                                  |
| deepcopy                   | 352 us                                                 | 322 us: 1.09x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 89.0 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.06x faster                                                  |
| float                      | 80.8 ms                                                | 77.9 ms: 1.04x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 39.3 us: 1.03x faster                                                  |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                                   |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.00x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.83 sec: 1.02x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                  |
| generators                 | 32.2 ms                                                | 33.2 ms: 1.03x slower                                                  |
| go                         | 139 ms                                                 | 145 ms: 1.04x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.22 sec: 1.04x slower                                                 |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 84.1 ms: 1.07x slower                                                  |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                                  |
| comprehensions             | 19.8 us                                                | 21.3 us: 1.07x slower                                                  |
| scimark_sor                | 130 ms                                                 | 139 ms: 1.07x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.30 us: 1.07x slower                                                  |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                 |
| regex_compile              | 142 ms                                                 | 157 ms: 1.10x slower                                                   |
| logging_silent             | 109 ns                                                 | 121 ns: 1.11x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.40 us: 1.12x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.6 ms: 1.13x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 162 ms: 1.14x slower                                                   |
| raytrace                   | 299 ms                                                 | 341 ms: 1.14x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 190 ms: 1.15x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 854 ms: 1.15x slower                                                   |
| chaos                      | 62.8 ms                                                | 72.4 ms: 1.15x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.43 sec: 1.15x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.79 sec: 1.15x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.15x slower                                                  |
| logging_format             | 7.35 us                                                | 8.50 us: 1.16x slower                                                  |
| pyflate                    | 448 ms                                                 | 519 ms: 1.16x slower                                                   |
| scimark_fft                | 342 ms                                                 | 396 ms: 1.16x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 98.7 ms: 1.16x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.76 sec: 1.16x slower                                                 |
| html5lib                   | 63.6 ms                                                | 73.8 ms: 1.16x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 124 ms: 1.16x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 89.3 ms: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.0 us: 1.17x slower                                                  |
| thrift                     | 791 us                                                 | 927 us: 1.17x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 259 us: 1.18x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.97 ms: 1.18x slower                                                  |
| sympy_str                  | 292 ms                                                 | 345 ms: 1.18x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 63.1 ms: 1.19x slower                                                  |
| 2to3                       | 264 ms                                                 | 313 ms: 1.19x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 70.8 ms: 1.20x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 24.7 ms: 1.20x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.21x slower                                                  |
| sympy_expand               | 468 ms                                                 | 570 ms: 1.22x slower                                                   |
| nqueens                    | 80.1 ms                                                | 98.1 ms: 1.23x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.59 ms: 1.23x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 61.9 ms: 1.23x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 84.5 ms: 1.23x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 382 us: 1.24x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.24x slower                                                   |
| genshi_text                | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 205 us: 1.26x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                  |
| django_template            | 34.7 ms                                                | 44.1 ms: 1.27x slower                                                  |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                                   |
| richards                   | 45.9 ms                                                | 59.3 ms: 1.29x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.72 ms: 1.30x slower                                                  |
| richards_super             | 51.9 ms                                                | 68.1 ms: 1.31x slower                                                  |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.32x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                  |
| telco                      | 6.53 ms                                                | 8.82 ms: 1.35x slower                                                  |
| coverage                   | 71.4 ms                                                | 97.6 ms: 1.37x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.83 ms: 1.40x slower                                                  |
| mako                       | 11.0 ms                                                | 16.2 ms: 1.47x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| nbody                      | 89.3 ms                                                | 140 ms: 1.56x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.2 ms: 8.81x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.36x