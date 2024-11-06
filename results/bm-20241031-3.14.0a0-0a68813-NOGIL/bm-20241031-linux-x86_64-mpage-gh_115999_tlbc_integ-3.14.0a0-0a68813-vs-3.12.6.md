# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_integ
- machine: linux-x86_64
- commit hash: 0a68813
- commit date: 2024-10-31
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 677 ms: 1.48x slower                                                 |
| docutils       | 4.00 sec                                               | 4.80 sec: 1.20x slower                                               |
| html5lib       | 88.9 ms                                                | 149 ms: 1.68x slower                                                 |
| tornado_http   | 266 ms                                                 | 345 ms: 1.30x slower                                                 |
| Geometric mean | (ref)                                                  | 1.40x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp        | 923 ms                                                 | 1.04 sec: 1.12x slower                                               |
| asyncio_tcp_ssl    | 2.81 sec                                               | 3.30 sec: 1.17x slower                                               |
| async_generators   | 589 ms                                                 | 701 ms: 1.19x slower                                                 |
| asyncio_websockets | 748 ms                                                 | 1.00 sec: 1.34x slower                                               |
| coroutines         | 29.5 ms                                                | 40.1 ms: 1.36x slower                                                |
| Geometric mean     | (ref)                                                  | 1.23x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 123 ms                                                 | 224 ms: 1.82x slower                                                 |
| nbody          | 119 ms                                                 | 304 ms: 2.55x slower                                                 |
| Geometric mean | (ref)                                                  | 1.65x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 32.5 ms                                                | 37.8 ms: 1.16x slower                                                |
| regex_compile  | 187 ms                                                 | 301 ms: 1.61x slower                                                 |
| Geometric mean | (ref)                                                  | 1.18x slower                                                         |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 45.7 us: 1.15x faster                                                |
| pickle_list          | 6.97 us                                                | 6.46 us: 1.08x faster                                                |
| xml_etree_parse      | 241 ms                                                 | 224 ms: 1.08x faster                                                 |
| pickle               | 16.4 us                                                | 15.4 us: 1.06x faster                                                |
| json_loads           | 37.9 us                                                | 45.8 us: 1.21x slower                                                |
| unpickle_list        | 6.83 us                                                | 8.47 us: 1.24x slower                                                |
| xml_etree_generate   | 127 ms                                                 | 159 ms: 1.25x slower                                                 |
| unpickle             | 21.2 us                                                | 27.2 us: 1.28x slower                                                |
| json_dumps           | 14.3 ms                                                | 19.7 ms: 1.38x slower                                                |
| tomli_loads          | 2.88 sec                                               | 4.24 sec: 1.47x slower                                               |
| xml_etree_process    | 83.7 ms                                                | 131 ms: 1.57x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 785 us: 1.80x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 566 us: 1.89x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                         |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.1 ms: 1.09x slower                                                |
| python_startup         | 23.7 ms                                                | 28.8 ms: 1.22x slower                                                |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 83.0 ms: 1.85x slower                                                |
| genshi_xml      | 67.6 ms                                                | 128 ms: 1.89x slower                                                 |
| mako            | 15.7 ms                                                | 31.1 ms: 1.98x slower                                                |
| genshi_text     | 30.2 ms                                                | 61.6 ms: 2.04x slower                                                |
| Geometric mean  | (ref)                                                  | 1.94x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 5.86 ms                                                | 4.99 ms: 1.17x faster                                                |
| pickle_dict              | 52.7 us                                                | 45.7 us: 1.15x faster                                                |
| pickle_list              | 6.97 us                                                | 6.46 us: 1.08x faster                                                |
| xml_etree_parse          | 241 ms                                                 | 224 ms: 1.08x faster                                                 |
| pickle                   | 16.4 us                                                | 15.4 us: 1.06x faster                                                |
| pathlib                  | 31.6 ms                                                | 34.1 ms: 1.08x slower                                                |
| python_startup_no_site   | 17.6 ms                                                | 19.1 ms: 1.09x slower                                                |
| asyncio_tcp              | 923 ms                                                 | 1.04 sec: 1.12x slower                                               |
| sqlite_synth             | 3.87 us                                                | 4.39 us: 1.13x slower                                                |
| regex_v8                 | 32.5 ms                                                | 37.8 ms: 1.16x slower                                                |
| asyncio_tcp_ssl          | 2.81 sec                                               | 3.30 sec: 1.17x slower                                               |
| async_generators         | 589 ms                                                 | 701 ms: 1.19x slower                                                 |
| docutils                 | 4.00 sec                                               | 4.80 sec: 1.20x slower                                               |
| json_loads               | 37.9 us                                                | 45.8 us: 1.21x slower                                                |
| scimark_fft              | 500 ms                                                 | 606 ms: 1.21x slower                                                 |
| deepcopy                 | 468 us                                                 | 568 us: 1.21x slower                                                 |
| python_startup           | 23.7 ms                                                | 28.8 ms: 1.22x slower                                                |
| unpickle_list            | 6.83 us                                                | 8.47 us: 1.24x slower                                                |
| xml_etree_generate       | 127 ms                                                 | 159 ms: 1.25x slower                                                 |
| json                     | 6.85 ms                                                | 8.73 ms: 1.27x slower                                                |
| pylint                   | 465 ms                                                 | 594 ms: 1.28x slower                                                 |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 8.57 ms: 1.28x slower                                                |
| unpickle                 | 21.2 us                                                | 27.2 us: 1.28x slower                                                |
| mdp                      | 3.97 sec                                               | 5.10 sec: 1.28x slower                                               |
| tornado_http             | 266 ms                                                 | 345 ms: 1.30x slower                                                 |
| deepcopy_memo            | 52.4 us                                                | 70.2 us: 1.34x slower                                                |
| asyncio_websockets       | 748 ms                                                 | 1.00 sec: 1.34x slower                                               |
| coroutines               | 29.5 ms                                                | 40.1 ms: 1.36x slower                                                |
| meteor_contest           | 146 ms                                                 | 201 ms: 1.37x slower                                                 |
| json_dumps               | 14.3 ms                                                | 19.7 ms: 1.38x slower                                                |
| bpe_tokeniser            | 6.59 sec                                               | 9.16 sec: 1.39x slower                                               |
| nqueens                  | 117 ms                                                 | 164 ms: 1.40x slower                                                 |
| pycparser                | 1.79 sec                                               | 2.51 sec: 1.40x slower                                               |
| fannkuch                 | 540 ms                                                 | 769 ms: 1.42x slower                                                 |
| pyflate                  | 727 ms                                                 | 1.05 sec: 1.44x slower                                               |
| spectral_norm            | 156 ms                                                 | 226 ms: 1.45x slower                                                 |
| dulwich_log              | 100 ms                                                 | 146 ms: 1.46x slower                                                 |
| tomli_loads              | 2.88 sec                                               | 4.24 sec: 1.47x slower                                               |
| typing_runtime_protocols | 224 us                                                 | 330 us: 1.47x slower                                                 |
| generators               | 41.1 ms                                                | 60.7 ms: 1.48x slower                                                |
| 2to3                     | 456 ms                                                 | 677 ms: 1.48x slower                                                 |
| sqlglot_normalize        | 157 ms                                                 | 234 ms: 1.49x slower                                                 |
| deepcopy_reduce          | 4.04 us                                                | 6.03 us: 1.50x slower                                                |
| crypto_pyaes             | 107 ms                                                 | 162 ms: 1.51x slower                                                 |
| comprehensions           | 27.1 us                                                | 41.6 us: 1.53x slower                                                |
| telco                    | 9.59 ms                                                | 14.9 ms: 1.56x slower                                                |
| sqlglot_optimize         | 76.0 ms                                                | 119 ms: 1.56x slower                                                 |
| sympy_integrate          | 29.8 ms                                                | 46.5 ms: 1.56x slower                                                |
| xml_etree_process        | 83.7 ms                                                | 131 ms: 1.57x slower                                                 |
| pprint_safe_repr         | 967 ms                                                 | 1.56 sec: 1.61x slower                                               |
| regex_compile            | 187 ms                                                 | 301 ms: 1.61x slower                                                 |
| coverage                 | 95.4 ms                                                | 154 ms: 1.61x slower                                                 |
| scimark_monte_carlo      | 96.4 ms                                                | 157 ms: 1.63x slower                                                 |
| pprint_pformat           | 1.98 sec                                               | 3.24 sec: 1.64x slower                                               |
| html5lib                 | 88.9 ms                                                | 149 ms: 1.68x slower                                                 |
| logging_simple           | 9.45 us                                                | 16.4 us: 1.74x slower                                                |
| thrift                   | 1.06 ms                                                | 1.86 ms: 1.75x slower                                                |
| sympy_str                | 385 ms                                                 | 682 ms: 1.77x slower                                                 |
| pickle_pure_python       | 436 us                                                 | 785 us: 1.80x slower                                                 |
| logging_silent           | 139 ns                                                 | 253 ns: 1.81x slower                                                 |
| float                    | 123 ms                                                 | 224 ms: 1.82x slower                                                 |
| scimark_lu               | 152 ms                                                 | 279 ms: 1.83x slower                                                 |
| richards_super           | 72.8 ms                                                | 134 ms: 1.83x slower                                                 |
| django_template          | 44.9 ms                                                | 83.0 ms: 1.85x slower                                                |
| logging_format           | 9.59 us                                                | 17.8 us: 1.86x slower                                                |
| chaos                    | 84.9 ms                                                | 159 ms: 1.87x slower                                                 |
| unpickle_pure_python     | 300 us                                                 | 566 us: 1.89x slower                                                 |
| genshi_xml               | 67.6 ms                                                | 128 ms: 1.89x slower                                                 |
| raytrace                 | 408 ms                                                 | 783 ms: 1.92x slower                                                 |
| hexiom                   | 8.27 ms                                                | 16.1 ms: 1.94x slower                                                |
| richards                 | 60.3 ms                                                | 119 ms: 1.97x slower                                                 |
| mako                     | 15.7 ms                                                | 31.1 ms: 1.98x slower                                                |
| scimark_sor              | 167 ms                                                 | 335 ms: 2.01x slower                                                 |
| genshi_text              | 30.2 ms                                                | 61.6 ms: 2.04x slower                                                |
| sympy_sum                | 222 ms                                                 | 469 ms: 2.12x slower                                                 |
| sqlglot_transpile        | 2.34 ms                                                | 4.99 ms: 2.13x slower                                                |
| go                       | 172 ms                                                 | 379 ms: 2.20x slower                                                 |
| sympy_expand             | 582 ms                                                 | 1.31 sec: 2.24x slower                                               |
| sqlglot_parse            | 1.79 ms                                                | 4.27 ms: 2.39x slower                                                |
| nbody                    | 119 ms                                                 | 304 ms: 2.55x slower                                                 |
| deltablue                | 4.27 ms                                                | 12.0 ms: 2.81x slower                                                |
| bench_mp_pool            | 20.7 ms                                                | 58.4 ms: 2.82x slower                                                |
| unpack_sequence          | 60.2 ns                                                | 213 ns: 3.54x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.49x slower                                                         |

Benchmark hidden because not significant (6): bench_thread_pool, pidigits, create_gc_cycles, regex_dna, regex_effbot, xml_etree_iterparse
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.42x
- 95% likely to have a slowdown of 1.40x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.19x