# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 2613a14
- commit date: 2024-09-25
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 706 ms: 1.59x slower                                                 |
| docutils       | 4.01 sec                                                     | 4.90 sec: 1.22x slower                                               |
| html5lib       | 92.6 ms                                                      | 144 ms: 1.56x slower                                                 |
| tornado_http   | 251 ms                                                       | 370 ms: 1.47x slower                                                 |
| Geometric mean | (ref)                                                        | 1.45x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg        | 1.40 sec                                                     | 1.13 sec: 1.24x faster                                               |
| async_tree_io           | 1.39 sec                                                     | 1.28 sec: 1.08x faster                                               |
| asyncio_websockets      | 766 ms                                                       | 794 ms: 1.04x slower                                                 |
| async_tree_none_tg      | 504 ms                                                       | 530 ms: 1.05x slower                                                 |
| async_tree_cpu_io_mixed | 889 ms                                                       | 960 ms: 1.08x slower                                                 |
| asyncio_tcp             | 948 ms                                                       | 1.11 sec: 1.18x slower                                               |
| coroutines              | 30.9 ms                                                      | 37.2 ms: 1.21x slower                                                |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 3.43 sec: 1.24x slower                                               |
| async_generators        | 567 ms                                                       | 747 ms: 1.32x slower                                                 |
| Geometric mean          | (ref)                                                        | 1.06x slower                                                         |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 116 ms                                                       | 201 ms: 1.73x slower                                                 |
| nbody          | 119 ms                                                       | 275 ms: 2.31x slower                                                 |
| Geometric mean | (ref)                                                        | 1.57x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.41 ms: 1.07x faster                                                |
| regex_v8       | 32.8 ms                                                      | 36.0 ms: 1.10x slower                                                |
| regex_compile  | 182 ms                                                       | 282 ms: 1.55x slower                                                 |
| Geometric mean | (ref)                                                        | 1.13x slower                                                         |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 158 ms: 1.12x faster                                                 |
| unpickle             | 20.5 us                                                      | 21.9 us: 1.07x slower                                                |
| unpickle_list        | 6.68 us                                                      | 7.79 us: 1.17x slower                                                |
| json_dumps           | 14.1 ms                                                      | 17.3 ms: 1.22x slower                                                |
| json_loads           | 34.3 us                                                      | 43.9 us: 1.28x slower                                                |
| xml_etree_generate   | 122 ms                                                       | 157 ms: 1.28x slower                                                 |
| tomli_loads          | 2.78 sec                                                     | 4.05 sec: 1.46x slower                                               |
| xml_etree_process    | 85.9 ms                                                      | 143 ms: 1.67x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 498 us: 1.72x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 758 us: 1.82x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                         |

