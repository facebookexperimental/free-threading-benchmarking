# Results vs. 3.13.0rc2

- fork: python
- ref: 832bc0b0ea20c2fade5d
- machine: linux-x86_64
- commit hash: 832bc0b
- commit date: 2026-07-12
- overall geometric mean: 1.032x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 257 ms: 1.01x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.40 sec: 1.10x faster                                                |
| html5lib       | 68.6 ms                                                                | 58.0 ms: 1.18x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 715 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 541 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 373 ms: 1.23x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 290 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 754 ms: 1.19x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 360 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 558 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 295 ms: 1.13x faster                                                  |
| async_generators           | 375 ms                                                                 | 341 ms: 1.10x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 199 ms: 1.09x faster                                                  |
| float          | 76.7 ms                                                                | 75.9 ms: 1.01x faster                                                 |
| nbody          | 85.3 ms                                                                | 96.9 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.60 ms: 1.24x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                                 |
| regex_dna      | 189 ms                                                                 | 178 ms: 1.06x faster                                                  |
| regex_compile  | 131 ms                                                                 | 148 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.83 sec: 1.10x faster                                                |
| json_dumps           | 10.6 ms                                                                | 9.72 ms: 1.09x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 89.6 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 86.4 ms: 1.01x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 212 us: 1.02x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 60.8 ms: 1.03x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 312 us: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.02 ms: 1.06x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.4 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 35.4 ms: 1.04x slower                                                 |
| mako            | 11.2 ms                                                                | 12.0 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 114 ms: 2.77x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.06x faster                                                |
| deepcopy                   | 357 us                                                                 | 235 us: 1.52x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.6 us: 1.43x faster                                                 |
| go                         | 141 ms                                                                 | 102 ms: 1.37x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 117 us: 1.33x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 108 ms: 1.24x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.60 ms: 1.24x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 715 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 541 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 373 ms: 1.23x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 290 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.56 us: 1.22x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 754 ms: 1.19x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 58.0 ms: 1.18x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 360 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 558 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 295 ms: 1.13x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 95.4 ms: 1.13x faster                                                 |
| pyflate                    | 449 ms                                                                 | 400 ms: 1.12x faster                                                  |
| async_generators           | 375 ms                                                                 | 341 ms: 1.10x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.83 sec: 1.10x faster                                                |
| docutils                   | 2.63 sec                                                               | 2.40 sec: 1.10x faster                                                |
| json_dumps                 | 10.6 ms                                                                | 9.72 ms: 1.09x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 68.2 ms: 1.09x faster                                                 |
| pidigits                   | 216 ms                                                                 | 199 ms: 1.09x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 323 ms: 1.08x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 17.9 ms: 1.07x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 178 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.20 sec: 1.06x faster                                                |
| python_startup_no_site     | 7.41 ms                                                                | 7.02 ms: 1.06x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.6 ms: 1.05x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.1 ms: 1.05x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 74.3 ms: 1.05x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.69 ms: 1.05x faster                                                 |
| comprehensions             | 16.6 us                                                                | 16.0 us: 1.04x faster                                                 |
| richards                   | 44.4 ms                                                                | 42.9 ms: 1.04x faster                                                 |
| richards_super             | 50.4 ms                                                                | 48.7 ms: 1.03x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.1 ms: 1.03x faster                                                 |
| chaos                      | 56.3 ms                                                                | 54.6 ms: 1.03x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.75 us: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.64 ms: 1.02x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 64.4 ms: 1.02x faster                                                 |
| logging_simple             | 6.14 us                                                                | 6.03 us: 1.02x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.22 us: 1.01x faster                                                 |
| float                      | 76.7 ms                                                                | 75.9 ms: 1.01x faster                                                 |
| 2to3                       | 259 ms                                                                 | 257 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 714 ms: 1.01x faster                                                  |
| logging_silent             | 98.2 ns                                                                | 97.7 ns: 1.01x faster                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.45 sec: 1.00x faster                                                |
| scimark_lu                 | 112 ms                                                                 | 113 ms: 1.00x slower                                                  |
| json                       | 4.98 ms                                                                | 5.04 ms: 1.01x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 103 ms: 1.01x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 86.4 ms: 1.01x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 381 ms: 1.01x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 462 ms: 1.02x slower                                                  |
| raytrace                   | 250 ms                                                                 | 254 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 212 us: 1.02x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 158 ms: 1.02x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 69.8 ms: 1.02x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 60.8 ms: 1.03x slower                                                 |
| thrift                     | 772 us                                                                 | 798 us: 1.03x slower                                                  |
| django_template            | 34.2 ms                                                                | 35.4 ms: 1.04x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.26 ms: 1.05x slower                                                 |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 312 us: 1.07x slower                                                  |
| mako                       | 11.2 ms                                                                | 12.0 ms: 1.07x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.4 ms: 1.12x slower                                                 |
| regex_compile              | 131 ms                                                                 | 148 ms: 1.13x slower                                                  |
| nbody                      | 85.3 ms                                                                | 96.9 ms: 1.14x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.03 ms: 1.21x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.68 ms: 1.26x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                 |
| telco                      | 7.77 ms                                                                | 157 ms: 20.20x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 233 ms: 21.16x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (4): pycparser, json_loads, coverage, sympy_str
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260712-3.16.0a0-832bc0b/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x