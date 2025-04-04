# Results vs. 3.13.0rc2

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: linux-x86_64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.107x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 311 ms: 1.20x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.90 sec: 1.10x slower                                                 |
| html5lib       | 68.6 ms                                                                | 73.9 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 574 ms: 1.57x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 317 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 530 ms: 1.26x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 286 ms: 1.24x faster                                                   |
| async_generators           | 375 ms                                                                 | 392 ms: 1.05x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 27.2 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.21x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 210 ms: 1.03x faster                                                   |
| float          | 76.7 ms                                                                | 77.1 ms: 1.01x slower                                                  |
| nbody          | 85.3 ms                                                                | 135 ms: 1.58x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.72 ms: 1.18x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                                  |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.07x faster                                                   |
| regex_compile  | 131 ms                                                                 | 170 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 131 ms: 1.04x faster                                                   |
| json_loads           | 27.3 us                                                                | 29.6 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 102 ms: 1.19x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 13.1 ms: 1.24x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 74.1 ms: 1.25x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.53 sec: 1.26x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 270 us: 1.29x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 378 us: 1.30x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.17x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 44.6 ms: 1.30x slower                                                  |
| genshi_xml      | 49.1 ms                                                                | 67.5 ms: 1.37x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 31.5 ms: 1.45x slower                                                  |
| mako            | 11.2 ms                                                                | 16.5 ms: 1.47x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.40x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.79 ms: 1.85x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.46 sec: 1.60x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 574 ms: 1.57x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 317 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 530 ms: 1.26x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 286 ms: 1.24x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.72 ms: 1.18x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                                  |
| deepcopy                   | 357 us                                                                 | 329 us: 1.09x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.07x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.04x faster                                                   |
| pidigits                   | 216 ms                                                                 | 210 ms: 1.03x faster                                                   |
| float                      | 76.7 ms                                                                | 77.1 ms: 1.01x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                  |
| json                       | 4.98 ms                                                                | 5.13 ms: 1.03x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.9 ms: 1.03x slower                                                  |
| async_generators           | 375 ms                                                                 | 392 ms: 1.05x slower                                                   |
| dulwich_log                | 74.5 ms                                                                | 78.2 ms: 1.05x slower                                                  |
| deepcopy_memo              | 38.1 us                                                                | 40.4 us: 1.06x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.34 us: 1.07x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 73.9 ms: 1.08x slower                                                  |
| json_loads                 | 27.3 us                                                                | 29.6 us: 1.08x slower                                                  |
| go                         | 141 ms                                                                 | 153 ms: 1.09x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.23 sec: 1.10x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 384 ms: 1.10x slower                                                   |
| docutils                   | 2.63 sec                                                               | 2.90 sec: 1.10x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.94 sec: 1.11x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 121 ms: 1.12x slower                                                   |
| telco                      | 7.77 ms                                                                | 8.75 ms: 1.12x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 152 ms: 1.14x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.51 ms: 1.16x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 27.2 ms: 1.17x slower                                                  |
| pyflate                    | 449 ms                                                                 | 533 ms: 1.19x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 102 ms: 1.19x slower                                                   |
| 2to3                       | 259 ms                                                                 | 311 ms: 1.20x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 876 ms: 1.22x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 24.3 ms: 1.23x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 13.1 ms: 1.24x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.81 sec: 1.25x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 74.1 ms: 1.25x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 141 ms: 1.26x slower                                                   |
| tomli_loads                | 2.01 sec                                                               | 2.53 sec: 1.26x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 196 ms: 1.27x slower                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.0 ms: 1.28x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 125 ns: 1.28x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 354 ms: 1.29x slower                                                   |
| regex_compile              | 131 ms                                                                 | 170 ms: 1.29x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 270 us: 1.29x slower                                                   |
| chaos                      | 56.3 ms                                                                | 72.9 ms: 1.30x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 378 us: 1.30x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 590 ms: 1.30x slower                                                   |
| django_template            | 34.2 ms                                                                | 44.6 ms: 1.30x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 102 ms: 1.31x slower                                                   |
| comprehensions             | 16.6 us                                                                | 21.9 us: 1.32x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 90.7 ms: 1.33x slower                                                  |
| coverage                   | 82.5 ms                                                                | 110 ms: 1.33x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 137 ms: 1.35x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 210 us: 1.35x slower                                                   |
| raytrace                   | 250 ms                                                                 | 337 ms: 1.35x slower                                                   |
| richards_super             | 50.4 ms                                                                | 68.3 ms: 1.36x slower                                                  |
| richards                   | 44.4 ms                                                                | 60.4 ms: 1.36x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 8.15 ms: 1.37x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 515 ms: 1.37x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 67.5 ms: 1.37x slower                                                  |
| logging_simple             | 6.14 us                                                                | 8.46 us: 1.38x slower                                                  |
| logging_format             | 6.92 us                                                                | 9.66 us: 1.40x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 4.47 ms: 1.44x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 31.5 ms: 1.45x slower                                                  |
| mako                       | 11.2 ms                                                                | 16.5 ms: 1.47x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| generators                 | 28.5 ms                                                                | 44.1 ms: 1.55x slower                                                  |
| nbody                      | 85.3 ms                                                                | 135 ms: 1.58x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.19 ms: 3.45x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 97.1 ms: 8.83x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                           |

Benchmark hidden because not significant (3): asyncio_websockets, xml_etree_iterparse, pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.107x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.35x