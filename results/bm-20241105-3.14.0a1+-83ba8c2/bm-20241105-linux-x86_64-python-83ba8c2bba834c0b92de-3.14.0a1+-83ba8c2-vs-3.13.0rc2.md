# Results vs. 3.13.0rc2

- fork: python
- ref: 83ba8c2bba834c0b92de
- machine: linux-x86_64
- commit hash: 83ba8c2
- commit date: 2024-11-05
- overall geometric mean: 1.14x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 488 ms: 1.10x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.21 sec: 1.05x slower                                                 |
| html5lib       | 92.6 ms                                                      | 97.6 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines         | 30.9 ms                                                      | 34.7 ms: 1.12x slower                                                  |
| async_generators   | 567 ms                                                       | 684 ms: 1.21x slower                                                   |
| asyncio_websockets | 766 ms                                                       | 998 ms: 1.30x slower                                                   |
| Geometric mean     | (ref)                                                        | 1.11x slower                                                           |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 236 ms: 1.07x faster                                                   |
| float          | 116 ms                                                       | 147 ms: 1.27x slower                                                   |
| nbody          | 119 ms                                                       | 199 ms: 1.67x slower                                                   |
| Geometric mean | (ref)                                                        | 1.26x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 36.0 ms: 1.10x slower                                                  |
| regex_compile  | 182 ms                                                       | 206 ms: 1.13x slower                                                   |
| regex_effbot   | 4.74 ms                                                      | 5.43 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 44.6 us: 1.06x faster                                                  |
| unpickle             | 20.5 us                                                      | 21.9 us: 1.07x slower                                                  |
| json_loads           | 34.3 us                                                      | 37.7 us: 1.10x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 3.06 sec: 1.10x slower                                                 |
| pickle               | 15.1 us                                                      | 17.1 us: 1.13x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 97.7 ms: 1.14x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 16.4 ms: 1.16x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 339 us: 1.17x slower                                                   |
| unpickle_list        | 6.68 us                                                      | 7.84 us: 1.17x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 144 ms: 1.18x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 533 us: 1.28x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 87.2 ms: 1.21x slower                                                  |
| mako            | 15.9 ms                                                      | 19.8 ms: 1.24x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 41.2 ms: 1.30x slower                                                  |
| django_template | 44.3 ms                                                      | 58.9 ms: 1.33x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 498 us                                                       | 427 us: 1.17x faster                                                   |
| pidigits                 | 251 ms                                                       | 236 ms: 1.07x faster                                                   |
| telco                    | 12.2 ms                                                      | 11.4 ms: 1.06x faster                                                  |
| pickle_dict              | 47.2 us                                                      | 44.6 us: 1.06x faster                                                  |
| unpack_sequence          | 74.3 ns                                                      | 70.7 ns: 1.05x faster                                                  |
| deepcopy_reduce          | 4.10 us                                                      | 4.23 us: 1.03x slower                                                  |
| crypto_pyaes             | 100 ms                                                       | 104 ms: 1.04x slower                                                   |
| nqueens                  | 112 ms                                                       | 117 ms: 1.05x slower                                                   |
| docutils                 | 4.01 sec                                                     | 4.21 sec: 1.05x slower                                                 |
| html5lib                 | 92.6 ms                                                      | 97.6 ms: 1.05x slower                                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.04 sec: 1.06x slower                                                 |
| unpickle                 | 20.5 us                                                      | 21.9 us: 1.07x slower                                                  |
| mdp                      | 3.80 sec                                                     | 4.08 sec: 1.07x slower                                                 |
| coverage                 | 107 ms                                                       | 116 ms: 1.08x slower                                                   |
| scimark_fft              | 473 ms                                                       | 510 ms: 1.08x slower                                                   |
| sympy_str                | 379 ms                                                       | 408 ms: 1.08x slower                                                   |
| thrift                   | 1.10 ms                                                      | 1.20 ms: 1.09x slower                                                  |
| 2to3                     | 445 ms                                                       | 488 ms: 1.10x slower                                                   |
| regex_v8                 | 32.8 ms                                                      | 36.0 ms: 1.10x slower                                                  |
| json                     | 6.51 ms                                                      | 7.17 ms: 1.10x slower                                                  |
| json_loads               | 34.3 us                                                      | 37.7 us: 1.10x slower                                                  |
| tomli_loads              | 2.78 sec                                                     | 3.06 sec: 1.10x slower                                                 |
| richards                 | 65.5 ms                                                      | 73.1 ms: 1.12x slower                                                  |
| scimark_monte_carlo      | 90.6 ms                                                      | 101 ms: 1.12x slower                                                   |
| coroutines               | 30.9 ms                                                      | 34.7 ms: 1.12x slower                                                  |
| generators               | 40.0 ms                                                      | 45.2 ms: 1.13x slower                                                  |
| pickle                   | 15.1 us                                                      | 17.1 us: 1.13x slower                                                  |
| regex_compile            | 182 ms                                                       | 206 ms: 1.13x slower                                                   |
| xml_etree_process        | 85.9 ms                                                      | 97.7 ms: 1.14x slower                                                  |
| pyflate                  | 664 ms                                                       | 757 ms: 1.14x slower                                                   |
| chaos                    | 83.6 ms                                                      | 95.4 ms: 1.14x slower                                                  |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 7.74 ms: 1.15x slower                                                  |
| regex_effbot             | 4.74 ms                                                      | 5.43 ms: 1.15x slower                                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 7.22 sec: 1.15x slower                                                 |
| typing_runtime_protocols | 226 us                                                       | 259 us: 1.15x slower                                                   |
| gc_traversal             | 5.70 ms                                                      | 6.55 ms: 1.15x slower                                                  |
| scimark_lu               | 146 ms                                                       | 169 ms: 1.15x slower                                                   |
| dulwich_log              | 93.7 ms                                                      | 109 ms: 1.16x slower                                                   |
| json_dumps               | 14.1 ms                                                      | 16.4 ms: 1.16x slower                                                  |
| sqlglot_transpile        | 2.20 ms                                                      | 2.55 ms: 1.16x slower                                                  |
| sympy_expand             | 601 ms                                                       | 698 ms: 1.16x slower                                                   |
| unpickle_pure_python     | 290 us                                                       | 339 us: 1.17x slower                                                   |
| logging_format           | 9.24 us                                                      | 10.8 us: 1.17x slower                                                  |
| scimark_sor              | 179 ms                                                       | 209 ms: 1.17x slower                                                   |
| unpickle_list            | 6.68 us                                                      | 7.84 us: 1.17x slower                                                  |
| sympy_sum                | 210 ms                                                       | 247 ms: 1.17x slower                                                   |
| pprint_pformat           | 1.94 sec                                                     | 2.28 sec: 1.18x slower                                                 |
| logging_simple           | 8.56 us                                                      | 10.1 us: 1.18x slower                                                  |
| xml_etree_generate       | 122 ms                                                       | 144 ms: 1.18x slower                                                   |
| richards_super           | 73.2 ms                                                      | 87.5 ms: 1.20x slower                                                  |
| sqlglot_parse            | 1.76 ms                                                      | 2.10 ms: 1.20x slower                                                  |
| spectral_norm            | 157 ms                                                       | 188 ms: 1.20x slower                                                   |
| async_generators         | 567 ms                                                       | 684 ms: 1.21x slower                                                   |
| hexiom                   | 8.11 ms                                                      | 9.80 ms: 1.21x slower                                                  |
| genshi_xml               | 72.1 ms                                                      | 87.2 ms: 1.21x slower                                                  |
| mako                     | 15.9 ms                                                      | 19.8 ms: 1.24x slower                                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 93.8 ms: 1.25x slower                                                  |
| logging_silent           | 130 ns                                                       | 165 ns: 1.27x slower                                                   |
| float                    | 116 ms                                                       | 147 ms: 1.27x slower                                                   |
| comprehensions           | 22.2 us                                                      | 28.4 us: 1.28x slower                                                  |
| pickle_pure_python       | 416 us                                                       | 533 us: 1.28x slower                                                   |
| deltablue                | 4.44 ms                                                      | 5.74 ms: 1.29x slower                                                  |
| asyncio_websockets       | 766 ms                                                       | 998 ms: 1.30x slower                                                   |
| genshi_text              | 31.7 ms                                                      | 41.2 ms: 1.30x slower                                                  |
| django_template          | 44.3 ms                                                      | 58.9 ms: 1.33x slower                                                  |
| pycparser                | 1.57 sec                                                     | 2.09 sec: 1.33x slower                                                 |
| raytrace                 | 344 ms                                                       | 465 ms: 1.35x slower                                                   |
| sqlglot_normalize        | 140 ms                                                       | 191 ms: 1.37x slower                                                   |
| nbody                    | 119 ms                                                       | 199 ms: 1.67x slower                                                   |
| bench_mp_pool            | 18.7 ms                                                      | 77.7 ms: 4.16x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.14x slower                                                           |

Benchmark hidden because not significant (18): xml_etree_parse, asyncio_tcp, pathlib, python_startup, deepcopy_memo, asyncio_tcp_ssl, sqlite_synth, sympy_integrate, bench_thread_pool, pickle_list, xml_etree_iterparse, regex_dna, python_startup_no_site, fannkuch, meteor_contest, go, create_gc_cycles, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.01x