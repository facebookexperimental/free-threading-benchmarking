# Results vs. 3.13.0rc2

- fork: python
- ref: b90ecea9e6b33dae360e
- machine: linux-x86_64
- commit hash: b90ecea
- commit date: 2025-06-05
- overall geometric mean: 1.067x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 249 ms: 1.04x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                |
| html5lib       | 68.6 ms                                                                | 60.9 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 593 ms: 1.49x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 618 ms: 1.46x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 249 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 265 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 507 ms: 1.25x faster                                                  |
| async_generators           | 375 ms                                                                 | 332 ms: 1.13x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| float          | 76.7 ms                                                                | 70.8 ms: 1.08x faster                                                 |
| nbody          | 85.3 ms                                                                | 86.4 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                                 |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 22.7 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.90 sec: 1.06x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 82.7 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.8 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.2 ms                                                                | 58.2 ms: 1.02x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 210 us: 1.01x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                 |
| json_loads           | 27.3 us                                                                | 28.2 us: 1.03x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 306 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.28 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.3 ms: 1.07x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 48.1 ms: 1.02x faster                                                 |
| django_template | 34.2 ms                                                                | 34.6 ms: 1.01x slower                                                 |
| mako            | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.05x faster                                                |
| async_tree_io              | 881 ms                                                                 | 593 ms: 1.49x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 618 ms: 1.46x faster                                                  |
| deepcopy                   | 357 us                                                                 | 253 us: 1.42x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 249 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 265 ms: 1.33x faster                                                  |
| go                         | 141 ms                                                                 | 106 ms: 1.32x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 29.1 us: 1.31x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 507 ms: 1.25x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 112 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.65 us: 1.18x faster                                                 |
| pylint                     | 317 ms                                                                 | 277 ms: 1.14x faster                                                  |
| async_generators           | 375 ms                                                                 | 332 ms: 1.13x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 60.9 ms: 1.13x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 66.2 ms: 1.12x faster                                                 |
| pidigits                   | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| pyflate                    | 449 ms                                                                 | 407 ms: 1.10x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                                 |
| float                      | 76.7 ms                                                                | 70.8 ms: 1.08x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 99.3 ms: 1.08x faster                                                 |
| richards_super             | 50.4 ms                                                                | 46.8 ms: 1.08x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.15 sec: 1.07x faster                                                |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.27 ms: 1.07x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 61.6 ms: 1.07x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 20.3 ms: 1.07x faster                                                 |
| richards                   | 44.4 ms                                                                | 41.6 ms: 1.07x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 327 ms: 1.06x faster                                                  |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.90 sec: 1.06x faster                                                |
| sympy_integrate            | 19.7 ms                                                                | 18.7 ms: 1.05x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.8 us: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                  |
| 2to3                       | 259 ms                                                                 | 249 ms: 1.04x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                |
| hexiom                     | 5.95 ms                                                                | 5.74 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 82.7 ms: 1.03x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 266 ms: 1.03x faster                                                  |
| generators                 | 28.5 ms                                                                | 27.7 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.8 ms: 1.03x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 151 us: 1.03x faster                                                  |
| thrift                     | 772 us                                                                 | 752 us: 1.03x faster                                                  |
| nqueens                    | 77.7 ms                                                                | 75.8 ms: 1.03x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.64 ms: 1.02x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 22.7 ms: 1.02x faster                                                 |
| genshi_xml                 | 49.1 ms                                                                | 48.1 ms: 1.02x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.0 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 7.28 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 58.2 ms: 1.02x faster                                                 |
| sympy_expand               | 454 ms                                                                 | 447 ms: 1.02x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 152 ms: 1.01x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 111 ms: 1.01x faster                                                  |
| meteor_contest             | 101 ms                                                                 | 100 ms: 1.01x faster                                                  |
| coverage                   | 82.5 ms                                                                | 81.5 ms: 1.01x faster                                                 |
| chaos                      | 56.3 ms                                                                | 56.1 ms: 1.00x faster                                                 |
| raytrace                   | 250 ms                                                                 | 251 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 210 us: 1.01x slower                                                  |
| django_template            | 34.2 ms                                                                | 34.6 ms: 1.01x slower                                                 |
| nbody                      | 85.3 ms                                                                | 86.4 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| json                       | 4.98 ms                                                                | 5.09 ms: 1.02x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 387 ms: 1.03x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.2 us: 1.03x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 306 us: 1.05x slower                                                  |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.28 us: 1.05x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.48 us: 1.06x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.31 ms: 1.07x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 777 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.59 sec: 1.09x slower                                                |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.5 ms: 1.14x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.37 ms: 1.32x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.91 ms: 1.43x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 469 ns: 4.78x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 98.0 ms: 8.91x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (3): sqlite_synth, asyncio_websockets, pathlib
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.067x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x