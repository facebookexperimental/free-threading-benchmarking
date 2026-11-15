# Results vs. 3.13.0rc2

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: linux-x86_64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.063x slower
- HPT reliability: 91.34%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 290 ms: 1.12x slower                                                      |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                                    |
| html5lib       | 68.6 ms                                                                | 67.2 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 699 ms: 1.29x faster                                                      |
| async_generators           | 375 ms                                                                 | 294 ms: 1.27x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 720 ms: 1.22x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 575 ms: 1.16x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 564 ms: 1.12x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 411 ms: 1.12x faster                                                      |
| asyncio_tcp                | 502 ms                                                                 | 454 ms: 1.11x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 397 ms: 1.03x faster                                                      |
| asyncio_websockets         | 517 ms                                                                 | 502 ms: 1.03x faster                                                      |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.57 sec: 1.04x slower                                                    |
| coroutines                 | 23.3 ms                                                                | 26.0 ms: 1.11x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.09x faster                                                              |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 192 ms: 1.12x faster                                                      |
| float          | 76.7 ms                                                                | 84.3 ms: 1.10x slower                                                     |
| nbody          | 85.3 ms                                                                | 117 ms: 1.37x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 19.9 ms: 1.16x faster                                                     |
| regex_effbot   | 3.21 ms                                                                | 2.83 ms: 1.13x faster                                                     |
| regex_dna      | 189 ms                                                                 | 169 ms: 1.11x faster                                                      |
| regex_compile  | 131 ms                                                                 | 171 ms: 1.30x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 10.2 ms: 1.04x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.99 sec: 1.01x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 96.4 ms: 1.02x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                                      |
| pickle_dict          | 32.7 us                                                                | 35.5 us: 1.08x slower                                                     |
| pickle               | 11.4 us                                                                | 12.6 us: 1.10x slower                                                     |
| json_loads           | 27.3 us                                                                | 30.9 us: 1.13x slower                                                     |
| unpickle             | 14.6 us                                                                | 16.7 us: 1.15x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 98.4 ms: 1.15x slower                                                     |
| unpickle_pure_python | 208 us                                                                 | 242 us: 1.16x slower                                                      |
| pickle_list          | 4.81 us                                                                | 5.60 us: 1.16x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 347 us: 1.19x slower                                                      |
| unpickle_list        | 4.60 us                                                                | 5.69 us: 1.24x slower                                                     |
| xml_etree_process    | 59.2 ms                                                                | 75.2 ms: 1.27x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.87 ms: 1.20x slower                                                     |
| python_startup         | 11.0 ms                                                                | 13.4 ms: 1.21x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.20x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 41.5 ms: 1.21x slower                                                     |
| mako            | 11.2 ms                                                                | 16.1 ms: 1.43x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.32x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 116 ms: 2.73x faster                                                      |
| gc_traversal               | 3.32 ms                                                                | 1.81 ms: 1.83x faster                                                     |
| mdp                        | 2.34 sec                                                               | 1.29 sec: 1.81x faster                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 6.65 ms: 1.65x faster                                                     |
| deepcopy                   | 357 us                                                                 | 268 us: 1.34x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 699 ms: 1.29x faster                                                      |
| async_generators           | 375 ms                                                                 | 294 ms: 1.27x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 720 ms: 1.22x faster                                                      |
| regex_v8                   | 23.2 ms                                                                | 19.9 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 575 ms: 1.16x faster                                                      |
| go                         | 141 ms                                                                 | 121 ms: 1.16x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 136 us: 1.15x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 33.3 us: 1.14x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.83 ms: 1.13x faster                                                     |
| pidigits                   | 216 ms                                                                 | 192 ms: 1.12x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 564 ms: 1.12x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 411 ms: 1.12x faster                                                      |
| regex_dna                  | 189 ms                                                                 | 169 ms: 1.11x faster                                                      |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                     |
| asyncio_tcp                | 502 ms                                                                 | 454 ms: 1.11x faster                                                      |
| scimark_sor                | 134 ms                                                                 | 121 ms: 1.10x faster                                                      |
| pathlib                    | 19.3 ms                                                                | 18.2 ms: 1.06x faster                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 2.95 us: 1.06x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.26 sec: 1.05x faster                                                    |
| dulwich_log                | 74.5 ms                                                                | 71.5 ms: 1.04x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                      |
| scimark_fft                | 348 ms                                                                 | 335 ms: 1.04x faster                                                      |
| json_dumps                 | 10.6 ms                                                                | 10.2 ms: 1.04x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 104 ms: 1.03x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 397 ms: 1.03x faster                                                      |
| asyncio_websockets         | 517 ms                                                                 | 502 ms: 1.03x faster                                                      |
| html5lib                   | 68.6 ms                                                                | 67.2 ms: 1.02x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.99 sec: 1.01x faster                                                    |
| pyflate                    | 449 ms                                                                 | 451 ms: 1.00x slower                                                      |
| xml_etree_iterparse        | 94.4 ms                                                                | 96.4 ms: 1.02x slower                                                     |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.57 sec: 1.04x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                                    |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                                      |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.07 ms: 1.07x slower                                                     |
| comprehensions             | 16.6 us                                                                | 17.9 us: 1.08x slower                                                     |
| pickle_dict                | 32.7 us                                                                | 35.5 us: 1.08x slower                                                     |
| json                       | 4.98 ms                                                                | 5.45 ms: 1.09x slower                                                     |
| chaos                      | 56.3 ms                                                                | 61.5 ms: 1.09x slower                                                     |
| float                      | 76.7 ms                                                                | 84.3 ms: 1.10x slower                                                     |
| hexiom                     | 5.95 ms                                                                | 6.56 ms: 1.10x slower                                                     |
| pickle                     | 11.4 us                                                                | 12.6 us: 1.10x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 21.9 ms: 1.11x slower                                                     |
| coroutines                 | 23.3 ms                                                                | 26.0 ms: 1.11x slower                                                     |
| 2to3                       | 259 ms                                                                 | 290 ms: 1.12x slower                                                      |
| nqueens                    | 77.7 ms                                                                | 87.4 ms: 1.12x slower                                                     |
| json_loads                 | 27.3 us                                                                | 30.9 us: 1.13x slower                                                     |
| logging_silent             | 98.2 ns                                                                | 112 ns: 1.14x slower                                                      |
| logging_simple             | 6.14 us                                                                | 7.02 us: 1.14x slower                                                     |
| unpickle                   | 14.6 us                                                                | 16.7 us: 1.15x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 824 ms: 1.15x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 98.4 ms: 1.15x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 242 us: 1.16x slower                                                      |
| pickle_list                | 4.81 us                                                                | 5.60 us: 1.16x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.70 sec: 1.16x slower                                                    |
| scimark_lu                 | 112 ms                                                                 | 131 ms: 1.17x slower                                                      |
| logging_format             | 6.92 us                                                                | 8.09 us: 1.17x slower                                                     |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.1 ms: 1.17x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 321 ms: 1.17x slower                                                      |
| sympy_expand               | 454 ms                                                                 | 537 ms: 1.18x slower                                                      |
| generators                 | 28.5 ms                                                                | 33.8 ms: 1.18x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 183 ms: 1.19x slower                                                      |
| raytrace                   | 250 ms                                                                 | 296 ms: 1.19x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 347 us: 1.19x slower                                                      |
| deltablue                  | 3.10 ms                                                                | 3.69 ms: 1.19x slower                                                     |
| thrift                     | 772 us                                                                 | 921 us: 1.19x slower                                                      |
| python_startup_no_site     | 7.41 ms                                                                | 8.87 ms: 1.20x slower                                                     |
| richards                   | 44.4 ms                                                                | 53.1 ms: 1.20x slower                                                     |
| richards_super             | 50.4 ms                                                                | 60.7 ms: 1.20x slower                                                     |
| python_startup             | 11.0 ms                                                                | 13.4 ms: 1.21x slower                                                     |
| django_template            | 34.2 ms                                                                | 41.5 ms: 1.21x slower                                                     |
| unpickle_list              | 4.60 us                                                                | 5.69 us: 1.24x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.24x slower                                                      |
| fannkuch                   | 376 ms                                                                 | 471 ms: 1.25x slower                                                      |
| xml_etree_process          | 59.2 ms                                                                | 75.2 ms: 1.27x slower                                                     |
| unpack_sequence            | 39.3 ns                                                                | 49.9 ns: 1.27x slower                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 87.9 ms: 1.29x slower                                                     |
| regex_compile              | 131 ms                                                                 | 171 ms: 1.30x slower                                                      |
| nbody                      | 85.3 ms                                                                | 117 ms: 1.37x slower                                                      |
| mako                       | 11.2 ms                                                                | 16.1 ms: 1.43x slower                                                     |
| coverage                   | 82.5 ms                                                                | 119 ms: 1.44x slower                                                      |
| bench_thread_pool          | 924 us                                                                 | 1.41 ms: 1.53x slower                                                     |
| telco                      | 7.77 ms                                                                | 175 ms: 22.45x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                              |

Benchmark hidden because not significant (2): create_gc_cycles, async_tree_none_tg
Ignored benchmarks (12) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20261114-3.16.0a2+dev-edd6f76-NOGIL/bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.063x slower

# HPT report

- Reliability score: 91.34% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x