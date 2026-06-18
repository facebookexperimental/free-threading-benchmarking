# Results vs. 3.13.0rc2

- fork: python
- ref: 9e863fab283eddca9c2a
- machine: linux-x86_64
- commit hash: 9e863fa
- commit date: 2026-06-17
- overall geometric mean: 1.029x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 257 ms: 1.01x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.43 sec: 1.08x faster                                                |
| html5lib       | 68.6 ms                                                                | 58.9 ms: 1.17x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.23x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 719 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 378 ms: 1.22x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 293 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 760 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 556 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 362 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 298 ms: 1.12x faster                                                  |
| async_generators           | 375 ms                                                                 | 341 ms: 1.10x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| float          | 76.7 ms                                                                | 75.6 ms: 1.02x faster                                                 |
| nbody          | 85.3 ms                                                                | 97.6 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.64 ms: 1.22x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.07x faster                                                 |
| regex_compile  | 131 ms                                                                 | 123 ms: 1.07x faster                                                  |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.68 ms: 1.10x faster                                                 |
| tomli_loads          | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| xml_etree_iterparse  | 94.4 ms                                                                | 90.0 ms: 1.05x faster                                                 |
| json_loads           | 27.3 us                                                                | 26.7 us: 1.02x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 86.1 ms: 1.01x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 60.8 ms: 1.03x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 215 us: 1.03x slower                                                  |
| xml_etree_parse      | 136 ms                                                                 | 142 ms: 1.05x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 314 us: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 6.95 ms: 1.07x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 35.7 ms: 1.05x slower                                                 |
| mako            | 11.2 ms                                                                | 11.8 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 115 ms: 2.76x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.07x faster                                                |
| deepcopy                   | 357 us                                                                 | 230 us: 1.55x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.5 us: 1.44x faster                                                 |
| go                         | 141 ms                                                                 | 107 ms: 1.32x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 119 us: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.23x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 719 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 378 ms: 1.22x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.64 ms: 1.22x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.57 us: 1.21x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 111 ms: 1.21x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 293 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 760 ms: 1.19x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 58.9 ms: 1.17x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 93.7 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 556 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 362 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 298 ms: 1.12x faster                                                  |
| pidigits                   | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| json_dumps                 | 10.6 ms                                                                | 9.68 ms: 1.10x faster                                                 |
| async_generators           | 375 ms                                                                 | 341 ms: 1.10x faster                                                  |
| pyflate                    | 449 ms                                                                 | 413 ms: 1.09x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 17.7 ms: 1.09x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| docutils                   | 2.63 sec                                                               | 2.43 sec: 1.08x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 69.0 ms: 1.08x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.07x faster                                                 |
| regex_compile              | 131 ms                                                                 | 123 ms: 1.07x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 6.95 ms: 1.07x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 327 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.21 sec: 1.06x faster                                                |
| nqueens                    | 77.7 ms                                                                | 74.1 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 90.0 ms: 1.05x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.8 us: 1.05x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.1 ms: 1.03x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.78 ms: 1.03x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 64.1 ms: 1.03x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.8 ms: 1.03x faster                                                 |
| json_loads                 | 27.3 us                                                                | 26.7 us: 1.02x faster                                                 |
| logging_simple             | 6.14 us                                                                | 6.00 us: 1.02x faster                                                 |
| chaos                      | 56.3 ms                                                                | 55.1 ms: 1.02x faster                                                 |
| richards                   | 44.4 ms                                                                | 43.5 ms: 1.02x faster                                                 |
| richards_super             | 50.4 ms                                                                | 49.4 ms: 1.02x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.80 us: 1.02x faster                                                 |
| float                      | 76.7 ms                                                                | 75.6 ms: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.68 ms: 1.01x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 100.0 ms: 1.01x faster                                                |
| 2to3                       | 259 ms                                                                 | 257 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                                 |
| logging_silent             | 98.2 ns                                                                | 98.9 ns: 1.01x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 379 ms: 1.01x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 86.1 ms: 1.01x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 727 ms: 1.01x slower                                                  |
| thrift                     | 772 us                                                                 | 782 us: 1.01x slower                                                  |
| coverage                   | 82.5 ms                                                                | 83.8 ms: 1.02x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 462 ms: 1.02x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.48 sec: 1.02x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 158 ms: 1.02x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 69.7 ms: 1.02x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 115 ms: 1.02x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 60.8 ms: 1.03x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 215 us: 1.03x slower                                                  |
| raytrace                   | 250 ms                                                                 | 259 ms: 1.04x slower                                                  |
| django_template            | 34.2 ms                                                                | 35.7 ms: 1.05x slower                                                 |
| xml_etree_parse            | 136 ms                                                                 | 142 ms: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.05x slower                                                |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.06x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 314 us: 1.08x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.44 ms: 1.11x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| nbody                      | 85.3 ms                                                                | 97.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.02 ms: 1.21x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.68 ms: 1.26x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                 |
| telco                      | 7.77 ms                                                                | 160 ms: 20.56x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 311 ms: 28.23x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (3): json, sqlite_synth, sympy_str
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260617-3.16.0a0-9e863fa/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 99.80% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x