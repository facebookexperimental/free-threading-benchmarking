# Results vs. 3.13.0rc2

- fork: python
- ref: cdfdf7bb73a5751ecec7
- machine: linux-x86_64
- commit hash: cdfdf7b
- commit date: 2026-10-08
- overall geometric mean: 1.074x slower
- HPT reliability: 97.26%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.90 sec: 1.10x slower                                                |
| html5lib       | 68.6 ms                                                                | 67.4 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 698 ms: 1.29x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 708 ms: 1.24x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 423 ms: 1.09x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 632 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 612 ms: 1.03x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 343 ms: 1.03x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 400 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 506 ms: 1.02x faster                                                  |
| async_generators           | 375 ms                                                                 | 421 ms: 1.12x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 27.1 ms: 1.16x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 197 ms: 1.10x faster                                                  |
| float          | 76.7 ms                                                                | 85.2 ms: 1.11x slower                                                 |
| nbody          | 85.3 ms                                                                | 117 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                                 |
| regex_effbot   | 3.21 ms                                                                | 2.98 ms: 1.08x faster                                                 |
| regex_dna      | 189 ms                                                                 | 178 ms: 1.06x faster                                                  |
| regex_compile  | 131 ms                                                                 | 169 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.99 ms: 1.06x faster                                                 |
| tomli_loads          | 2.01 sec                                                               | 1.96 sec: 1.03x faster                                                |
| xml_etree_iterparse  | 94.4 ms                                                                | 96.1 ms: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 140 ms: 1.03x slower                                                  |
| json_loads           | 27.3 us                                                                | 30.5 us: 1.12x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 75.5 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.70 ms: 1.31x slower                                                 |
| python_startup         | 11.0 ms                                                                | 16.3 ms: 1.48x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.39x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 41.5 ms: 1.21x slower                                                 |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.31x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 131 ms: 2.43x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.88x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.30 sec: 1.79x faster                                                |
| bench_mp_pool              | 11.0 ms                                                                | 6.75 ms: 1.63x faster                                                 |
| deepcopy                   | 357 us                                                                 | 266 us: 1.34x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 698 ms: 1.29x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 708 ms: 1.24x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 1.91 us: 1.17x faster                                                 |
| go                         | 141 ms                                                                 | 120 ms: 1.17x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 32.9 us: 1.16x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 121 ms: 1.11x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                                 |
| pidigits                   | 216 ms                                                                 | 197 ms: 1.10x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 423 ms: 1.09x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.98 ms: 1.08x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.91 us: 1.07x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 18.1 ms: 1.06x faster                                                 |
| json_dumps                 | 10.6 ms                                                                | 9.99 ms: 1.06x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 327 ms: 1.06x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 146 us: 1.06x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 70.1 ms: 1.06x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 178 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 632 ms: 1.05x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 103 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 612 ms: 1.03x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 343 ms: 1.03x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.96 sec: 1.03x faster                                                |
| async_tree_memoization_tg  | 410 ms                                                                 | 400 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 506 ms: 1.02x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 67.4 ms: 1.02x faster                                                 |
| pyflate                    | 449 ms                                                                 | 443 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.44 sec: 1.00x faster                                                |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.01x slower                                                |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 96.1 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.86 ms: 1.02x slower                                                 |
| xml_etree_parse            | 136 ms                                                                 | 140 ms: 1.03x slower                                                  |
| chaos                      | 56.3 ms                                                                | 59.6 ms: 1.06x slower                                                 |
| json                       | 4.98 ms                                                                | 5.41 ms: 1.08x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 107 ns: 1.09x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.90 sec: 1.10x slower                                                |
| sympy_integrate            | 19.7 ms                                                                | 21.8 ms: 1.11x slower                                                 |
| comprehensions             | 16.6 us                                                                | 18.4 us: 1.11x slower                                                 |
| float                      | 76.7 ms                                                                | 85.2 ms: 1.11x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.5 us: 1.12x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 87.2 ms: 1.12x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.69 ms: 1.12x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 808 ms: 1.12x slower                                                  |
| async_generators           | 375 ms                                                                 | 421 ms: 1.12x slower                                                  |
| 2to3                       | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.67 sec: 1.15x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 316 ms: 1.15x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.09 us: 1.15x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.99 us: 1.16x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 130 ms: 1.16x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 27.1 ms: 1.16x slower                                                 |
| raytrace                   | 250 ms                                                                 | 291 ms: 1.16x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 529 ms: 1.17x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 180 ms: 1.17x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.9 ms: 1.17x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| richards                   | 44.4 ms                                                                | 53.1 ms: 1.20x slower                                                 |
| richards_super             | 50.4 ms                                                                | 60.7 ms: 1.20x slower                                                 |
| thrift                     | 772 us                                                                 | 936 us: 1.21x slower                                                  |
| django_template            | 34.2 ms                                                                | 41.5 ms: 1.21x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.77 ms: 1.22x slower                                                 |
| generators                 | 28.5 ms                                                                | 35.1 ms: 1.23x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 465 ms: 1.24x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 75.5 ms: 1.27x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 87.1 ms: 1.28x slower                                                 |
| regex_compile              | 131 ms                                                                 | 169 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.70 ms: 1.31x slower                                                 |
| nbody                      | 85.3 ms                                                                | 117 ms: 1.37x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                 |
| coverage                   | 82.5 ms                                                                | 117 ms: 1.42x slower                                                  |
| python_startup             | 11.0 ms                                                                | 16.3 ms: 1.48x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.64 ms: 1.77x slower                                                 |
| telco                      | 7.77 ms                                                                | 176 ms: 22.69x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x slower

# HPT report

- Reliability score: 97.26% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x