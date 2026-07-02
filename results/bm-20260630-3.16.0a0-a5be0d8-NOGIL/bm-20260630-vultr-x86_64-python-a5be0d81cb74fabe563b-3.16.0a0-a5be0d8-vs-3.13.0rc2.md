# Results vs. 3.13.0rc2

- fork: python
- ref: a5be0d81cb74fabe563b
- machine: linux-x86_64
- commit hash: a5be0d8
- commit date: 2026-06-30
- overall geometric mean: 1.068x slower
- HPT reliability: 97.35%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 294 ms: 1.13x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.95 sec: 1.12x slower                                                |
| html5lib       | 68.6 ms                                                                | 65.9 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 684 ms: 1.32x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 703 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 601 ms: 1.11x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 418 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 581 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 394 ms: 1.04x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 324 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 388 ms: 1.03x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 25.1 ms: 1.07x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 180 ms: 1.20x faster                                                  |
| float          | 76.7 ms                                                                | 86.3 ms: 1.13x slower                                                 |
| nbody          | 85.3 ms                                                                | 127 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 20.5 ms: 1.13x faster                                                 |
| regex_effbot   | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                                 |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.04x faster                                                  |
| regex_compile  | 131 ms                                                                 | 167 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.94 sec: 1.04x faster                                                |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 95.0 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 141 ms: 1.04x slower                                                  |
| json_loads           | 27.3 us                                                                | 30.1 us: 1.10x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 235 us: 1.13x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 98.7 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 73.9 ms: 1.25x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.14 ms: 1.23x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.31x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 40.2 ms: 1.18x slower                                                 |
| mako            | 11.2 ms                                                                | 16.2 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 131 ms: 2.42x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.87x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                                |
| bench_mp_pool              | 11.0 ms                                                                | 6.91 ms: 1.59x faster                                                 |
| deepcopy                   | 357 us                                                                 | 262 us: 1.36x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 684 ms: 1.32x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 703 ms: 1.25x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 30.6 us: 1.25x faster                                                 |
| pidigits                   | 216 ms                                                                 | 180 ms: 1.20x faster                                                  |
| go                         | 141 ms                                                                 | 121 ms: 1.16x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 1.94 us: 1.16x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 20.5 ms: 1.13x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 601 ms: 1.11x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 418 ms: 1.10x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.86 us: 1.09x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 581 ms: 1.09x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 143 us: 1.09x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 17.8 ms: 1.08x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 125 ms: 1.07x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 70.8 ms: 1.05x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 65.9 ms: 1.04x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 394 ms: 1.04x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.94 sec: 1.04x faster                                                |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 324 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.35 sec: 1.03x faster                                                |
| json_dumps                 | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.12 sec: 1.00x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.0 ms: 1.01x slower                                                 |
| pyflate                    | 449 ms                                                                 | 461 ms: 1.03x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.03x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 359 ms: 1.03x slower                                                  |
| async_generators           | 375 ms                                                                 | 388 ms: 1.03x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 141 ms: 1.04x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.05x slower                                                  |
| json                       | 4.98 ms                                                                | 5.27 ms: 1.06x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 105 ns: 1.07x slower                                                  |
| comprehensions             | 16.6 us                                                                | 17.7 us: 1.07x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 25.1 ms: 1.07x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.1 us: 1.10x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 21.7 ms: 1.10x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.60 ms: 1.11x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 799 ms: 1.11x slower                                                  |
| chaos                      | 56.3 ms                                                                | 62.6 ms: 1.11x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.95 sec: 1.12x slower                                                |
| float                      | 76.7 ms                                                                | 86.3 ms: 1.13x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 87.7 ms: 1.13x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 235 us: 1.13x slower                                                  |
| 2to3                       | 259 ms                                                                 | 294 ms: 1.13x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.66 sec: 1.14x slower                                                |
| sympy_str                  | 274 ms                                                                 | 312 ms: 1.14x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.01 us: 1.14x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.91 us: 1.14x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 129 ms: 1.15x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 523 ms: 1.15x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 98.7 ms: 1.16x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.53 ms: 1.16x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 181 ms: 1.17x slower                                                  |
| generators                 | 28.5 ms                                                                | 33.5 ms: 1.17x slower                                                 |
| richards                   | 44.4 ms                                                                | 52.1 ms: 1.17x slower                                                 |
| thrift                     | 772 us                                                                 | 905 us: 1.17x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.2 ms: 1.18x slower                                                 |
| richards_super             | 50.4 ms                                                                | 59.6 ms: 1.18x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.72 ms: 1.20x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 457 ms: 1.22x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 80.1 ms: 1.22x slower                                                 |
| raytrace                   | 250 ms                                                                 | 305 ms: 1.22x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.22x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.14 ms: 1.23x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 73.9 ms: 1.25x slower                                                 |
| regex_compile              | 131 ms                                                                 | 167 ms: 1.27x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 88.9 ms: 1.30x slower                                                 |
| coverage                   | 82.5 ms                                                                | 113 ms: 1.37x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                                 |
| mako                       | 11.2 ms                                                                | 16.2 ms: 1.45x slower                                                 |
| nbody                      | 85.3 ms                                                                | 127 ms: 1.49x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.47 ms: 1.59x slower                                                 |
| telco                      | 7.77 ms                                                                | 174 ms: 22.43x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                          |
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260630-3.16.0a0-a5be0d8-NOGIL/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.068x slower

# HPT report

- Reliability score: 97.35% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x