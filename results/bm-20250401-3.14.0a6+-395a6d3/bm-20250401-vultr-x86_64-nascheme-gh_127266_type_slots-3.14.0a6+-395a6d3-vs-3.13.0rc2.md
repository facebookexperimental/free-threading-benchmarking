# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 395a6d3
- commit date: 2025-04-01
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 248 ms: 1.05x faster                                                     |
| docutils       | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                     |
| async_tree_io_tg           | 901 ms                                                                 | 623 ms: 1.45x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 610 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 499 ms: 1.34x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 310 ms: 1.32x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 256 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                     |
| async_generators           | 375 ms                                                                 | 327 ms: 1.15x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                    |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 196 ms: 1.10x faster                                                     |
| float          | 76.7 ms                                                                | 71.6 ms: 1.07x faster                                                    |
| nbody          | 85.3 ms                                                                | 97.2 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.61 ms: 1.23x faster                                                    |
| regex_dna      | 189 ms                                                                 | 167 ms: 1.13x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                    |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.94 sec: 1.03x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.3 ms: 1.03x faster                                                    |
| xml_etree_process    | 59.2 ms                                                                | 58.1 ms: 1.02x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 83.8 ms: 1.02x faster                                                    |
| json_loads           | 27.3 us                                                                | 27.0 us: 1.01x faster                                                    |
| unpickle_pure_python | 208 us                                                                 | 211 us: 1.01x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 302 us: 1.04x slower                                                     |
| json_dumps           | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.58 ms: 1.16x slower                                                    |
| python_startup         | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.4 ms: 1.07x faster                                                    |
| genshi_xml      | 49.1 ms                                                                | 47.7 ms: 1.03x faster                                                    |
| django_template | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                                    |
| mako            | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.17 sec: 2.00x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                     |
| async_tree_io_tg           | 901 ms                                                                 | 623 ms: 1.45x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 610 ms: 1.44x faster                                                     |
| deepcopy                   | 357 us                                                                 | 253 us: 1.41x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 499 ms: 1.34x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 310 ms: 1.32x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 256 ms: 1.30x faster                                                     |
| deepcopy_memo              | 38.1 us                                                                | 29.4 us: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                     |
| go                         | 141 ms                                                                 | 111 ms: 1.27x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.61 ms: 1.23x faster                                                    |
| deepcopy_reduce            | 3.12 us                                                                | 2.61 us: 1.20x faster                                                    |
| scimark_sor                | 134 ms                                                                 | 112 ms: 1.19x faster                                                     |
| pylint                     | 317 ms                                                                 | 275 ms: 1.15x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 93.6 ms: 1.15x faster                                                    |
| async_generators           | 375 ms                                                                 | 327 ms: 1.15x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 65.5 ms: 1.14x faster                                                    |
| regex_dna                  | 189 ms                                                                 | 167 ms: 1.13x faster                                                     |
| pidigits                   | 216 ms                                                                 | 196 ms: 1.10x faster                                                     |
| pyflate                    | 449 ms                                                                 | 409 ms: 1.10x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 320 ms: 1.09x faster                                                     |
| richards_super             | 50.4 ms                                                                | 46.4 ms: 1.09x faster                                                    |
| richards                   | 44.4 ms                                                                | 40.9 ms: 1.09x faster                                                    |
| float                      | 76.7 ms                                                                | 71.6 ms: 1.07x faster                                                    |
| telco                      | 7.77 ms                                                                | 7.26 ms: 1.07x faster                                                    |
| generators                 | 28.5 ms                                                                | 26.7 ms: 1.07x faster                                                    |
| logging_silent             | 98.2 ns                                                                | 92.1 ns: 1.07x faster                                                    |
| genshi_text                | 21.7 ms                                                                | 20.4 ms: 1.07x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.49 ms: 1.06x faster                                                    |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                     |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.25 sec: 1.05x faster                                                   |
| 2to3                       | 259 ms                                                                 | 248 ms: 1.05x faster                                                     |
| sympy_integrate            | 19.7 ms                                                                | 18.8 ms: 1.05x faster                                                    |
| coverage                   | 82.5 ms                                                                | 78.8 ms: 1.05x faster                                                    |
| docutils                   | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                   |
| logging_format             | 6.92 us                                                                | 6.63 us: 1.04x faster                                                    |
| deltablue                  | 3.10 ms                                                                | 2.97 ms: 1.04x faster                                                    |
| sqlite_synth               | 2.25 us                                                                | 2.17 us: 1.04x faster                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.4 ms: 1.04x faster                                                    |
| tomli_loads                | 2.01 sec                                                               | 1.94 sec: 1.03x faster                                                   |
| json                       | 4.98 ms                                                                | 4.82 ms: 1.03x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.3 ms: 1.03x faster                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 151 us: 1.03x faster                                                     |
| genshi_xml                 | 49.1 ms                                                                | 47.7 ms: 1.03x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 702 ms: 1.02x faster                                                     |
| logging_simple             | 6.14 us                                                                | 6.00 us: 1.02x faster                                                    |
| scimark_lu                 | 112 ms                                                                 | 110 ms: 1.02x faster                                                     |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                   |
| xml_etree_process          | 59.2 ms                                                                | 58.1 ms: 1.02x faster                                                    |
| sympy_str                  | 274 ms                                                                 | 269 ms: 1.02x faster                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 83.8 ms: 1.02x faster                                                    |
| pprint_pformat             | 1.46 sec                                                               | 1.43 sec: 1.02x faster                                                   |
| hexiom                     | 5.95 ms                                                                | 5.86 ms: 1.02x faster                                                    |
| chaos                      | 56.3 ms                                                                | 55.5 ms: 1.01x faster                                                    |
| json_loads                 | 27.3 us                                                                | 27.0 us: 1.01x faster                                                    |
| sympy_sum                  | 154 ms                                                                 | 152 ms: 1.01x faster                                                     |
| comprehensions             | 16.6 us                                                                | 16.4 us: 1.01x faster                                                    |
| meteor_contest             | 101 ms                                                                 | 101 ms: 1.01x faster                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 67.7 ms: 1.01x faster                                                    |
| django_template            | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                                    |
| unpickle_pure_python       | 208 us                                                                 | 211 us: 1.01x slower                                                     |
| raytrace                   | 250 ms                                                                 | 255 ms: 1.02x slower                                                     |
| pickle_pure_python         | 292 us                                                                 | 302 us: 1.04x slower                                                     |
| fannkuch                   | 376 ms                                                                 | 391 ms: 1.04x slower                                                     |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                    |
| json_dumps                 | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                                    |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.12x slower                                                    |
| nbody                      | 85.3 ms                                                                | 97.2 ms: 1.14x slower                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 8.58 ms: 1.16x slower                                                    |
| python_startup             | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                    |
| gc_traversal               | 3.32 ms                                                                | 4.60 ms: 1.39x slower                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.85 ms: 1.39x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 88.4 ms: 8.04x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                             |

Benchmark hidden because not significant (4): pathlib, asyncio_websockets, nqueens, sympy_expand
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250401-3.14.0a6+-395a6d3/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.13x