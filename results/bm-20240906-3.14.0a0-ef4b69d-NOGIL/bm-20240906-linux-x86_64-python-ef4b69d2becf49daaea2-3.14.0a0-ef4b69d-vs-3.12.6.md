# Results vs. 3.12.6

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 719 ms: 1.58x slower                                                  |
| docutils       | 4.00 sec                                               | 4.96 sec: 1.24x slower                                                |
| html5lib       | 88.9 ms                                                | 139 ms: 1.56x slower                                                  |
| tornado_http   | 266 ms                                                 | 350 ms: 1.32x slower                                                  |
| Geometric mean | (ref)                                                  | 1.42x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.65x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 660 ms: 1.41x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.34 sec: 1.37x faster                                                |
| async_tree_none_tg         | 704 ms                                                 | 514 ms: 1.37x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 747 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 863 ms: 1.28x faster                                                  |
| async_tree_none            | 741 ms                                                 | 610 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 952 ms: 1.13x faster                                                  |
| async_generators           | 589 ms                                                 | 734 ms: 1.25x slower                                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.56 sec: 1.27x slower                                                |
| asyncio_tcp                | 923 ms                                                 | 1.22 sec: 1.32x slower                                                |
| coroutines                 | 29.5 ms                                                | 41.7 ms: 1.41x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 204 ms: 1.66x slower                                                  |
| nbody          | 119 ms                                                 | 300 ms: 2.52x slower                                                  |
| Geometric mean | (ref)                                                  | 1.61x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 294 ms: 1.06x slower                                                  |
| regex_v8       | 32.5 ms                                                | 37.7 ms: 1.16x slower                                                 |
| regex_compile  | 187 ms                                                 | 284 ms: 1.52x slower                                                  |
| Geometric mean | (ref)                                                  | 1.15x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 40.9 us: 1.29x faster                                                 |
| xml_etree_parse      | 241 ms                                                 | 215 ms: 1.12x faster                                                  |
| pickle_list          | 6.97 us                                                | 6.59 us: 1.06x faster                                                 |
| unpickle_list        | 6.83 us                                                | 7.20 us: 1.05x slower                                                 |
| json_loads           | 37.9 us                                                | 44.0 us: 1.16x slower                                                 |
| json_dumps           | 14.3 ms                                                | 18.1 ms: 1.26x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 163 ms: 1.28x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 4.30 sec: 1.49x slower                                                |
| xml_etree_process    | 83.7 ms                                                | 128 ms: 1.53x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 550 us: 1.83x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 870 us: 2.00x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.18x slower                                                          |

