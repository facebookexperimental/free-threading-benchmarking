# Results vs. 3.12.6

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.107x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| html5lib       | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 506 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 515 ms: 1.39x faster                                                  |
| async_generators           | 384 ms                                                 | 335 ms: 1.15x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.7 ms: 1.13x faster                                                 |
| nbody          | 89.3 ms                                                | 91.1 ms: 1.02x slower                                                 |
| pidigits       | 184 ms                                                 | 205 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 82.9 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                                  |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                 |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.31 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.0 ms: 1.14x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 47.6 ms: 1.05x faster                                                 |
| django_template | 34.7 ms                                                | 33.8 ms: 1.03x faster                                                 |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 506 ms: 1.43x faster                                                  |
| deepcopy                   | 352 us                                                 | 247 us: 1.43x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.4 us: 1.42x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 515 ms: 1.39x faster                                                  |
| go                         | 139 ms                                                 | 106 ms: 1.31x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.21x faster                                                 |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                 |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 67.7 ms: 1.16x faster                                                 |
| generators                 | 32.2 ms                                                | 27.8 ms: 1.16x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.11 sec: 1.15x faster                                                |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| spectral_norm              | 110 ms                                                 | 95.9 ms: 1.15x faster                                                 |
| async_generators           | 384 ms                                                 | 335 ms: 1.15x faster                                                  |
| richards                   | 45.9 ms                                                | 40.2 ms: 1.14x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.0 ms: 1.14x faster                                                 |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.2 ms: 1.14x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                |
| float                      | 80.8 ms                                                | 71.7 ms: 1.13x faster                                                 |
| pyflate                    | 448 ms                                                 | 398 ms: 1.13x faster                                                  |
| richards_super             | 51.9 ms                                                | 46.1 ms: 1.13x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 69.2 ms: 1.11x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.5 ms: 1.10x faster                                                 |
| sympy_str                  | 292 ms                                                 | 266 ms: 1.09x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.65 ms: 1.09x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.09x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.21 ms: 1.07x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.07x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 698 ms: 1.07x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 47.6 ms: 1.05x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 755 us: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| nqueens                    | 80.1 ms                                                | 76.5 ms: 1.05x faster                                                 |
| scimark_fft                | 342 ms                                                 | 328 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                  |
| sympy_expand               | 468 ms                                                 | 449 ms: 1.04x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.9 ms: 1.03x faster                                                 |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                  |
| django_template            | 34.7 ms                                                | 33.8 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.56 us: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                 |
| logging_format             | 7.35 us                                                | 7.49 us: 1.02x slower                                                 |
| nbody                      | 89.3 ms                                                | 91.1 ms: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.31 ms: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.14 ms: 1.02x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                 |
| fannkuch                   | 372 ms                                                 | 386 ms: 1.04x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.7 us: 1.08x slower                                                 |
| pidigits                   | 184 ms                                                 | 205 ms: 1.11x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                 |
| telco                      | 6.53 ms                                                | 7.33 ms: 1.12x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.0 ms: 1.13x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.57 ms: 1.32x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.94 ms: 1.77x slower                                                 |
| logging_silent             | 109 ns                                                 | 463 ns: 4.25x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 98.4 ms: 9.11x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (2): scimark_sparse_mat_mult, asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.107x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.15x