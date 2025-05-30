# Results vs. 3.13.0rc2

- fork: python
- ref: 8a4d4f37abb9fa639fdc
- machine: linux-x86_64
- commit hash: 8a4d4f3
- commit date: 2025-04-25
- overall geometric mean: 1.074x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 247 ms: 1.05x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 305 ms: 1.51x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 604 ms: 1.49x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 510 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 508 ms: 1.25x faster                                                   |
| async_generators           | 375 ms                                                                 | 326 ms: 1.15x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 69.1 ms: 1.11x faster                                                  |
| pidigits       | 216 ms                                                                 | 198 ms: 1.09x faster                                                   |
| nbody          | 85.3 ms                                                                | 87.8 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.68 ms: 1.20x faster                                                  |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                                   |
| regex_compile  | 131 ms                                                                 | 122 ms: 1.08x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 22.0 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.87 sec: 1.08x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 82.0 ms: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 131 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.9 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 57.7 ms: 1.03x faster                                                  |
| json_loads           | 27.3 us                                                                | 27.8 us: 1.02x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 213 us: 1.02x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 307 us: 1.05x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 11.3 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.65 ms: 1.17x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                                  |
| genshi_xml      | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                                  |
| django_template | 34.2 ms                                                                | 33.9 ms: 1.01x faster                                                  |
| mako            | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.07x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 305 ms: 1.51x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 604 ms: 1.49x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                   |
| deepcopy                   | 357 us                                                                 | 245 us: 1.46x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 28.9 us: 1.32x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 510 ms: 1.31x faster                                                   |
| go                         | 141 ms                                                                 | 108 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 508 ms: 1.25x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 109 ms: 1.23x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.56 us: 1.22x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.68 ms: 1.20x faster                                                  |
| async_generators           | 375 ms                                                                 | 326 ms: 1.15x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 94.2 ms: 1.14x faster                                                  |
| pylint                     | 317 ms                                                                 | 279 ms: 1.14x faster                                                   |
| float                      | 76.7 ms                                                                | 69.1 ms: 1.11x faster                                                  |
| pyflate                    | 449 ms                                                                 | 405 ms: 1.11x faster                                                   |
| telco                      | 7.77 ms                                                                | 7.06 ms: 1.10x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 67.7 ms: 1.10x faster                                                  |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.09x faster                                                   |
| scimark_fft                | 348 ms                                                                 | 321 ms: 1.09x faster                                                   |
| tomli_loads                | 2.01 sec                                                               | 1.87 sec: 1.08x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                                   |
| regex_compile              | 131 ms                                                                 | 122 ms: 1.08x faster                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.14 sec: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.43 ms: 1.07x faster                                                  |
| richards                   | 44.4 ms                                                                | 41.5 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 61.6 ms: 1.07x faster                                                  |
| richards_super             | 50.4 ms                                                                | 47.2 ms: 1.07x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 22.0 ms: 1.06x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 18.7 ms: 1.05x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.57 us: 1.05x faster                                                  |
| 2to3                       | 259 ms                                                                 | 247 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 688 ms: 1.05x faster                                                   |
| chaos                      | 56.3 ms                                                                | 53.9 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 82.0 ms: 1.04x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.40 sec: 1.04x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.74 ms: 1.04x faster                                                  |
| logging_simple             | 6.14 us                                                                | 5.93 us: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.04x faster                                                   |
| sympy_str                  | 274 ms                                                                 | 265 ms: 1.03x faster                                                   |
| genshi_xml                 | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.9 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 57.7 ms: 1.03x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.03x faster                                                  |
| generators                 | 28.5 ms                                                                | 27.8 ms: 1.03x faster                                                  |
| meteor_contest             | 101 ms                                                                 | 98.9 ms: 1.03x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.02x faster                                                 |
| logging_silent             | 98.2 ns                                                                | 96.1 ns: 1.02x faster                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 66.8 ms: 1.02x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 151 ms: 1.02x faster                                                   |
| sympy_expand               | 454 ms                                                                 | 445 ms: 1.02x faster                                                   |
| nqueens                    | 77.7 ms                                                                | 76.6 ms: 1.01x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 111 ms: 1.01x faster                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 154 us: 1.01x faster                                                   |
| json                       | 4.98 ms                                                                | 4.93 ms: 1.01x faster                                                  |
| raytrace                   | 250 ms                                                                 | 247 ms: 1.01x faster                                                   |
| django_template            | 34.2 ms                                                                | 33.9 ms: 1.01x faster                                                  |
| comprehensions             | 16.6 us                                                                | 16.7 us: 1.01x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 380 ms: 1.01x slower                                                   |
| json_loads                 | 27.3 us                                                                | 27.8 us: 1.02x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 213 us: 1.02x slower                                                   |
| nbody                      | 85.3 ms                                                                | 87.8 ms: 1.03x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.23 ms: 1.04x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 307 us: 1.05x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 11.3 ms: 1.06x slower                                                  |
| mako                       | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.13x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 8.65 ms: 1.17x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.45 ms: 1.34x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.86 ms: 1.39x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 88.1 ms: 8.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (3): coverage, asyncio_websockets, pathlib
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250425-3.14.0a7+-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x