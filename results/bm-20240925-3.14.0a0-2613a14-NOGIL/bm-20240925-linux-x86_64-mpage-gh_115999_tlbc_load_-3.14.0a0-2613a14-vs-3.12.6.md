# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 2613a14
- commit date: 2024-09-25
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 706 ms: 1.55x slower                                                 |
| docutils       | 4.00 sec                                               | 4.90 sec: 1.23x slower                                               |
| html5lib       | 88.9 ms                                                | 144 ms: 1.62x slower                                                 |
| tornado_http   | 266 ms                                                 | 370 ms: 1.39x slower                                                 |
| Geometric mean | (ref)                                                  | 1.44x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.13 sec: 1.71x faster                                               |
| async_tree_io              | 1.85 sec                                               | 1.28 sec: 1.44x faster                                               |
| async_tree_memoization_tg  | 930 ms                                                 | 693 ms: 1.34x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 530 ms: 1.33x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 740 ms: 1.32x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 851 ms: 1.29x faster                                                 |
| async_tree_none            | 741 ms                                                 | 576 ms: 1.29x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 960 ms: 1.12x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 794 ms: 1.06x slower                                                 |
| asyncio_tcp                | 923 ms                                                 | 1.11 sec: 1.21x slower                                               |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.43 sec: 1.22x slower                                               |
| coroutines                 | 29.5 ms                                                | 37.2 ms: 1.26x slower                                                |
| async_generators           | 589 ms                                                 | 747 ms: 1.27x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.12x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 241 ms: 1.04x faster                                                 |
| float          | 123 ms                                                 | 201 ms: 1.63x slower                                                 |
| nbody          | 119 ms                                                 | 275 ms: 2.31x slower                                                 |
| Geometric mean | (ref)                                                  | 1.54x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.41 ms: 1.16x faster                                                |
| regex_v8       | 32.5 ms                                                | 36.0 ms: 1.11x slower                                                |
| regex_compile  | 187 ms                                                 | 282 ms: 1.51x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                         |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 46.7 us: 1.13x faster                                                |
| xml_etree_iterparse  | 169 ms                                                 | 158 ms: 1.07x faster                                                 |
| pickle               | 16.4 us                                                | 15.3 us: 1.07x faster                                                |
| xml_etree_parse      | 241 ms                                                 | 227 ms: 1.06x faster                                                 |
| pickle_list          | 6.97 us                                                | 6.63 us: 1.05x faster                                                |
| unpickle_list        | 6.83 us                                                | 7.79 us: 1.14x slower                                                |
| json_loads           | 37.9 us                                                | 43.9 us: 1.16x slower                                                |
| json_dumps           | 14.3 ms                                                | 17.3 ms: 1.21x slower                                                |
| xml_etree_generate   | 127 ms                                                 | 157 ms: 1.23x slower                                                 |
| tomli_loads          | 2.88 sec                                               | 4.05 sec: 1.41x slower                                               |
| unpickle_pure_python | 300 us                                                 | 498 us: 1.66x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 143 ms: 1.71x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 758 us: 1.74x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.18x slower                                                         |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 22.1 ms: 1.25x slower                                                |
| python_startup         | 23.7 ms                                                | 33.7 ms: 1.42x slower                                                |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 50.8 ms: 1.68x slower                                                |
| genshi_xml      | 67.6 ms                                                | 114 ms: 1.69x slower                                                 |
| django_template | 44.9 ms                                                | 78.9 ms: 1.76x slower                                                |
| mako            | 15.7 ms                                                | 30.4 ms: 1.93x slower                                                |
| Geometric mean  | (ref)                                                  | 1.76x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.13 sec: 1.71x faster                                               |
| async_tree_io              | 1.85 sec                                               | 1.28 sec: 1.44x faster                                               |
| async_tree_memoization_tg  | 930 ms                                                 | 693 ms: 1.34x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 530 ms: 1.33x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 740 ms: 1.32x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 851 ms: 1.29x faster                                                 |
| async_tree_none            | 741 ms                                                 | 576 ms: 1.29x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.41 ms: 1.16x faster                                                |
| pickle_dict                | 52.7 us                                                | 46.7 us: 1.13x faster                                                |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 960 ms: 1.12x faster                                                 |
| bench_mp_pool              | 20.7 ms                                                | 18.5 ms: 1.12x faster                                                |
| xml_etree_iterparse        | 169 ms                                                 | 158 ms: 1.07x faster                                                 |
| pickle                     | 16.4 us                                                | 15.3 us: 1.07x faster                                                |
| xml_etree_parse            | 241 ms                                                 | 227 ms: 1.06x faster                                                 |
| pickle_list                | 6.97 us                                                | 6.63 us: 1.05x faster                                                |
| pidigits                   | 250 ms                                                 | 241 ms: 1.04x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 794 ms: 1.06x slower                                                 |
| json                       | 6.85 ms                                                | 7.39 ms: 1.08x slower                                                |
| create_gc_cycles           | 1.94 ms                                                | 2.12 ms: 1.09x slower                                                |
| scimark_fft                | 500 ms                                                 | 549 ms: 1.10x slower                                                 |
| pathlib                    | 31.6 ms                                                | 34.8 ms: 1.10x slower                                                |
| regex_v8                   | 32.5 ms                                                | 36.0 ms: 1.11x slower                                                |
| unpickle_list              | 6.83 us                                                | 7.79 us: 1.14x slower                                                |
| json_loads                 | 37.9 us                                                | 43.9 us: 1.16x slower                                                |
| deepcopy                   | 468 us                                                 | 545 us: 1.17x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 17.3 ms: 1.21x slower                                                |
| asyncio_tcp                | 923 ms                                                 | 1.11 sec: 1.21x slower                                               |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.43 sec: 1.22x slower                                               |
| docutils                   | 4.00 sec                                               | 4.90 sec: 1.23x slower                                               |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.26 ms: 1.23x slower                                                |
| xml_etree_generate         | 127 ms                                                 | 157 ms: 1.23x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.81 us: 1.24x slower                                                |
| nqueens                    | 117 ms                                                 | 145 ms: 1.24x slower                                                 |
| meteor_contest             | 146 ms                                                 | 182 ms: 1.25x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 22.1 ms: 1.25x slower                                                |
| coroutines                 | 29.5 ms                                                | 37.2 ms: 1.26x slower                                                |
| pycparser                  | 1.79 sec                                               | 2.26 sec: 1.26x slower                                               |
| async_generators           | 589 ms                                                 | 747 ms: 1.27x slower                                                 |
| pylint                     | 465 ms                                                 | 604 ms: 1.30x slower                                                 |
| typing_runtime_protocols   | 224 us                                                 | 292 us: 1.30x slower                                                 |
| mdp                        | 3.97 sec                                               | 5.17 sec: 1.30x slower                                               |
| spectral_norm              | 156 ms                                                 | 203 ms: 1.30x slower                                                 |
| deepcopy_memo              | 52.4 us                                                | 70.1 us: 1.34x slower                                                |
| deepcopy_reduce            | 4.04 us                                                | 5.41 us: 1.34x slower                                                |
| sqlglot_normalize          | 157 ms                                                 | 211 ms: 1.35x slower                                                 |
| dulwich_log                | 100 ms                                                 | 136 ms: 1.35x slower                                                 |
| generators                 | 41.1 ms                                                | 56.8 ms: 1.38x slower                                                |
| tornado_http               | 266 ms                                                 | 370 ms: 1.39x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 4.86 ms: 1.40x slower                                                |
| tomli_loads                | 2.88 sec                                               | 4.05 sec: 1.41x slower                                               |
| crypto_pyaes               | 107 ms                                                 | 151 ms: 1.41x slower                                                 |
| pyflate                    | 727 ms                                                 | 1.03 sec: 1.42x slower                                               |
| python_startup             | 23.7 ms                                                | 33.7 ms: 1.42x slower                                                |
| fannkuch                   | 540 ms                                                 | 784 ms: 1.45x slower                                                 |
| comprehensions             | 27.1 us                                                | 39.5 us: 1.46x slower                                                |
| bpe_tokeniser              | 6.59 sec                                               | 9.77 sec: 1.48x slower                                               |
| telco                      | 9.59 ms                                                | 14.4 ms: 1.50x slower                                                |
| regex_compile              | 187 ms                                                 | 282 ms: 1.51x slower                                                 |
| coverage                   | 95.4 ms                                                | 145 ms: 1.52x slower                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 116 ms: 1.53x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 45.5 ms: 1.53x slower                                                |
| 2to3                       | 456 ms                                                 | 706 ms: 1.55x slower                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 152 ms: 1.57x slower                                                 |
| thrift                     | 1.06 ms                                                | 1.68 ms: 1.58x slower                                                |
| pprint_pformat             | 1.98 sec                                               | 3.16 sec: 1.60x slower                                               |
| html5lib                   | 88.9 ms                                                | 144 ms: 1.62x slower                                                 |
| float                      | 123 ms                                                 | 201 ms: 1.63x slower                                                 |
| pprint_safe_repr           | 967 ms                                                 | 1.60 sec: 1.65x slower                                               |
| logging_simple             | 9.45 us                                                | 15.6 us: 1.66x slower                                                |
| unpickle_pure_python       | 300 us                                                 | 498 us: 1.66x slower                                                 |
| richards_super             | 72.8 ms                                                | 122 ms: 1.67x slower                                                 |
| genshi_text                | 30.2 ms                                                | 50.8 ms: 1.68x slower                                                |
| genshi_xml                 | 67.6 ms                                                | 114 ms: 1.69x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 143 ms: 1.71x slower                                                 |
| richards                   | 60.3 ms                                                | 104 ms: 1.73x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 758 us: 1.74x slower                                                 |
| django_template            | 44.9 ms                                                | 78.9 ms: 1.76x slower                                                |
| chaos                      | 84.9 ms                                                | 150 ms: 1.77x slower                                                 |
| raytrace                   | 408 ms                                                 | 727 ms: 1.78x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 272 ms: 1.79x slower                                                 |
| sympy_str                  | 385 ms                                                 | 688 ms: 1.79x slower                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 4.45 ms: 1.90x slower                                                |
| mako                       | 15.7 ms                                                | 30.4 ms: 1.93x slower                                                |
| logging_format             | 9.59 us                                                | 18.6 us: 1.94x slower                                                |
| hexiom                     | 8.27 ms                                                | 16.4 ms: 1.98x slower                                                |
| logging_silent             | 139 ns                                                 | 277 ns: 1.99x slower                                                 |
| scimark_sor                | 167 ms                                                 | 341 ms: 2.05x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 466 ms: 2.10x slower                                                 |
| sympy_expand               | 582 ms                                                 | 1.25 sec: 2.15x slower                                               |
| sqlglot_parse              | 1.79 ms                                                | 3.96 ms: 2.21x slower                                                |
| go                         | 172 ms                                                 | 384 ms: 2.23x slower                                                 |
| nbody                      | 119 ms                                                 | 275 ms: 2.31x slower                                                 |
| deltablue                  | 4.27 ms                                                | 11.4 ms: 2.66x slower                                                |
| unpack_sequence            | 60.2 ns                                                | 182 ns: 3.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.35x slower                                                         |

Benchmark hidden because not significant (3): regex_dna, unpickle, gc_traversal
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.18x