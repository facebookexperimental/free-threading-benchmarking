# Results vs. 3.13.0rc2

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.038x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                  |
| html5lib       | 67.0 ms                                                      | 63.4 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 638 ms: 1.43x faster                                                  |
| async_tree_io              | 876 ms                                                       | 618 ms: 1.42x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 534 ms: 1.19x faster                                                  |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.52 sec: 1.00x slower                                                |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                          |

Benchmark hidden because not significant (1): asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 65.0 ms: 1.19x faster                                                 |
| nbody          | 85.1 ms                                                      | 86.9 ms: 1.02x slower                                                 |
| pidigits       | 217 ms                                                       | 230 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                 |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.77 sec: 1.13x faster                                                |
| unpickle_pure_python | 210 us                                                       | 189 us: 1.11x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 54.1 ms: 1.10x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 78.3 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| unpickle             | 14.3 us                                                      | 14.0 us: 1.02x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.4 ms: 1.02x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 33.0 us: 1.01x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.03x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.27 us: 1.07x slower                                                 |
| json_loads           | 27.0 us                                                      | 29.0 us: 1.07x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.11 us: 1.08x slower                                                 |
| pickle               | 11.3 us                                                      | 12.6 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.7 ms: 1.06x faster                                                 |
| genshi_text     | 21.5 ms                                                      | 20.4 ms: 1.05x faster                                                 |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 49.6 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.03x faster                                                |
| richards                   | 45.2 ms                                                      | 29.7 ms: 1.52x faster                                                 |
| richards_super             | 51.6 ms                                                      | 34.3 ms: 1.51x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 638 ms: 1.43x faster                                                  |
| async_tree_io              | 876 ms                                                       | 618 ms: 1.42x faster                                                  |
| deepcopy                   | 355 us                                                       | 256 us: 1.39x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.3 us: 1.33x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| spectral_norm              | 111 ms                                                       | 84.9 ms: 1.31x faster                                                 |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                  |
| go                         | 141 ms                                                       | 111 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                  |
| scimark_fft                | 349 ms                                                       | 282 ms: 1.24x faster                                                  |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 534 ms: 1.19x faster                                                  |
| float                      | 77.5 ms                                                      | 65.0 ms: 1.19x faster                                                 |
| pyflate                    | 449 ms                                                       | 389 ms: 1.15x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.74 us: 1.13x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.77 sec: 1.13x faster                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 3.97 sec: 1.12x faster                                                |
| pylint                     | 317 ms                                                       | 285 ms: 1.11x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 189 us: 1.11x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.7 ms: 1.10x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 2.83 ms: 1.10x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 54.1 ms: 1.10x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 78.3 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 59.9 ms: 1.09x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 692 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                |
| html5lib                   | 67.0 ms                                                      | 63.4 ms: 1.06x faster                                                 |
| mako                       | 11.3 ms                                                      | 10.7 ms: 1.06x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.4 ms: 1.05x faster                                                 |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                  |
| meteor_contest             | 102 ms                                                       | 98.1 ms: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                 |
| logging_silent             | 103 ns                                                       | 100.0 ns: 1.03x faster                                                |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.03x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                 |
| unpickle                   | 14.3 us                                                      | 14.0 us: 1.02x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.87 ms: 1.02x faster                                                 |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.4 ms: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.64 ms: 1.01x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.8 ms: 1.01x faster                                                 |
| thrift                     | 778 us                                                       | 768 us: 1.01x faster                                                  |
| logging_simple             | 6.16 us                                                      | 6.11 us: 1.01x faster                                                 |
| fannkuch                   | 370 ms                                                       | 367 ms: 1.01x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.3 us: 1.01x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.9 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.52 sec: 1.00x slower                                                |
| crypto_pyaes               | 67.9 ms                                                      | 68.1 ms: 1.00x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                 |
| generators                 | 28.8 ms                                                      | 29.2 ms: 1.01x slower                                                 |
| raytrace                   | 253 ms                                                       | 256 ms: 1.01x slower                                                  |
| pickle_dict                | 32.5 us                                                      | 33.0 us: 1.01x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.5 ms: 1.02x slower                                                 |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 49.6 ms: 1.02x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.02x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| nbody                      | 85.1 ms                                                      | 86.9 ms: 1.02x slower                                                 |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.15 sec: 1.03x slower                                                |
| sympy_expand               | 457 ms                                                       | 473 ms: 1.03x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.22 ms: 1.06x slower                                                 |
| pidigits                   | 217 ms                                                       | 230 ms: 1.06x slower                                                  |
| pickle_list                | 4.93 us                                                      | 5.27 us: 1.07x slower                                                 |
| json_loads                 | 27.0 us                                                      | 29.0 us: 1.07x slower                                                 |
| unpack_sequence            | 44.8 ns                                                      | 48.3 ns: 1.08x slower                                                 |
| unpickle_list              | 4.71 us                                                      | 5.11 us: 1.08x slower                                                 |
| pickle                     | 11.3 us                                                      | 12.6 us: 1.11x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.15x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.96 ms: 1.47x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.73 ms: 1.50x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.37x slower                                                  |
| telco                      | 7.82 ms                                                      | 156 ms: 19.99x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (6): asyncio_tcp, sympy_sum, docutils, nqueens, logging_format, sympy_str
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.038x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x