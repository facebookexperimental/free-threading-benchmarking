# Results vs. 3.13.0rc2

- fork: mpage
- ref: measure_latest_lfb
- machine: linux-x86_64
- commit hash: 80fc5aa
- commit date: 2025-03-23
- overall geometric mean: 1.037x faster
- HPT reliability: 60.03%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 269 ms: 1.04x slower                                                |
| html5lib       | 68.6 ms                                                                | 61.7 ms: 1.11x faster                                               |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 486 ms: 1.85x faster                                                |
| async_tree_io              | 881 ms                                                                 | 519 ms: 1.70x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 211 ms: 1.58x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 299 ms: 1.54x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 267 ms: 1.54x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 430 ms: 1.47x faster                                                |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 464 ms: 1.44x faster                                                |
| async_tree_none            | 353 ms                                                                 | 250 ms: 1.41x faster                                                |
| coroutines                 | 23.3 ms                                                                | 19.7 ms: 1.18x faster                                               |
| async_generators           | 375 ms                                                                 | 332 ms: 1.13x faster                                                |
| Geometric mean             | (ref)                                                                  | 1.42x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 64.2 ms: 1.20x faster                                               |
| pidigits       | 216 ms                                                                 | 187 ms: 1.16x faster                                                |
| nbody          | 85.3 ms                                                                | 108 ms: 1.27x slower                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.99 ms: 1.07x faster                                               |
| regex_v8       | 23.2 ms                                                                | 21.8 ms: 1.06x faster                                               |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.03x faster                                                |
| regex_compile  | 131 ms                                                                 | 135 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 84.3 ms: 1.12x faster                                               |
| xml_etree_generate   | 85.4 ms                                                                | 84.1 ms: 1.02x faster                                               |
| tomli_loads          | 2.01 sec                                                               | 2.00 sec: 1.00x faster                                              |
| xml_etree_process    | 59.2 ms                                                                | 59.7 ms: 1.01x slower                                               |
| xml_etree_parse      | 136 ms                                                                 | 141 ms: 1.03x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 218 us: 1.05x slower                                                |
| pickle_pure_python   | 292 us                                                                 | 311 us: 1.07x slower                                                |
| json_loads           | 27.3 us                                                                | 29.3 us: 1.07x slower                                               |
| json_dumps           | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.03x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                               |
| python_startup_no_site | 7.41 ms                                                                | 11.0 ms: 1.48x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.44x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 50.6 ms: 1.03x slower                                               |
| django_template | 34.2 ms                                                                | 36.5 ms: 1.07x slower                                               |
| genshi_text     | 21.7 ms                                                                | 23.4 ms: 1.08x slower                                               |
| mako            | 11.2 ms                                                                | 14.4 ms: 1.28x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.11x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 486 ms: 1.85x faster                                                |
| async_tree_io              | 881 ms                                                                 | 519 ms: 1.70x faster                                                |
| gc_traversal               | 3.32 ms                                                                | 2.08 ms: 1.59x faster                                               |
| async_tree_none_tg         | 333 ms                                                                 | 211 ms: 1.58x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 299 ms: 1.54x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 267 ms: 1.54x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 430 ms: 1.47x faster                                                |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 464 ms: 1.44x faster                                                |
| async_tree_none            | 353 ms                                                                 | 250 ms: 1.41x faster                                                |
| deepcopy                   | 357 us                                                                 | 260 us: 1.37x faster                                                |
| scimark_sor                | 134 ms                                                                 | 107 ms: 1.25x faster                                                |
| float                      | 76.7 ms                                                                | 64.2 ms: 1.20x faster                                               |
| go                         | 141 ms                                                                 | 118 ms: 1.19x faster                                                |
| deepcopy_memo              | 38.1 us                                                                | 32.1 us: 1.19x faster                                               |
| coroutines                 | 23.3 ms                                                                | 19.7 ms: 1.18x faster                                               |
| scimark_fft                | 348 ms                                                                 | 294 ms: 1.18x faster                                                |
| spectral_norm              | 108 ms                                                                 | 92.2 ms: 1.17x faster                                               |
| deepcopy_reduce            | 3.12 us                                                                | 2.68 us: 1.17x faster                                               |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.16x faster                                                |
| logging_silent             | 98.2 ns                                                                | 85.3 ns: 1.15x faster                                               |
| sqlite_synth               | 2.25 us                                                                | 1.96 us: 1.15x faster                                               |
| async_generators           | 375 ms                                                                 | 332 ms: 1.13x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 84.3 ms: 1.12x faster                                               |
| html5lib                   | 68.6 ms                                                                | 61.7 ms: 1.11x faster                                               |
| pylint                     | 317 ms                                                                 | 293 ms: 1.08x faster                                                |
| regex_effbot               | 3.21 ms                                                                | 2.99 ms: 1.07x faster                                               |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.46 ms: 1.07x faster                                               |
| regex_v8                   | 23.2 ms                                                                | 21.8 ms: 1.06x faster                                               |
| dulwich_log                | 74.5 ms                                                                | 70.8 ms: 1.05x faster                                               |
| bpe_tokeniser              | 4.46 sec                                                               | 4.29 sec: 1.04x faster                                              |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.03x faster                                                |
| pyflate                    | 449 ms                                                                 | 438 ms: 1.03x faster                                                |
| pathlib                    | 19.3 ms                                                                | 18.9 ms: 1.02x faster                                               |
| xml_etree_generate         | 85.4 ms                                                                | 84.1 ms: 1.02x faster                                               |
| scimark_monte_carlo        | 65.8 ms                                                                | 65.0 ms: 1.01x faster                                               |
| generators                 | 28.5 ms                                                                | 28.3 ms: 1.01x faster                                               |
| tomli_loads                | 2.01 sec                                                               | 2.00 sec: 1.00x faster                                              |
| chaos                      | 56.3 ms                                                                | 56.7 ms: 1.01x slower                                               |
| xml_etree_process          | 59.2 ms                                                                | 59.7 ms: 1.01x slower                                               |
| richards                   | 44.4 ms                                                                | 45.2 ms: 1.02x slower                                               |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                              |
| regex_compile              | 131 ms                                                                 | 135 ms: 1.03x slower                                                |
| telco                      | 7.77 ms                                                                | 7.98 ms: 1.03x slower                                               |
| comprehensions             | 16.6 us                                                                | 17.0 us: 1.03x slower                                               |
| genshi_xml                 | 49.1 ms                                                                | 50.6 ms: 1.03x slower                                               |
| json                       | 4.98 ms                                                                | 5.15 ms: 1.03x slower                                               |
| xml_etree_parse            | 136 ms                                                                 | 141 ms: 1.03x slower                                                |
| 2to3                       | 259 ms                                                                 | 269 ms: 1.04x slower                                                |
| pprint_safe_repr           | 719 ms                                                                 | 751 ms: 1.04x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 218 us: 1.05x slower                                                |
| thrift                     | 772 us                                                                 | 813 us: 1.05x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.27 ms: 1.06x slower                                               |
| pprint_pformat             | 1.46 sec                                                               | 1.54 sec: 1.06x slower                                              |
| nqueens                    | 77.7 ms                                                                | 82.7 ms: 1.06x slower                                               |
| richards_super             | 50.4 ms                                                                | 53.7 ms: 1.07x slower                                               |
| logging_simple             | 6.14 us                                                                | 6.55 us: 1.07x slower                                               |
| django_template            | 34.2 ms                                                                | 36.5 ms: 1.07x slower                                               |
| pickle_pure_python         | 292 us                                                                 | 311 us: 1.07x slower                                                |
| raytrace                   | 250 ms                                                                 | 267 ms: 1.07x slower                                                |
| json_loads                 | 27.3 us                                                                | 29.3 us: 1.07x slower                                               |
| sympy_integrate            | 19.7 ms                                                                | 21.2 ms: 1.08x slower                                               |
| genshi_text                | 21.7 ms                                                                | 23.4 ms: 1.08x slower                                               |
| logging_format             | 6.92 us                                                                | 7.44 us: 1.08x slower                                               |
| hexiom                     | 5.95 ms                                                                | 6.41 ms: 1.08x slower                                               |
| fannkuch                   | 376 ms                                                                 | 412 ms: 1.09x slower                                                |
| sympy_expand               | 454 ms                                                                 | 498 ms: 1.10x slower                                                |
| sympy_str                  | 274 ms                                                                 | 302 ms: 1.10x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 170 ms: 1.10x slower                                                |
| typing_runtime_protocols   | 156 us                                                                 | 173 us: 1.11x slower                                                |
| coverage                   | 82.5 ms                                                                | 94.1 ms: 1.14x slower                                               |
| crypto_pyaes               | 68.2 ms                                                                | 79.0 ms: 1.16x slower                                               |
| meteor_contest             | 101 ms                                                                 | 118 ms: 1.16x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                               |
| mdp                        | 2.34 sec                                                               | 2.83 sec: 1.21x slower                                              |
| nbody                      | 85.3 ms                                                                | 108 ms: 1.27x slower                                                |
| mako                       | 11.2 ms                                                                | 14.4 ms: 1.28x slower                                               |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                               |
| python_startup_no_site     | 7.41 ms                                                                | 11.0 ms: 1.48x slower                                               |
| bench_thread_pool          | 924 us                                                                 | 3.07 ms: 3.32x slower                                               |
| bench_mp_pool              | 11.0 ms                                                                | 95.0 ms: 8.64x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (4): scimark_lu, asyncio_websockets, docutils, create_gc_cycles
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250323-3.14.0a6+-80fc5aa-CLANG,NOGIL/bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6+-80fc5aa.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 60.03% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.40x