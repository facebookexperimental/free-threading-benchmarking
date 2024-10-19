# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 819f30a
- commit date: 2024-10-18
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 413 ms                                                                | 411 ms: 1.00x faster                                                |
| docutils       | 3.32 sec                                                              | 3.28 sec: 1.01x faster                                              |
| tornado_http   | 163 ms                                                                | 162 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                        |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| coroutines         | 32.1 ms                                                               | 29.3 ms: 1.10x faster                                               |
| asyncio_websockets | 523 ms                                                                | 519 ms: 1.01x faster                                                |
| asyncio_tcp        | 575 ms                                                                | 581 ms: 1.01x slower                                                |
| asyncio_tcp_ssl    | 1.70 sec                                                              | 1.81 sec: 1.06x slower                                              |
| async_generators   | 492 ms                                                                | 525 ms: 1.07x slower                                                |
| Geometric mean     | (ref)                                                                 | 1.01x slower                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 224 ms                                                                | 185 ms: 1.21x faster                                                |
| float          | 154 ms                                                                | 146 ms: 1.06x faster                                                |
| pidigits       | 187 ms                                                                | 186 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                 | 1.09x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 228 ms                                                                | 221 ms: 1.03x faster                                                |
| regex_effbot   | 2.96 ms                                                               | 3.10 ms: 1.05x slower                                               |
| regex_v8       | 24.5 ms                                                               | 26.1 ms: 1.07x slower                                               |
| regex_dna      | 170 ms                                                                | 190 ms: 1.12x slower                                                |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 419 us                                                                | 393 us: 1.07x faster                                                |
| json_loads           | 29.7 us                                                               | 28.2 us: 1.05x faster                                               |
| pickle_pure_python   | 617 us                                                                | 586 us: 1.05x faster                                                |
| xml_etree_process    | 93.6 ms                                                               | 89.8 ms: 1.04x faster                                               |
| xml_etree_generate   | 114 ms                                                                | 110 ms: 1.04x faster                                                |
| xml_etree_iterparse  | 109 ms                                                                | 105 ms: 1.04x faster                                                |
| tomli_loads          | 3.31 sec                                                              | 3.22 sec: 1.03x faster                                              |
| pickle_dict          | 32.4 us                                                               | 31.6 us: 1.03x faster                                               |
| unpickle             | 14.8 us                                                               | 14.5 us: 1.02x faster                                               |
| xml_etree_parse      | 134 ms                                                                | 132 ms: 1.02x faster                                                |
| json_dumps           | 15.3 ms                                                               | 15.1 ms: 1.01x faster                                               |
| pickle_list          | 4.88 us                                                               | 4.84 us: 1.01x faster                                               |
| unpickle_list        | 5.05 us                                                               | 5.18 us: 1.03x slower                                               |
| Geometric mean       | (ref)                                                                 | 1.03x faster                                                        |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 10.1 ms                                                               | 10.2 ms: 1.01x slower                                               |
| python_startup         | 15.5 ms                                                               | 15.7 ms: 1.01x slower                                               |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|-----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 20.9 ms                                                               | 19.1 ms: 1.09x faster                                               |
| django_template | 65.0 ms                                                               | 62.5 ms: 1.04x faster                                               |
| genshi_xml      | 82.7 ms                                                               | 81.0 ms: 1.02x faster                                               |
| genshi_text     | 39.9 ms                                                               | 40.3 ms: 1.01x slower                                               |
| Geometric mean  | (ref)                                                                 | 1.04x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody                    | 224 ms                                                                | 185 ms: 1.21x faster                                                |
| spectral_norm            | 179 ms                                                                | 148 ms: 1.20x faster                                                |
| scimark_fft              | 456 ms                                                                | 391 ms: 1.17x faster                                                |
| scimark_sparse_mat_mult  | 6.16 ms                                                               | 5.46 ms: 1.13x faster                                               |
| chaos                    | 131 ms                                                                | 117 ms: 1.11x faster                                                |
| bpe_tokeniser            | 6.25 sec                                                              | 5.70 sec: 1.10x faster                                              |
| coroutines               | 32.1 ms                                                               | 29.3 ms: 1.10x faster                                               |
| mako                     | 20.9 ms                                                               | 19.1 ms: 1.09x faster                                               |
| scimark_monte_carlo      | 132 ms                                                                | 122 ms: 1.09x faster                                                |
| deepcopy_memo            | 53.8 us                                                               | 49.8 us: 1.08x faster                                               |
| hexiom                   | 12.4 ms                                                               | 11.6 ms: 1.07x faster                                               |
| pprint_safe_repr         | 1.35 sec                                                              | 1.26 sec: 1.07x faster                                              |
| unpickle_pure_python     | 419 us                                                                | 393 us: 1.07x faster                                                |
| pyflate                  | 795 ms                                                                | 747 ms: 1.06x faster                                                |
| pprint_pformat           | 2.80 sec                                                              | 2.63 sec: 1.06x faster                                              |
| scimark_sor              | 279 ms                                                                | 262 ms: 1.06x faster                                                |
| raytrace                 | 648 ms                                                                | 611 ms: 1.06x faster                                                |
| nqueens                  | 119 ms                                                                | 112 ms: 1.06x faster                                                |
| fannkuch                 | 584 ms                                                                | 553 ms: 1.06x faster                                                |
| float                    | 154 ms                                                                | 146 ms: 1.06x faster                                                |
| sqlite_synth             | 2.51 us                                                               | 2.38 us: 1.06x faster                                               |
| scimark_lu               | 246 ms                                                                | 233 ms: 1.05x faster                                                |
| richards_super           | 110 ms                                                                | 104 ms: 1.05x faster                                                |
| json_loads               | 29.7 us                                                               | 28.2 us: 1.05x faster                                               |
| pickle_pure_python       | 617 us                                                                | 586 us: 1.05x faster                                                |
| coverage                 | 106 ms                                                                | 101 ms: 1.05x faster                                                |
| json                     | 5.44 ms                                                               | 5.20 ms: 1.05x faster                                               |
| deepcopy_reduce          | 4.64 us                                                               | 4.43 us: 1.05x faster                                               |
| richards                 | 89.9 ms                                                               | 86.0 ms: 1.05x faster                                               |
| deepcopy                 | 439 us                                                                | 420 us: 1.04x faster                                                |
| xml_etree_process        | 93.6 ms                                                               | 89.8 ms: 1.04x faster                                               |
| pycparser                | 1.74 sec                                                              | 1.67 sec: 1.04x faster                                              |
| django_template          | 65.0 ms                                                               | 62.5 ms: 1.04x faster                                               |
| deltablue                | 9.05 ms                                                               | 8.71 ms: 1.04x faster                                               |
| xml_etree_generate       | 114 ms                                                                | 110 ms: 1.04x faster                                                |
| xml_etree_iterparse      | 109 ms                                                                | 105 ms: 1.04x faster                                                |
| crypto_pyaes             | 111 ms                                                                | 107 ms: 1.03x faster                                                |
| create_gc_cycles         | 1.13 ms                                                               | 1.10 ms: 1.03x faster                                               |
| regex_compile            | 228 ms                                                                | 221 ms: 1.03x faster                                                |
| sqlglot_normalize        | 179 ms                                                                | 173 ms: 1.03x faster                                                |
| logging_silent           | 215 ns                                                                | 209 ns: 1.03x faster                                                |
| sqlglot_optimize         | 90.0 ms                                                               | 87.3 ms: 1.03x faster                                               |
| comprehensions           | 30.3 us                                                               | 29.5 us: 1.03x faster                                               |
| tomli_loads              | 3.31 sec                                                              | 3.22 sec: 1.03x faster                                              |
| pickle_dict              | 32.4 us                                                               | 31.6 us: 1.03x faster                                               |
| unpack_sequence          | 143 ns                                                                | 140 ns: 1.02x faster                                                |
| genshi_xml               | 82.7 ms                                                               | 81.0 ms: 1.02x faster                                               |
| sympy_integrate          | 32.9 ms                                                               | 32.3 ms: 1.02x faster                                               |
| telco                    | 9.71 ms                                                               | 9.53 ms: 1.02x faster                                               |
| unpickle                 | 14.8 us                                                               | 14.5 us: 1.02x faster                                               |
| xml_etree_parse          | 134 ms                                                                | 132 ms: 1.02x faster                                                |
| go                       | 301 ms                                                                | 296 ms: 1.01x faster                                                |
| sqlglot_parse            | 2.88 ms                                                               | 2.84 ms: 1.01x faster                                               |
| sqlglot_transpile        | 3.33 ms                                                               | 3.29 ms: 1.01x faster                                               |
| json_dumps               | 15.3 ms                                                               | 15.1 ms: 1.01x faster                                               |
| sympy_expand             | 1.06 sec                                                              | 1.04 sec: 1.01x faster                                              |
| docutils                 | 3.32 sec                                                              | 3.28 sec: 1.01x faster                                              |
| pathlib                  | 22.2 ms                                                               | 21.9 ms: 1.01x faster                                               |
| tornado_http             | 163 ms                                                                | 162 ms: 1.01x faster                                                |
| sympy_str                | 539 ms                                                                | 533 ms: 1.01x faster                                                |
| typing_runtime_protocols | 246 us                                                                | 243 us: 1.01x faster                                                |
| dulwich_log              | 104 ms                                                                | 103 ms: 1.01x faster                                                |
| asyncio_websockets       | 523 ms                                                                | 519 ms: 1.01x faster                                                |
| pickle_list              | 4.88 us                                                               | 4.84 us: 1.01x faster                                               |
| 2to3                     | 413 ms                                                                | 411 ms: 1.00x faster                                                |
| pidigits                 | 187 ms                                                                | 186 ms: 1.00x faster                                                |
| genshi_text              | 39.9 ms                                                               | 40.3 ms: 1.01x slower                                               |
| asyncio_tcp              | 575 ms                                                                | 581 ms: 1.01x slower                                                |
| python_startup_no_site   | 10.1 ms                                                               | 10.2 ms: 1.01x slower                                               |
| python_startup           | 15.5 ms                                                               | 15.7 ms: 1.01x slower                                               |
| bench_mp_pool            | 70.7 ms                                                               | 71.7 ms: 1.01x slower                                               |
| thrift                   | 1.26 ms                                                               | 1.28 ms: 1.02x slower                                               |
| logging_simple           | 12.0 us                                                               | 12.3 us: 1.02x slower                                               |
| logging_format           | 13.1 us                                                               | 13.5 us: 1.03x slower                                               |
| unpickle_list            | 5.05 us                                                               | 5.18 us: 1.03x slower                                               |
| gc_traversal             | 2.47 ms                                                               | 2.55 ms: 1.03x slower                                               |
| generators               | 41.5 ms                                                               | 43.0 ms: 1.03x slower                                               |
| mdp                      | 3.07 sec                                                              | 3.21 sec: 1.05x slower                                              |
| regex_effbot             | 2.96 ms                                                               | 3.10 ms: 1.05x slower                                               |
| asyncio_tcp_ssl          | 1.70 sec                                                              | 1.81 sec: 1.06x slower                                              |
| regex_v8                 | 24.5 ms                                                               | 26.1 ms: 1.07x slower                                               |
| async_generators         | 492 ms                                                                | 525 ms: 1.07x slower                                                |
| bench_thread_pool        | 3.17 ms                                                               | 3.48 ms: 1.10x slower                                               |
| regex_dna                | 170 ms                                                                | 190 ms: 1.12x slower                                                |
| Geometric mean           | (ref)                                                                 | 1.03x faster                                                        |

Benchmark hidden because not significant (5): pickle, pylint, html5lib, meteor_contest, sympy_sum

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x