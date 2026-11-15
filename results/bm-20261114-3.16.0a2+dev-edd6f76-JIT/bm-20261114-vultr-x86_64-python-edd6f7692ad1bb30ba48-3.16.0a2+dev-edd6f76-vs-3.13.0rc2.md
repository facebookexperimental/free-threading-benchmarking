# Results vs. 3.13.0rc2

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: linux-x86_64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.168x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 250 ms: 1.04x faster                                                      |
| docutils       | 2.63 sec                                                               | 2.39 sec: 1.10x faster                                                    |
| html5lib       | 68.6 ms                                                                | 57.1 ms: 1.20x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators           | 375 ms                                                                 | 242 ms: 1.55x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 620 ms: 1.42x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 324 ms: 1.42x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 255 ms: 1.39x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 652 ms: 1.38x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 487 ms: 1.37x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 318 ms: 1.29x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 260 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                      |
| asyncio_tcp                | 502 ms                                                                 | 441 ms: 1.14x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 22.6 ms: 1.03x faster                                                     |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.47 sec: 1.03x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 85.3 ms                                                                | 59.6 ms: 1.43x faster                                                     |
| float          | 76.7 ms                                                                | 54.6 ms: 1.40x faster                                                     |
| pidigits       | 216 ms                                                                 | 177 ms: 1.22x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.35x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.56 ms: 1.26x faster                                                     |
| regex_dna      | 189 ms                                                                 | 159 ms: 1.18x faster                                                      |
| regex_v8       | 23.2 ms                                                                | 19.8 ms: 1.17x faster                                                     |
| regex_compile  | 131 ms                                                                 | 143 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.48 sec: 1.36x faster                                                    |
| json_dumps           | 10.6 ms                                                                | 8.42 ms: 1.26x faster                                                     |
| unpickle_pure_python | 208 us                                                                 | 171 us: 1.22x faster                                                      |
| pickle_pure_python   | 292 us                                                                 | 271 us: 1.08x faster                                                      |
| json_loads           | 27.3 us                                                                | 25.5 us: 1.07x faster                                                     |
| xml_etree_process    | 59.2 ms                                                                | 55.8 ms: 1.06x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 80.8 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 94.4 ms                                                                | 89.8 ms: 1.05x faster                                                     |
| unpickle             | 14.6 us                                                                | 14.3 us: 1.02x faster                                                     |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                                      |
| pickle_dict          | 32.7 us                                                                | 35.0 us: 1.07x slower                                                     |
| unpickle_list        | 4.60 us                                                                | 4.98 us: 1.08x slower                                                     |
| pickle               | 11.4 us                                                                | 12.7 us: 1.11x slower                                                     |
| pickle_list          | 4.81 us                                                                | 5.71 us: 1.19x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.04x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.44 ms: 1.00x slower                                                     |
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 9.90 ms: 1.13x faster                                                     |
| django_template | 34.2 ms                                                                | 32.2 ms: 1.06x faster                                                     |
| Geometric mean  | (ref)                                                                  | 1.10x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 107 ms: 2.97x faster                                                      |
| richards_super             | 50.4 ms                                                                | 20.6 ms: 2.44x faster                                                     |
| richards                   | 44.4 ms                                                                | 19.2 ms: 2.31x faster                                                     |
| mdp                        | 2.34 sec                                                               | 1.16 sec: 2.02x faster                                                    |
| scimark_sor                | 134 ms                                                                 | 78.2 ms: 1.71x faster                                                     |
| deepcopy                   | 357 us                                                                 | 219 us: 1.63x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 23.8 us: 1.60x faster                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 99.2 us: 1.57x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 68.7 ms: 1.57x faster                                                     |
| async_generators           | 375 ms                                                                 | 242 ms: 1.55x faster                                                      |
| nbody                      | 85.3 ms                                                                | 59.6 ms: 1.43x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 620 ms: 1.42x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 324 ms: 1.42x faster                                                      |
| go                         | 141 ms                                                                 | 99.8 ms: 1.41x faster                                                     |
| float                      | 76.7 ms                                                                | 54.6 ms: 1.40x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 255 ms: 1.39x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 652 ms: 1.38x faster                                                      |
| scimark_fft                | 348 ms                                                                 | 254 ms: 1.37x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 487 ms: 1.37x faster                                                      |
| tomli_loads                | 2.01 sec                                                               | 1.48 sec: 1.36x faster                                                    |
| scimark_lu                 | 112 ms                                                                 | 85.3 ms: 1.32x faster                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 2.41 us: 1.30x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 318 ms: 1.29x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 260 ms: 1.28x faster                                                      |
| pyflate                    | 449 ms                                                                 | 351 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 52.0 ms: 1.27x faster                                                     |
| json_dumps                 | 10.6 ms                                                                | 8.42 ms: 1.26x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.56 ms: 1.26x faster                                                     |
| logging_silent             | 98.2 ns                                                                | 78.4 ns: 1.25x faster                                                     |
| pidigits                   | 216 ms                                                                 | 177 ms: 1.22x faster                                                      |
| unpickle_pure_python       | 208 us                                                                 | 171 us: 1.22x faster                                                      |
| html5lib                   | 68.6 ms                                                                | 57.1 ms: 1.20x faster                                                     |
| nqueens                    | 77.7 ms                                                                | 64.9 ms: 1.20x faster                                                     |
| comprehensions             | 16.6 us                                                                | 13.9 us: 1.19x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 159 ms: 1.18x faster                                                      |
| pprint_safe_repr           | 719 ms                                                                 | 607 ms: 1.18x faster                                                      |
| chaos                      | 56.3 ms                                                                | 47.7 ms: 1.18x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 19.8 ms: 1.17x faster                                                     |
| deltablue                  | 3.10 ms                                                                | 2.65 ms: 1.17x faster                                                     |
| logging_format             | 6.92 us                                                                | 5.95 us: 1.16x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 3.85 sec: 1.16x faster                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.14 ms: 1.15x faster                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.27 sec: 1.15x faster                                                    |
| logging_simple             | 6.14 us                                                                | 5.38 us: 1.14x faster                                                     |
| fannkuch                   | 376 ms                                                                 | 330 ms: 1.14x faster                                                      |
| asyncio_tcp                | 502 ms                                                                 | 441 ms: 1.14x faster                                                      |
| mako                       | 11.2 ms                                                                | 9.90 ms: 1.13x faster                                                     |
| pathlib                    | 19.3 ms                                                                | 17.1 ms: 1.13x faster                                                     |
| docutils                   | 2.63 sec                                                               | 2.39 sec: 1.10x faster                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 62.7 ms: 1.09x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 68.5 ms: 1.09x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.08 us: 1.08x faster                                                     |
| json                       | 4.98 ms                                                                | 4.63 ms: 1.08x faster                                                     |
| pickle_pure_python         | 292 us                                                                 | 271 us: 1.08x faster                                                      |
| json_loads                 | 27.3 us                                                                | 25.5 us: 1.07x faster                                                     |
| xml_etree_process          | 59.2 ms                                                                | 55.8 ms: 1.06x faster                                                     |
| django_template            | 34.2 ms                                                                | 32.2 ms: 1.06x faster                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 80.8 ms: 1.06x faster                                                     |
| hexiom                     | 5.95 ms                                                                | 5.66 ms: 1.05x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.8 ms: 1.05x faster                                                     |
| 2to3                       | 259 ms                                                                 | 250 ms: 1.04x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 22.6 ms: 1.03x faster                                                     |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.47 sec: 1.03x faster                                                    |
| unpickle                   | 14.6 us                                                                | 14.3 us: 1.02x faster                                                     |
| meteor_contest             | 101 ms                                                                 | 99.2 ms: 1.02x faster                                                     |
| raytrace                   | 250 ms                                                                 | 248 ms: 1.01x faster                                                      |
| python_startup_no_site     | 7.41 ms                                                                | 7.44 ms: 1.00x slower                                                     |
| python_startup             | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 19.9 ms: 1.01x slower                                                     |
| coverage                   | 82.5 ms                                                                | 84.0 ms: 1.02x slower                                                     |
| pycparser                  | 1.12 sec                                                               | 1.15 sec: 1.02x slower                                                    |
| generators                 | 28.5 ms                                                                | 29.4 ms: 1.03x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 468 ms: 1.03x slower                                                      |
| create_gc_cycles           | 1.33 ms                                                                | 1.40 ms: 1.05x slower                                                     |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                                      |
| sympy_str                  | 274 ms                                                                 | 292 ms: 1.07x slower                                                      |
| pickle_dict                | 32.7 us                                                                | 35.0 us: 1.07x slower                                                     |
| unpickle_list              | 4.60 us                                                                | 4.98 us: 1.08x slower                                                     |
| regex_compile              | 131 ms                                                                 | 143 ms: 1.09x slower                                                      |
| sympy_sum                  | 154 ms                                                                 | 168 ms: 1.09x slower                                                      |
| gc_traversal               | 3.32 ms                                                                | 3.62 ms: 1.09x slower                                                     |
| pickle                     | 11.4 us                                                                | 12.7 us: 1.11x slower                                                     |
| pickle_list                | 4.81 us                                                                | 5.71 us: 1.19x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.31 ms: 1.42x slower                                                     |
| unpack_sequence            | 39.3 ns                                                                | 63.9 ns: 1.63x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 183 ms: 16.61x slower                                                     |
| telco                      | 7.77 ms                                                                | 134 ms: 17.27x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.10x faster                                                              |

Benchmark hidden because not significant (1): thrift
Ignored benchmarks (12) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20261114-3.16.0a2+dev-edd6f76-JIT/bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.168x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.14x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.18x