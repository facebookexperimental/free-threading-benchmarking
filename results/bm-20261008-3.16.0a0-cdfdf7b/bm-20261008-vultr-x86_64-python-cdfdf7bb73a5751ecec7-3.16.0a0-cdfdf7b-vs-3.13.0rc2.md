# Results vs. 3.13.0rc2

- fork: python
- ref: cdfdf7bb73a5751ecec7
- machine: linux-x86_64
- commit hash: cdfdf7b
- commit date: 2026-10-08
- overall geometric mean: 1.032x faster
- HPT reliability: 99.68%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 257 ms: 1.01x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.37 sec: 1.11x faster                                                |
| html5lib       | 68.6 ms                                                                | 57.9 ms: 1.19x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 543 ms: 1.23x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 720 ms: 1.22x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 376 ms: 1.22x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 295 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 763 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 564 ms: 1.12x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 367 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 301 ms: 1.11x faster                                                  |
| async_generators           | 375 ms                                                                 | 347 ms: 1.08x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 187 ms: 1.15x faster                                                  |
| float          | 76.7 ms                                                                | 71.7 ms: 1.07x faster                                                 |
| nbody          | 85.3 ms                                                                | 89.7 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.65 ms: 1.21x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                 |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 148 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.26 ms: 1.15x faster                                                 |
| tomli_loads          | 2.01 sec                                                               | 1.82 sec: 1.10x faster                                                |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.3 ms: 1.02x faster                                                 |
| json_loads           | 27.3 us                                                                | 27.0 us: 1.01x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 211 us: 1.01x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 301 us: 1.03x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 89.3 ms: 1.05x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 63.0 ms: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.71 ms: 1.04x slower                                                 |
| python_startup         | 11.0 ms                                                                | 12.9 ms: 1.17x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| django_template | 34.2 ms                                                                | 36.8 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 113 ms: 2.81x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.05x faster                                                |
| deepcopy                   | 357 us                                                                 | 227 us: 1.57x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.9 us: 1.41x faster                                                 |
| go                         | 141 ms                                                                 | 103 ms: 1.36x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 119 us: 1.31x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 105 ms: 1.27x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.49 us: 1.25x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 543 ms: 1.23x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 720 ms: 1.22x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 376 ms: 1.22x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 88.3 ms: 1.22x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.65 ms: 1.21x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 295 ms: 1.20x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 57.9 ms: 1.19x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 763 ms: 1.18x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 298 ms: 1.17x faster                                                  |
| pyflate                    | 449 ms                                                                 | 389 ms: 1.16x faster                                                  |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.15x faster                                                  |
| json_dumps                 | 10.6 ms                                                                | 9.26 ms: 1.15x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.20 ms: 1.13x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 564 ms: 1.12x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 66.7 ms: 1.12x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 367 ms: 1.12x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.37 sec: 1.11x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 301 ms: 1.11x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.82 sec: 1.10x faster                                                |
| regex_v8                   | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                 |
| async_generators           | 375 ms                                                                 | 347 ms: 1.08x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| float                      | 76.7 ms                                                                | 71.7 ms: 1.07x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 18.0 ms: 1.07x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.2 ms: 1.06x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.65 ms: 1.05x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.8 us: 1.05x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.27 sec: 1.04x faster                                                |
| chaos                      | 56.3 ms                                                                | 54.0 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.16 us: 1.04x faster                                                 |
| logging_silent             | 98.2 ns                                                                | 94.6 ns: 1.04x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 75.3 ms: 1.03x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.7 ms: 1.03x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.1 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.3 ms: 1.02x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.1 ms: 1.02x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                 |
| json_loads                 | 27.3 us                                                                | 27.0 us: 1.01x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 100 ms: 1.01x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 372 ms: 1.01x faster                                                  |
| 2to3                       | 259 ms                                                                 | 257 ms: 1.01x faster                                                  |
| richards_super             | 50.4 ms                                                                | 50.1 ms: 1.01x faster                                                 |
| richards                   | 44.4 ms                                                                | 44.1 ms: 1.01x faster                                                 |
| raytrace                   | 250 ms                                                                 | 252 ms: 1.01x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.21 us: 1.01x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 211 us: 1.01x slower                                                  |
| json                       | 4.98 ms                                                                | 5.04 ms: 1.01x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 279 ms: 1.02x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 157 ms: 1.02x slower                                                  |
| thrift                     | 772 us                                                                 | 788 us: 1.02x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 738 ms: 1.03x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.50 sec: 1.03x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 301 us: 1.03x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 469 ms: 1.03x slower                                                  |
| coverage                   | 82.5 ms                                                                | 85.7 ms: 1.04x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 7.71 ms: 1.04x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 89.3 ms: 1.05x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| nbody                      | 85.3 ms                                                                | 89.7 ms: 1.05x slower                                                 |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 119 ms: 1.06x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 63.0 ms: 1.06x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.32 ms: 1.07x slower                                                 |
| django_template            | 34.2 ms                                                                | 36.8 ms: 1.08x slower                                                 |
| regex_compile              | 131 ms                                                                 | 148 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                                | 12.9 ms: 1.17x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.01 ms: 1.21x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.63 ms: 1.22x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                 |
| telco                      | 7.77 ms                                                                | 164 ms: 21.10x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 262 ms: 23.80x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): logging_format
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 99.68% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x