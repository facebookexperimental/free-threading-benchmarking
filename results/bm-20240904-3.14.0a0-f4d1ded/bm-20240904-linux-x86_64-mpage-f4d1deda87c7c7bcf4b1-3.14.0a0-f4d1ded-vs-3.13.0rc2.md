# Results vs. 3.13.0rc2

- fork: mpage
- ref: f4d1deda87c7c7bcf4b1
- machine: linux-x86_64
- commit hash: f4d1ded
- commit date: 2024-09-04
- overall geometric mean: 1.27x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 546 ms: 1.23x slower                                                 |
| docutils       | 4.01 sec                                                     | 4.52 sec: 1.13x slower                                               |
| html5lib       | 92.6 ms                                                      | 130 ms: 1.40x slower                                                 |
| tornado_http   | 251 ms                                                       | 334 ms: 1.33x slower                                                 |
| Geometric mean | (ref)                                                        | 1.27x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.56 sec: 1.11x slower                                               |
| async_tree_none            | 572 ms                                                       | 636 ms: 1.11x slower                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.55 sec: 1.12x slower                                               |
| async_generators           | 567 ms                                                       | 637 ms: 1.12x slower                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 760 ms: 1.13x slower                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 1.01 sec: 1.14x slower                                               |
| async_tree_memoization     | 709 ms                                                       | 809 ms: 1.14x slower                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 1.01 sec: 1.18x slower                                               |
| async_tree_none_tg         | 504 ms                                                       | 609 ms: 1.21x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 38.7 ms: 1.25x slower                                                |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                         |

