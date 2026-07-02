# Results vs. 3.13.0rc2

- fork: python
- ref: a5be0d81cb74fabe563b
- machine: linux-x86_64
- commit hash: a5be0d8
- commit date: 2026-06-30
- overall geometric mean: 1.040x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 258 ms: 1.01x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.37 sec: 1.11x faster                                                |
| html5lib       | 68.6 ms                                                                | 59.4 ms: 1.15x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 537 ms: 1.24x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 374 ms: 1.23x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 717 ms: 1.23x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 753 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 552 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 362 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 296 ms: 1.12x faster                                                  |
| async_generators           | 375 ms                                                                 | 339 ms: 1.10x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 184 ms: 1.18x faster                                                  |
| float          | 76.7 ms                                                                | 73.7 ms: 1.04x faster                                                 |
| nbody          | 85.3 ms                                                                | 93.8 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.54 ms: 1.27x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                 |
| regex_dna      | 189 ms                                                                 | 178 ms: 1.06x faster                                                  |
| regex_compile  | 131 ms                                                                 | 147 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.80 sec: 1.12x faster                                                |
| json_dumps           | 10.6 ms                                                                | 9.95 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 88.8 ms: 1.06x faster                                                 |
| json_loads           | 27.3 us                                                                | 27.0 us: 1.01x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 210 us: 1.01x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 60.5 ms: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 6.94 ms: 1.07x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 35.1 ms: 1.03x slower                                                 |
| mako            | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 114 ms: 2.79x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.07x faster                                                |
| deepcopy                   | 357 us                                                                 | 229 us: 1.56x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.5 us: 1.44x faster                                                 |
| go                         | 141 ms                                                                 | 103 ms: 1.36x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 116 us: 1.34x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.54 ms: 1.27x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 107 ms: 1.25x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.51 us: 1.25x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 537 ms: 1.24x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 374 ms: 1.23x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 717 ms: 1.23x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 753 ms: 1.20x faster                                                  |
| pidigits                   | 216 ms                                                                 | 184 ms: 1.18x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 92.9 ms: 1.16x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 59.4 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 552 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 362 ms: 1.13x faster                                                  |
| pyflate                    | 449 ms                                                                 | 398 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 296 ms: 1.12x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.80 sec: 1.12x faster                                                |
| docutils                   | 2.63 sec                                                               | 2.37 sec: 1.11x faster                                                |
| async_generators           | 375 ms                                                                 | 339 ms: 1.10x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 17.6 ms: 1.10x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 318 ms: 1.09x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 68.9 ms: 1.08x faster                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 6.94 ms: 1.07x faster                                                 |
| json_dumps                 | 10.6 ms                                                                | 9.95 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.8 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.20 sec: 1.06x faster                                                |
| hexiom                     | 5.95 ms                                                                | 5.61 ms: 1.06x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.9 ms: 1.06x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 178 ms: 1.06x faster                                                  |
| richards                   | 44.4 ms                                                                | 42.0 ms: 1.06x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.7 us: 1.06x faster                                                 |
| richards_super             | 50.4 ms                                                                | 48.1 ms: 1.05x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 74.4 ms: 1.04x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.64 us: 1.04x faster                                                 |
| logging_simple             | 6.14 us                                                                | 5.90 us: 1.04x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 18.9 ms: 1.04x faster                                                 |
| float                      | 76.7 ms                                                                | 73.7 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.4 ms: 1.04x faster                                                 |
| chaos                      | 56.3 ms                                                                | 54.3 ms: 1.04x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.9 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.21 us: 1.02x faster                                                 |
| json                       | 4.98 ms                                                                | 4.91 ms: 1.01x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                                |
| sympy_str                  | 274 ms                                                                 | 271 ms: 1.01x faster                                                  |
| json_loads                 | 27.3 us                                                                | 27.0 us: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.71 ms: 1.01x faster                                                 |
| coverage                   | 82.5 ms                                                                | 81.8 ms: 1.01x faster                                                 |
| 2to3                       | 259 ms                                                                 | 258 ms: 1.01x faster                                                  |
| meteor_contest             | 101 ms                                                                 | 101 ms: 1.01x faster                                                  |
| raytrace                   | 250 ms                                                                 | 251 ms: 1.00x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 155 ms: 1.01x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 457 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 210 us: 1.01x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 380 ms: 1.01x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.01x slower                                                  |
| thrift                     | 772 us                                                                 | 781 us: 1.01x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 69.1 ms: 1.01x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 99.6 ns: 1.01x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 60.5 ms: 1.02x slower                                                 |
| django_template            | 34.2 ms                                                                | 35.1 ms: 1.03x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.25 ms: 1.05x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| mako                       | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                 |
| nbody                      | 85.3 ms                                                                | 93.8 ms: 1.10x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| regex_compile              | 131 ms                                                                 | 147 ms: 1.12x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 3.79 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.65 ms: 1.23x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.33 ms: 1.44x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 216 ms: 19.63x slower                                                 |
| telco                      | 7.77 ms                                                                | 158 ms: 20.38x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): pprint_safe_repr, xml_etree_generate, pprint_pformat
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260630-3.16.0a0-a5be0d8/bm-20260630-vultr-x86_64-python-a5be0d81cb74fabe563b-3.16.0a0-a5be0d8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x