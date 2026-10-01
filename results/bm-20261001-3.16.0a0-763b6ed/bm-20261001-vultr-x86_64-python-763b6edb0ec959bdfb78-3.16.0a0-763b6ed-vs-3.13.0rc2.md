# Results vs. 3.13.0rc2

- fork: python
- ref: 763b6edb0ec959bdfb78
- machine: linux-x86_64
- commit hash: 763b6ed
- commit date: 2026-10-01
- overall geometric mean: 1.030x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 259 ms: 1.00x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.38 sec: 1.11x faster                                                |
| html5lib       | 68.6 ms                                                                | 58.8 ms: 1.17x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 754 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 561 ms: 1.19x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 400 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 552 ms: 1.15x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 771 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 363 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 296 ms: 1.13x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 328 ms: 1.08x faster                                                  |
| async_generators           | 375 ms                                                                 | 349 ms: 1.07x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 187 ms: 1.15x faster                                                  |
| float          | 76.7 ms                                                                | 72.2 ms: 1.06x faster                                                 |
| nbody          | 85.3 ms                                                                | 89.1 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.64 ms: 1.22x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.07x faster                                                 |
| regex_dna      | 189 ms                                                                 | 178 ms: 1.06x faster                                                  |
| regex_compile  | 131 ms                                                                 | 148 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.34 ms: 1.14x faster                                                 |
| tomli_loads          | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.6 ms: 1.02x faster                                                 |
| json_loads           | 27.3 us                                                                | 27.5 us: 1.01x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 211 us: 1.01x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 88.1 ms: 1.03x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 301 us: 1.03x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 62.2 ms: 1.05x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 145 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.74 ms: 1.04x slower                                                 |
| python_startup         | 11.0 ms                                                                | 12.9 ms: 1.17x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                 |
| django_template | 34.2 ms                                                                | 36.9 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.08x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 113 ms: 2.80x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.05x faster                                                |
| deepcopy                   | 357 us                                                                 | 230 us: 1.55x faster                                                  |
| go                         | 141 ms                                                                 | 103 ms: 1.37x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.0 us: 1.36x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 118 us: 1.32x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 107 ms: 1.24x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.64 ms: 1.22x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.57 us: 1.22x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 754 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 561 ms: 1.19x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 90.8 ms: 1.18x faster                                                 |
| pyflate                    | 449 ms                                                                 | 380 ms: 1.18x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 58.8 ms: 1.17x faster                                                 |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.15x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 400 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 552 ms: 1.15x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 771 ms: 1.14x faster                                                  |
| json_dumps                 | 10.6 ms                                                                | 9.34 ms: 1.14x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 308 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 363 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 296 ms: 1.13x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.38 sec: 1.11x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 68.1 ms: 1.09x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                |
| pathlib                    | 19.3 ms                                                                | 17.7 ms: 1.09x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 328 ms: 1.08x faster                                                  |
| async_generators           | 375 ms                                                                 | 349 ms: 1.07x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.07x faster                                                 |
| chaos                      | 56.3 ms                                                                | 52.7 ms: 1.07x faster                                                 |
| float                      | 76.7 ms                                                                | 72.2 ms: 1.06x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 178 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.20 sec: 1.06x faster                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.49 ms: 1.06x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.64 ms: 1.06x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.8 us: 1.05x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 74.3 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.1 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.0 ms: 1.04x faster                                                 |
| logging_silent             | 98.2 ns                                                                | 95.3 ns: 1.03x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.74 us: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.6 ms: 1.02x faster                                                 |
| logging_simple             | 6.14 us                                                                | 6.04 us: 1.02x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 100.0 ms: 1.01x faster                                                |
| richards                   | 44.4 ms                                                                | 43.8 ms: 1.01x faster                                                 |
| generators                 | 28.5 ms                                                                | 28.2 ms: 1.01x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.6 ms: 1.01x faster                                                 |
| raytrace                   | 250 ms                                                                 | 248 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                                |
| 2to3                       | 259 ms                                                                 | 259 ms: 1.00x faster                                                  |
| sympy_str                  | 274 ms                                                                 | 275 ms: 1.00x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 155 ms: 1.01x slower                                                  |
| json_loads                 | 27.3 us                                                                | 27.5 us: 1.01x slower                                                 |
| coverage                   | 82.5 ms                                                                | 83.2 ms: 1.01x slower                                                 |
| json                       | 4.98 ms                                                                | 5.04 ms: 1.01x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 211 us: 1.01x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 729 ms: 1.01x slower                                                  |
| thrift                     | 772 us                                                                 | 788 us: 1.02x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 467 ms: 1.03x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.50 sec: 1.03x slower                                                |
| xml_etree_generate         | 85.4 ms                                                                | 88.1 ms: 1.03x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 301 us: 1.03x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 117 ms: 1.04x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 7.74 ms: 1.04x slower                                                 |
| nbody                      | 85.3 ms                                                                | 89.1 ms: 1.04x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 62.2 ms: 1.05x slower                                                 |
| xml_etree_parse            | 136 ms                                                                 | 145 ms: 1.06x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.31 ms: 1.07x slower                                                 |
| mako                       | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                 |
| django_template            | 34.2 ms                                                                | 36.9 ms: 1.08x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 3.72 ms: 1.12x slower                                                 |
| regex_compile              | 131 ms                                                                 | 148 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                                | 12.9 ms: 1.17x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.67 ms: 1.25x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                 |
| telco                      | 7.77 ms                                                                | 160 ms: 20.56x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 253 ms: 23.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (3): fannkuch, richards_super, sqlite_synth
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x