Benchmark hidden because not significant (3): asyncio_websockets, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 116 ms                                                       | 171 ms: 1.48x slower                                                 |
| nbody          | 119 ms                                                       | 226 ms: 1.90x slower                                                 |
| Geometric mean | (ref)                                                        | 1.41x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 304 ms: 1.08x slower                                                 |
| regex_v8       | 32.8 ms                                                      | 38.6 ms: 1.18x slower                                                |
| regex_compile  | 182 ms                                                       | 253 ms: 1.39x slower                                                 |
| Geometric mean | (ref)                                                        | 1.16x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle             | 20.5 us                                                      | 19.4 us: 1.06x faster                                                |
| pickle_dict          | 47.2 us                                                      | 45.2 us: 1.04x faster                                                |
| xml_etree_iterparse  | 177 ms                                                       | 196 ms: 1.11x slower                                                 |
| unpickle_list        | 6.68 us                                                      | 7.52 us: 1.13x slower                                                |
| xml_etree_generate   | 122 ms                                                       | 142 ms: 1.16x slower                                                 |
| json_loads           | 34.3 us                                                      | 40.3 us: 1.18x slower                                                |
| json_dumps           | 14.1 ms                                                      | 16.8 ms: 1.19x slower                                                |
| xml_etree_process    | 85.9 ms                                                      | 110 ms: 1.28x slower                                                 |
| tomli_loads          | 2.78 sec                                                     | 3.74 sec: 1.34x slower                                               |
| unpickle_pure_python | 290 us                                                       | 461 us: 1.59x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 673 us: 1.62x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.15x slower                                                         |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 23.5 ms: 1.05x slower                                                |
| python_startup_no_site | 15.3 ms                                                      | 16.3 ms: 1.06x slower                                                |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 43.7 ms: 1.38x slower                                                |
| genshi_xml      | 72.1 ms                                                      | 101 ms: 1.41x slower                                                 |
| mako            | 15.9 ms                                                      | 22.5 ms: 1.41x slower                                                |
| django_template | 44.3 ms                                                      | 64.3 ms: 1.45x slower                                                |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle                   | 20.5 us                                                      | 19.4 us: 1.06x faster                                                |
| pickle_dict                | 47.2 us                                                      | 45.2 us: 1.04x faster                                                |
| python_startup             | 22.4 ms                                                      | 23.5 ms: 1.05x slower                                                |
| deepcopy_memo              | 50.1 us                                                      | 53.1 us: 1.06x slower                                                |
| coverage                   | 107 ms                                                       | 114 ms: 1.06x slower                                                 |
| python_startup_no_site     | 15.3 ms                                                      | 16.3 ms: 1.06x slower                                                |
| mdp                        | 3.80 sec                                                     | 4.07 sec: 1.07x slower                                               |
| regex_dna                  | 282 ms                                                       | 304 ms: 1.08x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.47 us: 1.09x slower                                                |
| sqlite_synth               | 3.99 us                                                      | 4.40 us: 1.10x slower                                                |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.49 ms: 1.11x slower                                                |
| xml_etree_iterparse        | 177 ms                                                       | 196 ms: 1.11x slower                                                 |
| async_tree_io_tg           | 1.40 sec                                                     | 1.56 sec: 1.11x slower                                               |
| async_tree_none            | 572 ms                                                       | 636 ms: 1.11x slower                                                 |
| meteor_contest             | 150 ms                                                       | 168 ms: 1.12x slower                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.55 sec: 1.12x slower                                               |
| async_generators           | 567 ms                                                       | 637 ms: 1.12x slower                                                 |
| unpickle_list              | 6.68 us                                                      | 7.52 us: 1.13x slower                                                |
| pathlib                    | 29.9 ms                                                      | 33.7 ms: 1.13x slower                                                |
| docutils                   | 4.01 sec                                                     | 4.52 sec: 1.13x slower                                               |
| gc_traversal               | 5.70 ms                                                      | 6.46 ms: 1.13x slower                                                |
| async_tree_memoization_tg  | 670 ms                                                       | 760 ms: 1.13x slower                                                 |
| scimark_fft                | 473 ms                                                       | 538 ms: 1.14x slower                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 1.01 sec: 1.14x slower                                               |
| async_tree_memoization     | 709 ms                                                       | 809 ms: 1.14x slower                                                 |
| sympy_integrate            | 30.2 ms                                                      | 35.0 ms: 1.16x slower                                                |
| xml_etree_generate         | 122 ms                                                       | 142 ms: 1.16x slower                                                 |
| regex_v8                   | 32.8 ms                                                      | 38.6 ms: 1.18x slower                                                |
| json_loads                 | 34.3 us                                                      | 40.3 us: 1.18x slower                                                |
| json                       | 6.51 ms                                                      | 7.67 ms: 1.18x slower                                                |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 1.01 sec: 1.18x slower                                               |
| json_dumps                 | 14.1 ms                                                      | 16.8 ms: 1.19x slower                                                |
| pylint                     | 470 ms                                                       | 563 ms: 1.20x slower                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 7.57 sec: 1.20x slower                                               |
| async_tree_none_tg         | 504 ms                                                       | 609 ms: 1.21x slower                                                 |
| generators                 | 40.0 ms                                                      | 48.5 ms: 1.21x slower                                                |
| nqueens                    | 112 ms                                                       | 136 ms: 1.22x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 275 us: 1.22x slower                                                 |
| 2to3                       | 445 ms                                                       | 546 ms: 1.23x slower                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 23.1 ms: 1.24x slower                                                |
| sympy_expand               | 601 ms                                                       | 742 ms: 1.24x slower                                                 |
| sympy_sum                  | 210 ms                                                       | 260 ms: 1.24x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 38.7 ms: 1.25x slower                                                |
| fannkuch                   | 547 ms                                                       | 688 ms: 1.26x slower                                                 |
| sympy_str                  | 379 ms                                                       | 480 ms: 1.27x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 110 ms: 1.28x slower                                                 |
| pycparser                  | 1.57 sec                                                     | 2.06 sec: 1.31x slower                                               |
| thrift                     | 1.10 ms                                                      | 1.45 ms: 1.32x slower                                                |
| tornado_http               | 251 ms                                                       | 334 ms: 1.33x slower                                                 |
| tomli_loads                | 2.78 sec                                                     | 3.74 sec: 1.34x slower                                               |
| crypto_pyaes               | 100 ms                                                       | 137 ms: 1.37x slower                                                 |
| spectral_norm              | 157 ms                                                       | 216 ms: 1.38x slower                                                 |
| richards                   | 65.5 ms                                                      | 90.4 ms: 1.38x slower                                                |
| genshi_text                | 31.7 ms                                                      | 43.7 ms: 1.38x slower                                                |
| regex_compile              | 182 ms                                                       | 253 ms: 1.39x slower                                                 |
| comprehensions             | 22.2 us                                                      | 31.0 us: 1.39x slower                                                |
| html5lib                   | 92.6 ms                                                      | 130 ms: 1.40x slower                                                 |
| genshi_xml                 | 72.1 ms                                                      | 101 ms: 1.41x slower                                                 |
| mako                       | 15.9 ms                                                      | 22.5 ms: 1.41x slower                                                |
| pprint_safe_repr           | 987 ms                                                       | 1.39 sec: 1.41x slower                                               |
| pprint_pformat             | 1.94 sec                                                     | 2.76 sec: 1.42x slower                                               |
| sqlglot_optimize           | 74.7 ms                                                      | 106 ms: 1.42x slower                                                 |
| bench_thread_pool          | 2.89 ms                                                      | 4.17 ms: 1.44x slower                                                |
| pyflate                    | 664 ms                                                       | 961 ms: 1.45x slower                                                 |
| django_template            | 44.3 ms                                                      | 64.3 ms: 1.45x slower                                                |
| sqlglot_normalize          | 140 ms                                                       | 205 ms: 1.46x slower                                                 |
| float                      | 116 ms                                                       | 171 ms: 1.48x slower                                                 |
| logging_simple             | 8.56 us                                                      | 12.9 us: 1.51x slower                                                |
| richards_super             | 73.2 ms                                                      | 111 ms: 1.52x slower                                                 |
| chaos                      | 83.6 ms                                                      | 129 ms: 1.54x slower                                                 |
| go                         | 191 ms                                                       | 298 ms: 1.56x slower                                                 |
| unpickle_pure_python       | 290 us                                                       | 461 us: 1.59x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 673 us: 1.62x slower                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 147 ms: 1.62x slower                                                 |
| logging_silent             | 130 ns                                                       | 214 ns: 1.64x slower                                                 |
| logging_format             | 9.24 us                                                      | 15.4 us: 1.66x slower                                                |
| sqlglot_transpile          | 2.20 ms                                                      | 3.66 ms: 1.67x slower                                                |
| sqlglot_parse              | 1.76 ms                                                      | 2.93 ms: 1.67x slower                                                |
| scimark_sor                | 179 ms                                                       | 304 ms: 1.70x slower                                                 |
| hexiom                     | 8.11 ms                                                      | 13.9 ms: 1.71x slower                                                |
| raytrace                   | 344 ms                                                       | 608 ms: 1.77x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 261 ms: 1.78x slower                                                 |
| nbody                      | 119 ms                                                       | 226 ms: 1.90x slower                                                 |
| unpack_sequence            | 74.3 ns                                                      | 149 ns: 2.00x slower                                                 |
| deltablue                  | 4.44 ms                                                      | 9.01 ms: 2.03x slower                                                |
| Geometric mean             | (ref)                                                        | 1.27x slower                                                         |

Benchmark hidden because not significant (11): xml_etree_parse, pickle_list, create_gc_cycles, asyncio_websockets, deepcopy, telco, pickle, asyncio_tcp_ssl, pidigits, regex_effbot, asyncio_tcp
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.00x