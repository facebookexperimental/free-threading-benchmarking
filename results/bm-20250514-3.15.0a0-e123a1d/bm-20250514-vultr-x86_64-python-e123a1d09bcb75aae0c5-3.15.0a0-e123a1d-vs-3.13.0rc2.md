# Results vs. 3.13.0rc2

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.069x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 249 ms: 1.04x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                |
| html5lib       | 68.6 ms                                                                | 61.2 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 601 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 627 ms: 1.44x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 310 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 272 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 515 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 506 ms: 1.25x faster                                                  |
| async_generators           | 375 ms                                                                 | 335 ms: 1.12x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 71.7 ms: 1.07x faster                                                 |
| pidigits       | 216 ms                                                                 | 205 ms: 1.06x faster                                                  |
| nbody          | 85.3 ms                                                                | 91.1 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.8 ms: 1.06x faster                                                 |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 132 ms: 1.03x faster                                                  |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 82.9 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.2 ms                                                                | 58.0 ms: 1.02x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 208 us: 1.00x faster                                                  |
| json_dumps           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 305 us: 1.04x slower                                                  |
| json_loads           | 27.3 us                                                                | 28.7 us: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.31 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.0 ms: 1.09x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                                 |
| django_template | 34.2 ms                                                                | 33.8 ms: 1.01x faster                                                 |
| mako            | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.05x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 601 ms: 1.47x faster                                                  |
| deepcopy                   | 357 us                                                                 | 247 us: 1.45x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 627 ms: 1.44x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.4 us: 1.34x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 310 ms: 1.32x faster                                                  |
| go                         | 141 ms                                                                 | 106 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 272 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 515 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 506 ms: 1.25x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 110 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.61 us: 1.20x faster                                                 |
| pylint                     | 317 ms                                                                 | 279 ms: 1.14x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                                 |
| pyflate                    | 449 ms                                                                 | 398 ms: 1.13x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 95.9 ms: 1.12x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 61.2 ms: 1.12x faster                                                 |
| async_generators           | 375 ms                                                                 | 335 ms: 1.12x faster                                                  |
| richards                   | 44.4 ms                                                                | 40.2 ms: 1.11x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 67.7 ms: 1.10x faster                                                 |
| richards_super             | 50.4 ms                                                                | 46.1 ms: 1.09x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 20.0 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.11 sec: 1.09x faster                                                |
| tomli_loads                | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.40 ms: 1.08x faster                                                 |
| float                      | 76.7 ms                                                                | 71.7 ms: 1.07x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 328 ms: 1.06x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.8 ms: 1.06x faster                                                 |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.33 ms: 1.06x faster                                                 |
| pidigits                   | 216 ms                                                                 | 205 ms: 1.06x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.65 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.5 ms: 1.05x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 18.8 ms: 1.05x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                |
| 2to3                       | 259 ms                                                                 | 249 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 132 ms: 1.03x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 698 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 82.9 ms: 1.03x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 266 ms: 1.03x faster                                                  |
| generators                 | 28.5 ms                                                                | 27.8 ms: 1.03x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 110 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.42 sec: 1.02x faster                                                |
| thrift                     | 772 us                                                                 | 755 us: 1.02x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 58.0 ms: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                |
| chaos                      | 56.3 ms                                                                | 55.2 ms: 1.02x faster                                                 |
| coverage                   | 82.5 ms                                                                | 81.0 ms: 1.02x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 76.5 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 7.31 ms: 1.01x faster                                                 |
| comprehensions             | 16.6 us                                                                | 16.3 us: 1.01x faster                                                 |
| django_template            | 34.2 ms                                                                | 33.8 ms: 1.01x faster                                                 |
| sympy_expand               | 454 ms                                                                 | 449 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| sympy_sum                  | 154 ms                                                                 | 153 ms: 1.01x faster                                                  |
| meteor_contest             | 101 ms                                                                 | 101 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 208 us                                                                 | 208 us: 1.00x faster                                                  |
| raytrace                   | 250 ms                                                                 | 251 ms: 1.01x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 157 us: 1.01x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 69.2 ms: 1.01x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 386 ms: 1.03x slower                                                  |
| json                       | 4.98 ms                                                                | 5.14 ms: 1.03x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.21 ms: 1.04x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 305 us: 1.04x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.7 us: 1.05x slower                                                 |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| nbody                      | 85.3 ms                                                                | 91.1 ms: 1.07x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.56 us: 1.07x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.49 us: 1.08x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.14x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.57 ms: 1.38x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.94 ms: 1.45x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 463 ns: 4.71x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 98.4 ms: 8.94x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): sqlite_synth, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x