# Results vs. 3.13.0rc2

- fork: python
- ref: 910a92babf40b7b34baa
- machine: linux-x86_64
- commit hash: 910a92b
- commit date: 2026-11-16
- overall geometric mean: 1.055x faster
- HPT reliability: 99.69%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 252 ms: 1.03x faster                                                      |
| docutils       | 2.63 sec                                                               | 2.30 sec: 1.14x faster                                                    |
| html5lib       | 68.6 ms                                                                | 57.0 ms: 1.20x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators           | 375 ms                                                                 | 225 ms: 1.67x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 655 ms: 1.35x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 505 ms: 1.32x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 692 ms: 1.30x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 518 ms: 1.22x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 342 ms: 1.20x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 280 ms: 1.19x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.02x slower                                                     |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 177 ms: 1.22x faster                                                      |
| float          | 76.7 ms                                                                | 72.9 ms: 1.05x faster                                                     |
| nbody          | 85.3 ms                                                                | 89.6 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                     |
| regex_dna      | 189 ms                                                                 | 184 ms: 1.03x faster                                                      |
| regex_compile  | 131 ms                                                                 | 148 ms: 1.12x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.11 ms: 1.17x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.83 sec: 1.10x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.3 ms: 1.03x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 86.0 ms: 1.01x slower                                                     |
| unpickle_pure_python | 208 us                                                                 | 211 us: 1.01x slower                                                      |
| xml_etree_process    | 59.2 ms                                                                | 61.8 ms: 1.04x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 145 ms: 1.07x slower                                                      |
| pickle_pure_python   | 292 us                                                                 | 315 us: 1.08x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.33 ms: 1.01x faster                                                     |
| python_startup         | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 11.6 ms: 1.04x slower                                                     |
| django_template | 34.2 ms                                                                | 35.5 ms: 1.04x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.04x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 107 ms: 2.96x faster                                                      |
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.07x faster                                                    |
| async_generators           | 375 ms                                                                 | 225 ms: 1.67x faster                                                      |
| deepcopy                   | 357 us                                                                 | 234 us: 1.53x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 108 us: 1.44x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 27.8 us: 1.37x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 655 ms: 1.35x faster                                                      |
| go                         | 141 ms                                                                 | 105 ms: 1.33x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 505 ms: 1.32x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 692 ms: 1.30x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.28x faster                                                      |
| scimark_sor                | 134 ms                                                                 | 108 ms: 1.23x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 518 ms: 1.22x faster                                                      |
| pidigits                   | 216 ms                                                                 | 177 ms: 1.22x faster                                                      |
| deepcopy_reduce            | 3.12 us                                                                | 2.57 us: 1.21x faster                                                     |
| html5lib                   | 68.6 ms                                                                | 57.0 ms: 1.20x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 342 ms: 1.20x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 280 ms: 1.19x faster                                                      |
| spectral_norm              | 108 ms                                                                 | 90.8 ms: 1.19x faster                                                     |
| json_dumps                 | 10.6 ms                                                                | 9.11 ms: 1.17x faster                                                     |
| pyflate                    | 449 ms                                                                 | 387 ms: 1.16x faster                                                      |
| docutils                   | 2.63 sec                                                               | 2.30 sec: 1.14x faster                                                    |
| dulwich_log                | 74.5 ms                                                                | 65.4 ms: 1.14x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 308 ms: 1.13x faster                                                      |
| regex_effbot               | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.32 ms: 1.10x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.83 sec: 1.10x faster                                                    |
| pathlib                    | 19.3 ms                                                                | 17.7 ms: 1.09x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.15 sec: 1.07x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                     |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.2 ms: 1.06x faster                                                     |
| hexiom                     | 5.95 ms                                                                | 5.64 ms: 1.06x faster                                                     |
| float                      | 76.7 ms                                                                | 72.9 ms: 1.05x faster                                                     |
| nqueens                    | 77.7 ms                                                                | 74.1 ms: 1.05x faster                                                     |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.04x faster                                                     |
| sympy_integrate            | 19.7 ms                                                                | 19.0 ms: 1.04x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.3 ms: 1.03x faster                                                     |
| 2to3                       | 259 ms                                                                 | 252 ms: 1.03x faster                                                      |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.03x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 184 ms: 1.03x faster                                                      |
| logging_silent             | 98.2 ns                                                                | 95.6 ns: 1.03x faster                                                     |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.02x faster                                                    |
| chaos                      | 56.3 ms                                                                | 55.0 ms: 1.02x faster                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 67.2 ms: 1.01x faster                                                     |
| python_startup_no_site     | 7.41 ms                                                                | 7.33 ms: 1.01x faster                                                     |
| python_startup             | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                                     |
| meteor_contest             | 101 ms                                                                 | 102 ms: 1.01x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 86.0 ms: 1.01x slower                                                     |
| coverage                   | 82.5 ms                                                                | 83.1 ms: 1.01x slower                                                     |
| richards_super             | 50.4 ms                                                                | 50.8 ms: 1.01x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 725 ms: 1.01x slower                                                      |
| richards                   | 44.4 ms                                                                | 44.8 ms: 1.01x slower                                                     |
| generators                 | 28.5 ms                                                                | 28.8 ms: 1.01x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.47 sec: 1.01x slower                                                    |
| unpickle_pure_python       | 208 us                                                                 | 211 us: 1.01x slower                                                      |
| sympy_str                  | 274 ms                                                                 | 278 ms: 1.01x slower                                                      |
| thrift                     | 772 us                                                                 | 788 us: 1.02x slower                                                      |
| sympy_sum                  | 154 ms                                                                 | 158 ms: 1.02x slower                                                      |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                     |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.02x slower                                                     |
| raytrace                   | 250 ms                                                                 | 257 ms: 1.03x slower                                                      |
| gc_traversal               | 3.32 ms                                                                | 3.42 ms: 1.03x slower                                                     |
| mako                       | 11.2 ms                                                                | 11.6 ms: 1.04x slower                                                     |
| django_template            | 34.2 ms                                                                | 35.5 ms: 1.04x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 473 ms: 1.04x slower                                                      |
| xml_etree_process          | 59.2 ms                                                                | 61.8 ms: 1.04x slower                                                     |
| scimark_lu                 | 112 ms                                                                 | 118 ms: 1.05x slower                                                      |
| nbody                      | 85.3 ms                                                                | 89.6 ms: 1.05x slower                                                     |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| xml_etree_parse            | 136 ms                                                                 | 145 ms: 1.07x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 315 us: 1.08x slower                                                      |
| deltablue                  | 3.10 ms                                                                | 3.36 ms: 1.09x slower                                                     |
| regex_compile              | 131 ms                                                                 | 148 ms: 1.12x slower                                                      |
| bench_thread_pool          | 924 us                                                                 | 1.33 ms: 1.44x slower                                                     |
| telco                      | 7.77 ms                                                                | 160 ms: 20.60x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 263 ms: 23.94x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (5): logging_format, fannkuch, json, logging_simple, json_loads
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261116-3.16.0a2+dev-910a92b/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.055x faster

# HPT report

- Reliability score: 99.69% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x