Benchmark hidden because not significant (4): pickle_list, xml_etree_parse, pickle_dict, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 22.1 ms: 1.44x slower                                                |
| python_startup         | 22.4 ms                                                      | 33.7 ms: 1.51x slower                                                |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 114 ms: 1.58x slower                                                 |
| genshi_text     | 31.7 ms                                                      | 50.8 ms: 1.60x slower                                                |
| django_template | 44.3 ms                                                      | 78.9 ms: 1.78x slower                                                |
| mako            | 15.9 ms                                                      | 30.4 ms: 1.90x slower                                                |
| Geometric mean  | (ref)                                                        | 1.71x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240925-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg         | 1.40 sec                                                     | 1.13 sec: 1.24x faster                                               |
| create_gc_cycles         | 2.41 ms                                                      | 2.12 ms: 1.14x faster                                                |
| xml_etree_iterparse      | 177 ms                                                       | 158 ms: 1.12x faster                                                 |
| async_tree_io            | 1.39 sec                                                     | 1.28 sec: 1.08x faster                                               |
| regex_effbot             | 4.74 ms                                                      | 4.41 ms: 1.07x faster                                                |
| asyncio_websockets       | 766 ms                                                       | 794 ms: 1.04x slower                                                 |
| async_tree_none_tg       | 504 ms                                                       | 530 ms: 1.05x slower                                                 |
| unpickle                 | 20.5 us                                                      | 21.9 us: 1.07x slower                                                |
| gc_traversal             | 5.70 ms                                                      | 6.09 ms: 1.07x slower                                                |
| async_tree_cpu_io_mixed  | 889 ms                                                       | 960 ms: 1.08x slower                                                 |
| deepcopy                 | 498 us                                                       | 545 us: 1.10x slower                                                 |
| regex_v8                 | 32.8 ms                                                      | 36.0 ms: 1.10x slower                                                |
| json                     | 6.51 ms                                                      | 7.39 ms: 1.13x slower                                                |
| scimark_fft              | 473 ms                                                       | 549 ms: 1.16x slower                                                 |
| pathlib                  | 29.9 ms                                                      | 34.8 ms: 1.16x slower                                                |
| unpickle_list            | 6.68 us                                                      | 7.79 us: 1.17x slower                                                |
| asyncio_tcp              | 948 ms                                                       | 1.11 sec: 1.18x slower                                               |
| telco                    | 12.2 ms                                                      | 14.4 ms: 1.18x slower                                                |
| coroutines               | 30.9 ms                                                      | 37.2 ms: 1.21x slower                                                |
| sqlite_synth             | 3.99 us                                                      | 4.81 us: 1.21x slower                                                |
| meteor_contest           | 150 ms                                                       | 182 ms: 1.21x slower                                                 |
| docutils                 | 4.01 sec                                                     | 4.90 sec: 1.22x slower                                               |
| json_dumps               | 14.1 ms                                                      | 17.3 ms: 1.22x slower                                                |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.26 ms: 1.22x slower                                                |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.43 sec: 1.24x slower                                               |
| json_loads               | 34.3 us                                                      | 43.9 us: 1.28x slower                                                |
| xml_etree_generate       | 122 ms                                                       | 157 ms: 1.28x slower                                                 |
| pylint                   | 470 ms                                                       | 604 ms: 1.28x slower                                                 |
| typing_runtime_protocols | 226 us                                                       | 292 us: 1.29x slower                                                 |
| spectral_norm            | 157 ms                                                       | 203 ms: 1.30x slower                                                 |
| nqueens                  | 112 ms                                                       | 145 ms: 1.30x slower                                                 |
| async_generators         | 567 ms                                                       | 747 ms: 1.32x slower                                                 |
| deepcopy_reduce          | 4.10 us                                                      | 5.41 us: 1.32x slower                                                |
| coverage                 | 107 ms                                                       | 145 ms: 1.35x slower                                                 |
| mdp                      | 3.80 sec                                                     | 5.17 sec: 1.36x slower                                               |
| deepcopy_memo            | 50.1 us                                                      | 70.1 us: 1.40x slower                                                |
| generators               | 40.0 ms                                                      | 56.8 ms: 1.42x slower                                                |
| fannkuch                 | 547 ms                                                       | 784 ms: 1.43x slower                                                 |
| python_startup_no_site   | 15.3 ms                                                      | 22.1 ms: 1.44x slower                                                |
| pycparser                | 1.57 sec                                                     | 2.26 sec: 1.44x slower                                               |
| dulwich_log              | 93.7 ms                                                      | 136 ms: 1.45x slower                                                 |
| tomli_loads              | 2.78 sec                                                     | 4.05 sec: 1.46x slower                                               |
| tornado_http             | 251 ms                                                       | 370 ms: 1.47x slower                                                 |
| sympy_integrate          | 30.2 ms                                                      | 45.5 ms: 1.50x slower                                                |
| python_startup           | 22.4 ms                                                      | 33.7 ms: 1.51x slower                                                |
| crypto_pyaes             | 100 ms                                                       | 151 ms: 1.51x slower                                                 |
| sqlglot_normalize        | 140 ms                                                       | 211 ms: 1.51x slower                                                 |
| thrift                   | 1.10 ms                                                      | 1.68 ms: 1.53x slower                                                |
| regex_compile            | 182 ms                                                       | 282 ms: 1.55x slower                                                 |
| sqlglot_optimize         | 74.7 ms                                                      | 116 ms: 1.55x slower                                                 |
| pyflate                  | 664 ms                                                       | 1.03 sec: 1.55x slower                                               |
| bpe_tokeniser            | 6.28 sec                                                     | 9.77 sec: 1.55x slower                                               |
| html5lib                 | 92.6 ms                                                      | 144 ms: 1.56x slower                                                 |
| genshi_xml               | 72.1 ms                                                      | 114 ms: 1.58x slower                                                 |
| 2to3                     | 445 ms                                                       | 706 ms: 1.59x slower                                                 |
| richards                 | 65.5 ms                                                      | 104 ms: 1.59x slower                                                 |
| genshi_text              | 31.7 ms                                                      | 50.8 ms: 1.60x slower                                                |
| pprint_safe_repr         | 987 ms                                                       | 1.60 sec: 1.62x slower                                               |
| pprint_pformat           | 1.94 sec                                                     | 3.16 sec: 1.63x slower                                               |
| richards_super           | 73.2 ms                                                      | 122 ms: 1.66x slower                                                 |
| xml_etree_process        | 85.9 ms                                                      | 143 ms: 1.67x slower                                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 152 ms: 1.67x slower                                                 |
| bench_thread_pool        | 2.89 ms                                                      | 4.86 ms: 1.68x slower                                                |
| unpickle_pure_python     | 290 us                                                       | 498 us: 1.72x slower                                                 |
| float                    | 116 ms                                                       | 201 ms: 1.73x slower                                                 |
| comprehensions           | 22.2 us                                                      | 39.5 us: 1.77x slower                                                |
| django_template          | 44.3 ms                                                      | 78.9 ms: 1.78x slower                                                |
| chaos                    | 83.6 ms                                                      | 150 ms: 1.80x slower                                                 |
| sympy_str                | 379 ms                                                       | 688 ms: 1.81x slower                                                 |
| pickle_pure_python       | 416 us                                                       | 758 us: 1.82x slower                                                 |
| logging_simple           | 8.56 us                                                      | 15.6 us: 1.83x slower                                                |
| scimark_lu               | 146 ms                                                       | 272 ms: 1.86x slower                                                 |
| mako                     | 15.9 ms                                                      | 30.4 ms: 1.90x slower                                                |
| scimark_sor              | 179 ms                                                       | 341 ms: 1.91x slower                                                 |
| go                       | 191 ms                                                       | 384 ms: 2.01x slower                                                 |
| logging_format           | 9.24 us                                                      | 18.6 us: 2.01x slower                                                |
| hexiom                   | 8.11 ms                                                      | 16.4 ms: 2.02x slower                                                |
| sqlglot_transpile        | 2.20 ms                                                      | 4.45 ms: 2.03x slower                                                |
| sympy_expand             | 601 ms                                                       | 1.25 sec: 2.08x slower                                               |
| raytrace                 | 344 ms                                                       | 727 ms: 2.11x slower                                                 |
| logging_silent           | 130 ns                                                       | 277 ns: 2.13x slower                                                 |
| sympy_sum                | 210 ms                                                       | 466 ms: 2.22x slower                                                 |
| sqlglot_parse            | 1.76 ms                                                      | 3.96 ms: 2.25x slower                                                |
| nbody                    | 119 ms                                                       | 275 ms: 2.31x slower                                                 |
| unpack_sequence          | 74.3 ns                                                      | 182 ns: 2.45x slower                                                 |
| deltablue                | 4.44 ms                                                      | 11.4 ms: 2.56x slower                                                |
| Geometric mean           | (ref)                                                        | 1.40x slower                                                         |

Benchmark hidden because not significant (11): pidigits, pickle_list, xml_etree_parse, pickle_dict, bench_mp_pool, async_tree_cpu_io_mixed_tg, async_tree_none, pickle, regex_dna, async_tree_memoization_tg, async_tree_memoization
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.17x