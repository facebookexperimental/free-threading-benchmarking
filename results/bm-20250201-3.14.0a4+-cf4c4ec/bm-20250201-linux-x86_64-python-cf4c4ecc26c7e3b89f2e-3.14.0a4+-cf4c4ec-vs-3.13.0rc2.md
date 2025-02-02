# Results vs. 3.13.0rc2

- fork: python
- ref: cf4c4ecc26c7e3b89f2e
- machine: linux-x86_64
- commit hash: cf4c4ec
- commit date: 2025-02-01
- overall geometric mean: 1.055x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.54 sec: 1.13x faster                                                 |
| html5lib       | 92.6 ms                                                      | 84.0 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 890 ms: 1.56x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 909 ms: 1.54x faster                                                   |
| async_tree_none            | 572 ms                                                       | 386 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 467 ms: 1.44x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 514 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 682 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 387 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 732 ms: 1.16x faster                                                   |
| async_generators           | 567 ms                                                       | 535 ms: 1.06x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 724 ms: 1.06x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                           |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, coroutines, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 106 ms: 1.09x faster                                                   |
| nbody          | 119 ms                                                       | 126 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 164 ms: 1.11x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.29 ms: 1.10x faster                                                  |
| regex_dna      | 282 ms                                                       | 268 ms: 1.05x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 35.8 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 231 ms                                                       | 195 ms: 1.19x faster                                                   |
| xml_etree_iterparse | 177 ms                                                       | 151 ms: 1.17x faster                                                   |
| xml_etree_generate  | 122 ms                                                       | 112 ms: 1.09x faster                                                   |
| xml_etree_process   | 85.9 ms                                                      | 79.4 ms: 1.08x faster                                                  |
| tomli_loads         | 2.78 sec                                                     | 2.61 sec: 1.07x faster                                                 |
| unpickle            | 20.5 us                                                      | 19.4 us: 1.06x faster                                                  |
| pickle_pure_python  | 416 us                                                       | 451 us: 1.08x slower                                                   |
| json_loads          | 34.3 us                                                      | 37.4 us: 1.09x slower                                                  |
| pickle              | 15.1 us                                                      | 17.0 us: 1.12x slower                                                  |
| json_dumps          | 14.1 ms                                                      | 16.0 ms: 1.13x slower                                                  |
| pickle_list         | 6.86 us                                                      | 7.83 us: 1.14x slower                                                  |
| unpickle_list       | 6.68 us                                                      | 7.73 us: 1.16x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): pickle_dict, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 16.0 ms: 1.04x slower                                                  |
| python_startup         | 22.4 ms                                                      | 28.0 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 29.1 ms: 1.09x faster                                                  |
| mako            | 15.9 ms                                                      | 16.6 ms: 1.04x slower                                                  |
| django_template | 44.3 ms                                                      | 51.1 ms: 1.15x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 890 ms: 1.56x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 909 ms: 1.54x faster                                                   |
| async_tree_none            | 572 ms                                                       | 386 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 467 ms: 1.44x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 514 ms: 1.38x faster                                                   |
| deepcopy                   | 498 us                                                       | 373 us: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 682 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 387 ms: 1.30x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 38.8 us: 1.29x faster                                                  |
| spectral_norm              | 157 ms                                                       | 128 ms: 1.22x faster                                                   |
| go                         | 191 ms                                                       | 160 ms: 1.19x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 195 ms: 1.19x faster                                                   |
| scimark_sor                | 179 ms                                                       | 151 ms: 1.18x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 151 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 732 ms: 1.16x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.5 ms: 1.16x faster                                                  |
| pylint                     | 470 ms                                                       | 411 ms: 1.14x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.54 sec: 1.13x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.53 us: 1.13x faster                                                  |
| logging_simple             | 8.56 us                                                      | 7.68 us: 1.11x faster                                                  |
| regex_compile              | 182 ms                                                       | 164 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.10 ms: 1.11x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.29 ms: 1.10x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 84.0 ms: 1.10x faster                                                  |
| xml_etree_generate         | 122 ms                                                       | 112 ms: 1.09x faster                                                   |
| float                      | 116 ms                                                       | 106 ms: 1.09x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.78 sec: 1.09x faster                                                 |
| genshi_text                | 31.7 ms                                                      | 29.1 ms: 1.09x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 27.9 ms: 1.09x faster                                                  |
| xml_etree_process          | 85.9 ms                                                      | 79.4 ms: 1.08x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 92.8 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 84.6 ms: 1.07x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 211 us: 1.07x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.61 sec: 1.07x faster                                                 |
| async_generators           | 567 ms                                                       | 535 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 930 ms: 1.06x faster                                                   |
| unpickle                   | 20.5 us                                                      | 19.4 us: 1.06x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 724 ms: 1.06x faster                                                   |
| chaos                      | 83.6 ms                                                      | 79.5 ms: 1.05x faster                                                  |
| fannkuch                   | 547 ms                                                       | 521 ms: 1.05x faster                                                   |
| regex_dna                  | 282 ms                                                       | 268 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.94 sec                                                     | 1.86 sec: 1.04x faster                                                 |
| logging_format             | 9.24 us                                                      | 8.87 us: 1.04x faster                                                  |
| comprehensions             | 22.2 us                                                      | 21.4 us: 1.04x faster                                                  |
| scimark_fft                | 473 ms                                                       | 455 ms: 1.04x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.66 sec: 1.04x faster                                                 |
| logging_silent             | 130 ns                                                       | 135 ns: 1.04x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 4.62 ms: 1.04x slower                                                  |
| mako                       | 15.9 ms                                                      | 16.6 ms: 1.04x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 16.0 ms: 1.04x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 98.0 ms: 1.05x slower                                                  |
| pyflate                    | 664 ms                                                       | 698 ms: 1.05x slower                                                   |
| nbody                      | 119 ms                                                       | 126 ms: 1.06x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.36 ms: 1.07x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 8.73 ms: 1.08x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 451 us: 1.08x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.14 ms: 1.09x slower                                                  |
| json_loads                 | 34.3 us                                                      | 37.4 us: 1.09x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 160 ms: 1.09x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 35.8 ms: 1.09x slower                                                  |
| pickle                     | 15.1 us                                                      | 17.0 us: 1.12x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.0 ms: 1.13x slower                                                  |
| pickle_list                | 6.86 us                                                      | 7.83 us: 1.14x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 240 ms: 1.14x slower                                                   |
| json                       | 6.51 ms                                                      | 7.47 ms: 1.15x slower                                                  |
| django_template            | 44.3 ms                                                      | 51.1 ms: 1.15x slower                                                  |
| unpickle_list              | 6.68 us                                                      | 7.73 us: 1.16x slower                                                  |
| coverage                   | 107 ms                                                       | 132 ms: 1.23x slower                                                   |
| python_startup             | 22.4 ms                                                      | 28.0 ms: 1.25x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.19 ms: 1.44x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.68 ms: 1.52x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 96.1 ms: 5.14x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (24): sqlglot_optimize, pidigits, sympy_str, richards, richards_super, sympy_expand, sqlglot_parse, raytrace, nqueens, generators, deepcopy_reduce, unpack_sequence, genshi_xml, asyncio_tcp_ssl, sqlglot_normalize, coroutines, pathlib, meteor_contest, pycparser, asyncio_tcp, pickle_dict, unpickle_pure_python, thrift, 2to3
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
Ignored benchmarks (8) of results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.055x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x