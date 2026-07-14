# Results vs. 3.13.0rc2

- fork: python
- ref: 832bc0b0ea20c2fade5d
- machine: linux-x86_64
- commit hash: 832bc0b
- commit date: 2026-07-12
- overall geometric mean: 1.077x slower
- HPT reliability: 99.85%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| docutils       | 2.63 sec                                                               | 3.00 sec: 1.14x slower                                                |
| html5lib       | 68.6 ms                                                                | 66.8 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 681 ms: 1.32x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 706 ms: 1.25x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 419 ms: 1.10x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 396 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 325 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 698 ms: 1.05x slower                                                  |
| async_generators           | 375 ms                                                                 | 392 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 676 ms: 1.07x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 25.0 ms: 1.07x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 225 ms: 1.04x slower                                                  |
| float          | 76.7 ms                                                                | 84.6 ms: 1.10x slower                                                 |
| nbody          | 85.3 ms                                                                | 127 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.19x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 20.3 ms: 1.14x faster                                                 |
| regex_effbot   | 3.21 ms                                                                | 2.88 ms: 1.11x faster                                                 |
| regex_dna      | 189 ms                                                                 | 179 ms: 1.05x faster                                                  |
| regex_compile  | 131 ms                                                                 | 168 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.98 sec: 1.02x faster                                                |
| json_dumps           | 10.6 ms                                                                | 10.6 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 95.2 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 141 ms: 1.04x slower                                                  |
| json_loads           | 27.3 us                                                                | 29.9 us: 1.10x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 239 us: 1.15x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 341 us: 1.17x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 74.2 ms: 1.25x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.23 ms: 1.24x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.32x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 39.7 ms: 1.16x slower                                                 |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 131 ms: 2.42x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.76 ms: 1.89x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                                |
| bench_mp_pool              | 11.0 ms                                                                | 6.92 ms: 1.59x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 681 ms: 1.32x faster                                                  |
| deepcopy                   | 357 us                                                                 | 274 us: 1.30x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 706 ms: 1.25x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 31.7 us: 1.20x faster                                                 |
| go                         | 141 ms                                                                 | 120 ms: 1.17x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 1.96 us: 1.15x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 20.3 ms: 1.14x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.88 ms: 1.11x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 419 ms: 1.10x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 142 us: 1.10x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 123 ms: 1.08x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 17.8 ms: 1.08x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.92 us: 1.07x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 179 ms: 1.05x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 71.5 ms: 1.04x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 396 ms: 1.03x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 66.8 ms: 1.03x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 325 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.37 sec: 1.02x faster                                                |
| tomli_loads                | 2.01 sec                                                               | 1.98 sec: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| json_dumps                 | 10.6 ms                                                                | 10.6 ms: 1.01x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.2 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| scimark_fft                | 348 ms                                                                 | 351 ms: 1.01x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                 |
| pyflate                    | 449 ms                                                                 | 461 ms: 1.03x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 111 ms: 1.03x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 141 ms: 1.04x slower                                                  |
| pidigits                   | 216 ms                                                                 | 225 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 698 ms: 1.05x slower                                                  |
| async_generators           | 375 ms                                                                 | 392 ms: 1.05x slower                                                  |
| json                       | 4.98 ms                                                                | 5.31 ms: 1.06x slower                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 676 ms: 1.07x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 25.0 ms: 1.07x slower                                                 |
| comprehensions             | 16.6 us                                                                | 18.0 us: 1.08x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.9 us: 1.10x slower                                                 |
| float                      | 76.7 ms                                                                | 84.6 ms: 1.10x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 21.8 ms: 1.11x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.60 ms: 1.11x slower                                                 |
| chaos                      | 56.3 ms                                                                | 62.5 ms: 1.11x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.84 us: 1.11x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.74 us: 1.12x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 110 ns: 1.12x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 87.8 ms: 1.13x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 815 ms: 1.13x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 128 ms: 1.14x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 312 ms: 1.14x slower                                                  |
| 2to3                       | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| docutils                   | 2.63 sec                                                               | 3.00 sec: 1.14x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 239 us: 1.15x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.48 ms: 1.15x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 524 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.69 sec: 1.16x slower                                                |
| generators                 | 28.5 ms                                                                | 33.1 ms: 1.16x slower                                                 |
| django_template            | 34.2 ms                                                                | 39.7 ms: 1.16x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 180 ms: 1.17x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 341 us: 1.17x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| thrift                     | 772 us                                                                 | 913 us: 1.18x slower                                                  |
| richards_super             | 50.4 ms                                                                | 59.9 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 78.8 ms: 1.20x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.71 ms: 1.20x slower                                                 |
| richards                   | 44.4 ms                                                                | 53.9 ms: 1.21x slower                                                 |
| raytrace                   | 250 ms                                                                 | 304 ms: 1.22x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 465 ms: 1.24x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.23 ms: 1.24x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 74.2 ms: 1.25x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                  |
| regex_compile              | 131 ms                                                                 | 168 ms: 1.28x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 89.3 ms: 1.31x slower                                                 |
| coverage                   | 82.5 ms                                                                | 114 ms: 1.39x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                 |
| nbody                      | 85.3 ms                                                                | 127 ms: 1.48x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.47 ms: 1.59x slower                                                 |
| telco                      | 7.77 ms                                                                | 173 ms: 22.30x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260712-3.16.0a0-832bc0b-NOGIL/bm-20260712-vultr-x86_64-python-832bc0b0ea20c2fade5d-3.16.0a0-832bc0b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 99.85% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.35x