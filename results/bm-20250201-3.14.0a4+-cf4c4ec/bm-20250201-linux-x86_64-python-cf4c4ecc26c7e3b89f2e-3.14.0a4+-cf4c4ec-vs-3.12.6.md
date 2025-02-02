# Results vs. 3.12.6

- fork: python
- ref: cf4c4ecc26c7e3b89f2e
- machine: linux-x86_64
- commit hash: cf4c4ec
- commit date: 2025-02-01
- overall geometric mean: 1.096x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.54 sec: 1.13x faster                                                 |
| html5lib       | 88.9 ms                                                | 84.0 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 909 ms: 2.13x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 890 ms: 2.08x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 467 ms: 1.99x faster                                                   |
| async_tree_none            | 741 ms                                                 | 386 ms: 1.92x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 514 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 387 ms: 1.82x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 682 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 732 ms: 1.50x faster                                                   |
| async_generators           | 589 ms                                                 | 535 ms: 1.10x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 724 ms: 1.03x faster                                                   |
| asyncio_tcp                | 923 ms                                                 | 966 ms: 1.05x slower                                                   |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                           |

Benchmark hidden because not significant (1): asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 106 ms: 1.16x faster                                                   |
| pidigits       | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 126 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.29 ms: 1.20x faster                                                  |
| regex_compile  | 187 ms                                                 | 164 ms: 1.14x faster                                                   |
| regex_dna      | 278 ms                                                 | 268 ms: 1.04x faster                                                   |
| regex_v8       | 32.5 ms                                                | 35.8 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 195 ms: 1.24x faster                                                   |
| xml_etree_generate  | 127 ms                                                 | 112 ms: 1.13x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.61 sec: 1.11x faster                                                 |
| unpickle            | 21.2 us                                                | 19.4 us: 1.10x faster                                                  |
| pickle_dict         | 52.7 us                                                | 48.1 us: 1.10x faster                                                  |
| xml_etree_process   | 83.7 ms                                                | 79.4 ms: 1.05x faster                                                  |
| json_dumps          | 14.3 ms                                                | 16.0 ms: 1.12x slower                                                  |
| pickle_list         | 6.97 us                                                | 7.83 us: 1.12x slower                                                  |
| unpickle_list       | 6.83 us                                                | 7.73 us: 1.13x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (4): json_loads, unpickle_pure_python, pickle_pure_python, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 16.0 ms: 1.10x faster                                                  |
| python_startup         | 23.7 ms                                                | 28.0 ms: 1.18x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 15.7 ms                                                | 16.6 ms: 1.06x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 71.9 ms: 1.06x slower                                                  |
| django_template | 44.9 ms                                                | 51.1 ms: 1.14x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 909 ms: 2.13x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 890 ms: 2.08x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 467 ms: 1.99x faster                                                   |
| async_tree_none            | 741 ms                                                 | 386 ms: 1.92x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 514 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 387 ms: 1.82x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 682 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 732 ms: 1.50x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 38.8 us: 1.35x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.4 us: 1.27x faster                                                  |
| deepcopy                   | 468 us                                                 | 373 us: 1.25x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 195 ms: 1.24x faster                                                   |
| logging_simple             | 9.45 us                                                | 7.68 us: 1.23x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 178 ms: 1.23x faster                                                   |
| spectral_norm              | 156 ms                                                 | 128 ms: 1.21x faster                                                   |
| raytrace                   | 408 ms                                                 | 339 ms: 1.20x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.29 ms: 1.20x faster                                                  |
| float                      | 123 ms                                                 | 106 ms: 1.16x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 92.8 ms: 1.16x faster                                                  |
| regex_compile              | 187 ms                                                 | 164 ms: 1.14x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.78 sec: 1.14x faster                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 84.6 ms: 1.14x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 112 ms: 1.13x faster                                                   |
| pylint                     | 465 ms                                                 | 411 ms: 1.13x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.54 sec: 1.13x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.59 sec: 1.12x faster                                                 |
| sqlglot_normalize          | 157 ms                                                 | 140 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.14 ms: 1.11x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.61 sec: 1.11x faster                                                 |
| async_generators           | 589 ms                                                 | 535 ms: 1.10x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 16.0 ms: 1.10x faster                                                  |
| scimark_sor                | 167 ms                                                 | 151 ms: 1.10x faster                                                   |
| scimark_fft                | 500 ms                                                 | 455 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.10 ms: 1.10x faster                                                  |
| unpickle                   | 21.2 us                                                | 19.4 us: 1.10x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.53 us: 1.10x faster                                                  |
| pickle_dict                | 52.7 us                                                | 48.1 us: 1.10x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.66 sec: 1.08x faster                                                 |
| logging_format             | 9.59 us                                                | 8.87 us: 1.08x faster                                                  |
| go                         | 172 ms                                                 | 160 ms: 1.07x faster                                                   |
| sympy_integrate            | 29.8 ms                                                | 27.9 ms: 1.07x faster                                                  |
| chaos                      | 84.9 ms                                                | 79.5 ms: 1.07x faster                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 71.4 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.86 sec: 1.06x faster                                                 |
| typing_runtime_protocols   | 224 us                                                 | 211 us: 1.06x faster                                                   |
| nqueens                    | 117 ms                                                 | 110 ms: 1.06x faster                                                   |
| html5lib                   | 88.9 ms                                                | 84.0 ms: 1.06x faster                                                  |
| sympy_str                  | 385 ms                                                 | 364 ms: 1.06x faster                                                   |
| xml_etree_process          | 83.7 ms                                                | 79.4 ms: 1.05x faster                                                  |
| pyflate                    | 727 ms                                                 | 698 ms: 1.04x faster                                                   |
| pprint_safe_repr           | 967 ms                                                 | 930 ms: 1.04x faster                                                   |
| pidigits                   | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| regex_dna                  | 278 ms                                                 | 268 ms: 1.04x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 724 ms: 1.03x faster                                                   |
| asyncio_tcp                | 923 ms                                                 | 966 ms: 1.05x slower                                                   |
| richards                   | 60.3 ms                                                | 63.2 ms: 1.05x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 160 ms: 1.05x slower                                                   |
| coroutines                 | 29.5 ms                                                | 31.0 ms: 1.05x slower                                                  |
| nbody                      | 119 ms                                                 | 126 ms: 1.05x slower                                                   |
| hexiom                     | 8.27 ms                                                | 8.73 ms: 1.06x slower                                                  |
| mako                       | 15.7 ms                                                | 16.6 ms: 1.06x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 71.9 ms: 1.06x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.13 ms: 1.07x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 240 ms: 1.08x slower                                                   |
| deltablue                  | 4.27 ms                                                | 4.62 ms: 1.08x slower                                                  |
| json                       | 6.85 ms                                                | 7.47 ms: 1.09x slower                                                  |
| telco                      | 9.59 ms                                                | 10.5 ms: 1.09x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 35.8 ms: 1.10x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.0 ms: 1.12x slower                                                  |
| pickle_list                | 6.97 us                                                | 7.83 us: 1.12x slower                                                  |
| unpickle_list              | 6.83 us                                                | 7.73 us: 1.13x slower                                                  |
| django_template            | 44.9 ms                                                | 51.1 ms: 1.14x slower                                                  |
| python_startup             | 23.7 ms                                                | 28.0 ms: 1.18x slower                                                  |
| unpack_sequence            | 60.2 ns                                                | 74.1 ns: 1.23x slower                                                  |
| coverage                   | 95.4 ms                                                | 132 ms: 1.39x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.19 ms: 1.40x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.68 ms: 1.90x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 96.1 ms: 4.64x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (19): pathlib, sqlglot_parse, fannkuch, genshi_text, generators, logging_silent, dulwich_log, richards_super, asyncio_tcp_ssl, json_loads, unpickle_pure_python, sqlalchemy_imperative, sqlglot_transpile, sympy_expand, deepcopy_reduce, 2to3, pickle_pure_python, pickle, meteor_contest
Ignored benchmarks (7) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
Ignored benchmarks (6) of results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x