Benchmark hidden because not significant (3): pickle, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.5 ms: 1.22x slower                                                 |
| python_startup         | 23.7 ms                                                | 32.8 ms: 1.38x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 55.1 ms: 1.82x slower                                                 |
| django_template | 44.9 ms                                                | 85.9 ms: 1.91x slower                                                 |
| mako            | 15.7 ms                                                | 30.1 ms: 1.91x slower                                                 |
| genshi_xml      | 67.6 ms                                                | 129 ms: 1.92x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.89x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.65x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 660 ms: 1.41x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.34 sec: 1.37x faster                                                |
| async_tree_none_tg         | 704 ms                                                 | 514 ms: 1.37x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 747 ms: 1.31x faster                                                  |
| pickle_dict                | 52.7 us                                                | 40.9 us: 1.29x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 863 ms: 1.28x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 4.60 ms: 1.27x faster                                                 |
| async_tree_none            | 741 ms                                                 | 610 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 952 ms: 1.13x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 215 ms: 1.12x faster                                                  |
| pickle_list                | 6.97 us                                                | 6.59 us: 1.06x faster                                                 |
| unpickle_list              | 6.83 us                                                | 7.20 us: 1.05x slower                                                 |
| regex_dna                  | 278 ms                                                 | 294 ms: 1.06x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.12 ms: 1.09x slower                                                 |
| regex_v8                   | 32.5 ms                                                | 37.7 ms: 1.16x slower                                                 |
| json_loads                 | 37.9 us                                                | 44.0 us: 1.16x slower                                                 |
| pathlib                    | 31.6 ms                                                | 37.2 ms: 1.18x slower                                                 |
| json                       | 6.85 ms                                                | 8.10 ms: 1.18x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.60 us: 1.19x slower                                                 |
| deepcopy                   | 468 us                                                 | 568 us: 1.21x slower                                                  |
| pycparser                  | 1.79 sec                                               | 2.18 sec: 1.22x slower                                                |
| python_startup_no_site     | 17.6 ms                                                | 21.5 ms: 1.22x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.96 sec: 1.24x slower                                                |
| async_generators           | 589 ms                                                 | 734 ms: 1.25x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 18.1 ms: 1.26x slower                                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.56 sec: 1.27x slower                                                |
| xml_etree_generate         | 127 ms                                                 | 163 ms: 1.28x slower                                                  |
| deepcopy_memo              | 52.4 us                                                | 67.4 us: 1.29x slower                                                 |
| scimark_fft                | 500 ms                                                 | 652 ms: 1.30x slower                                                  |
| mdp                        | 3.97 sec                                               | 5.18 sec: 1.30x slower                                                |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.80 ms: 1.31x slower                                                 |
| tornado_http               | 266 ms                                                 | 350 ms: 1.32x slower                                                  |
| asyncio_tcp                | 923 ms                                                 | 1.22 sec: 1.32x slower                                                |
| generators                 | 41.1 ms                                                | 54.6 ms: 1.33x slower                                                 |
| pylint                     | 465 ms                                                 | 625 ms: 1.34x slower                                                  |
| meteor_contest             | 146 ms                                                 | 199 ms: 1.36x slower                                                  |
| comprehensions             | 27.1 us                                                | 37.3 us: 1.38x slower                                                 |
| python_startup             | 23.7 ms                                                | 32.8 ms: 1.38x slower                                                 |
| coroutines                 | 29.5 ms                                                | 41.7 ms: 1.41x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 156 ms: 1.45x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 5.97 us: 1.48x slower                                                 |
| pyflate                    | 727 ms                                                 | 1.08 sec: 1.48x slower                                                |
| nqueens                    | 117 ms                                                 | 174 ms: 1.49x slower                                                  |
| tomli_loads                | 2.88 sec                                               | 4.30 sec: 1.49x slower                                                |
| dulwich_log                | 100 ms                                                 | 152 ms: 1.52x slower                                                  |
| regex_compile              | 187 ms                                                 | 284 ms: 1.52x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 128 ms: 1.53x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 240 ms: 1.53x slower                                                  |
| telco                      | 9.59 ms                                                | 14.7 ms: 1.53x slower                                                 |
| fannkuch                   | 540 ms                                                 | 831 ms: 1.54x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.2 sec: 1.56x slower                                                |
| html5lib                   | 88.9 ms                                                | 139 ms: 1.56x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 5.45 ms: 1.57x slower                                                 |
| typing_runtime_protocols   | 224 us                                                 | 353 us: 1.57x slower                                                  |
| 2to3                       | 456 ms                                                 | 719 ms: 1.58x slower                                                  |
| spectral_norm              | 156 ms                                                 | 249 ms: 1.60x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.70 ms: 1.61x slower                                                 |
| logging_format             | 9.59 us                                                | 15.5 us: 1.61x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 48.3 ms: 1.62x slower                                                 |
| coverage                   | 95.4 ms                                                | 157 ms: 1.64x slower                                                  |
| float                      | 123 ms                                                 | 204 ms: 1.66x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 160 ms: 1.66x slower                                                  |
| richards_super             | 72.8 ms                                                | 123 ms: 1.69x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 130 ms: 1.71x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.68 sec: 1.74x slower                                                |
| pprint_pformat             | 1.98 sec                                               | 3.48 sec: 1.76x slower                                                |
| sympy_str                  | 385 ms                                                 | 696 ms: 1.81x slower                                                  |
| genshi_text                | 30.2 ms                                                | 55.1 ms: 1.82x slower                                                 |
| unpickle_pure_python       | 300 us                                                 | 550 us: 1.83x slower                                                  |
| raytrace                   | 408 ms                                                 | 751 ms: 1.84x slower                                                  |
| logging_silent             | 139 ns                                                 | 260 ns: 1.86x slower                                                  |
| logging_simple             | 9.45 us                                                | 17.7 us: 1.88x slower                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 4.43 ms: 1.90x slower                                                 |
| richards                   | 60.3 ms                                                | 114 ms: 1.90x slower                                                  |
| django_template            | 44.9 ms                                                | 85.9 ms: 1.91x slower                                                 |
| mako                       | 15.7 ms                                                | 30.1 ms: 1.91x slower                                                 |
| genshi_xml                 | 67.6 ms                                                | 129 ms: 1.92x slower                                                  |
| hexiom                     | 8.27 ms                                                | 16.4 ms: 1.98x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 870 us: 2.00x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 305 ms: 2.00x slower                                                  |
| scimark_sor                | 167 ms                                                 | 340 ms: 2.04x slower                                                  |
| chaos                      | 84.9 ms                                                | 176 ms: 2.08x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.72 ms: 2.08x slower                                                 |
| go                         | 172 ms                                                 | 361 ms: 2.10x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 492 ms: 2.22x slower                                                  |
| sympy_expand               | 582 ms                                                 | 1.33 sec: 2.29x slower                                                |
| nbody                      | 119 ms                                                 | 300 ms: 2.52x slower                                                  |
| deltablue                  | 4.27 ms                                                | 11.3 ms: 2.66x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 180 ns: 2.99x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.39x slower                                                          |

Benchmark hidden because not significant (7): pickle, regex_effbot, pidigits, asyncio_websockets, xml_etree_iterparse, unpickle, bench_mp_pool
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.15x