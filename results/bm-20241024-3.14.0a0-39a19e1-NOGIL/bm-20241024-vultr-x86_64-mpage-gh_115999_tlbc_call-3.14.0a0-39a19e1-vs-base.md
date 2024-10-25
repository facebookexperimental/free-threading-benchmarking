# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 39a19e1
- commit date: 2024-10-24
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 413 ms                                                                | 408 ms: 1.01x faster                                                |
| docutils       | 3.32 sec                                                              | 3.25 sec: 1.02x faster                                              |
| html5lib       | 104 ms                                                                | 102 ms: 1.02x faster                                                |
| tornado_http   | 163 ms                                                                | 161 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|--------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| coroutines         | 32.1 ms                                                               | 28.7 ms: 1.12x faster                                               |
| async_generators   | 492 ms                                                                | 487 ms: 1.01x faster                                                |
| asyncio_websockets | 523 ms                                                                | 520 ms: 1.01x faster                                                |
| asyncio_tcp        | 575 ms                                                                | 581 ms: 1.01x slower                                                |
| asyncio_tcp_ssl    | 1.70 sec                                                              | 1.83 sec: 1.07x slower                                              |
| Geometric mean     | (ref)                                                                 | 1.01x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 224 ms                                                                | 187 ms: 1.20x faster                                                |
| float          | 154 ms                                                                | 146 ms: 1.06x faster                                                |
| pidigits       | 187 ms                                                                | 223 ms: 1.19x slower                                                |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 228 ms                                                                | 215 ms: 1.06x faster                                                |
| regex_effbot   | 2.96 ms                                                               | 3.05 ms: 1.03x slower                                               |
| regex_v8       | 24.5 ms                                                               | 25.8 ms: 1.05x slower                                               |
| regex_dna      | 170 ms                                                                | 191 ms: 1.13x slower                                                |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 32.4 us                                                               | 29.7 us: 1.09x faster                                               |
| pickle_pure_python   | 617 us                                                                | 572 us: 1.08x faster                                                |
| unpickle_pure_python | 419 us                                                                | 389 us: 1.08x faster                                                |
| xml_etree_process    | 93.6 ms                                                               | 88.1 ms: 1.06x faster                                               |
| xml_etree_generate   | 114 ms                                                                | 108 ms: 1.06x faster                                                |
| json_loads           | 29.7 us                                                               | 28.2 us: 1.05x faster                                               |
| tomli_loads          | 3.31 sec                                                              | 3.18 sec: 1.04x faster                                              |
| xml_etree_iterparse  | 109 ms                                                                | 106 ms: 1.03x faster                                                |
| pickle_list          | 4.88 us                                                               | 4.74 us: 1.03x faster                                               |
| xml_etree_parse      | 134 ms                                                                | 131 ms: 1.02x faster                                                |
| json_dumps           | 15.3 ms                                                               | 15.1 ms: 1.02x faster                                               |
| unpickle_list        | 5.05 us                                                               | 5.07 us: 1.00x slower                                               |
| Geometric mean       | (ref)                                                                 | 1.04x faster                                                        |

Benchmark hidden because not significant (2): unpickle, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 10.1 ms                                                               | 10.3 ms: 1.02x slower                                               |
| python_startup         | 15.5 ms                                                               | 15.7 ms: 1.02x slower                                               |
| Geometric mean         | (ref)                                                                 | 1.02x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|-----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 20.9 ms                                                               | 19.2 ms: 1.09x faster                                               |
| genshi_xml      | 82.7 ms                                                               | 78.9 ms: 1.05x faster                                               |
| django_template | 65.0 ms                                                               | 62.3 ms: 1.04x faster                                               |
| genshi_text     | 39.9 ms                                                               | 38.8 ms: 1.03x faster                                               |
| Geometric mean  | (ref)                                                                 | 1.05x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|--------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| spectral_norm            | 179 ms                                                                | 147 ms: 1.21x faster                                                |
| nbody                    | 224 ms                                                                | 187 ms: 1.20x faster                                                |
| scimark_fft              | 456 ms                                                                | 387 ms: 1.18x faster                                                |
| chaos                    | 131 ms                                                                | 112 ms: 1.16x faster                                                |
| coroutines               | 32.1 ms                                                               | 28.7 ms: 1.12x faster                                               |
| raytrace                 | 648 ms                                                                | 580 ms: 1.12x faster                                                |
| scimark_sparse_mat_mult  | 6.16 ms                                                               | 5.61 ms: 1.10x faster                                               |
| deepcopy_memo            | 53.8 us                                                               | 49.1 us: 1.09x faster                                               |
| pickle_dict              | 32.4 us                                                               | 29.7 us: 1.09x faster                                               |
| mako                     | 20.9 ms                                                               | 19.2 ms: 1.09x faster                                               |
| pyflate                  | 795 ms                                                                | 735 ms: 1.08x faster                                                |
| deepcopy_reduce          | 4.64 us                                                               | 4.29 us: 1.08x faster                                               |
| pprint_safe_repr         | 1.35 sec                                                              | 1.25 sec: 1.08x faster                                              |
| bpe_tokeniser            | 6.25 sec                                                              | 5.79 sec: 1.08x faster                                              |
| scimark_monte_carlo      | 132 ms                                                                | 122 ms: 1.08x faster                                                |
| pickle_pure_python       | 617 us                                                                | 572 us: 1.08x faster                                                |
| unpickle_pure_python     | 419 us                                                                | 389 us: 1.08x faster                                                |
| pprint_pformat           | 2.80 sec                                                              | 2.60 sec: 1.08x faster                                              |
| scimark_sor              | 279 ms                                                                | 261 ms: 1.07x faster                                                |
| richards_super           | 110 ms                                                                | 103 ms: 1.07x faster                                                |
| deepcopy                 | 439 us                                                                | 411 us: 1.07x faster                                                |
| xml_etree_process        | 93.6 ms                                                               | 88.1 ms: 1.06x faster                                               |
| regex_compile            | 228 ms                                                                | 215 ms: 1.06x faster                                                |
| coverage                 | 106 ms                                                                | 100 ms: 1.06x faster                                                |
| pycparser                | 1.74 sec                                                              | 1.64 sec: 1.06x faster                                              |
| scimark_lu               | 246 ms                                                                | 233 ms: 1.06x faster                                                |
| nqueens                  | 119 ms                                                                | 112 ms: 1.06x faster                                                |
| xml_etree_generate       | 114 ms                                                                | 108 ms: 1.06x faster                                                |
| fannkuch                 | 584 ms                                                                | 554 ms: 1.06x faster                                                |
| float                    | 154 ms                                                                | 146 ms: 1.06x faster                                                |
| hexiom                   | 12.4 ms                                                               | 11.8 ms: 1.05x faster                                               |
| json_loads               | 29.7 us                                                               | 28.2 us: 1.05x faster                                               |
| sqlglot_optimize         | 90.0 ms                                                               | 85.5 ms: 1.05x faster                                               |
| richards                 | 89.9 ms                                                               | 85.4 ms: 1.05x faster                                               |
| deltablue                | 9.05 ms                                                               | 8.61 ms: 1.05x faster                                               |
| genshi_xml               | 82.7 ms                                                               | 78.9 ms: 1.05x faster                                               |
| json                     | 5.44 ms                                                               | 5.20 ms: 1.05x faster                                               |
| unpack_sequence          | 143 ns                                                                | 137 ns: 1.05x faster                                                |
| sqlglot_normalize        | 179 ms                                                                | 171 ms: 1.04x faster                                                |
| django_template          | 65.0 ms                                                               | 62.3 ms: 1.04x faster                                               |
| tomli_loads              | 3.31 sec                                                              | 3.18 sec: 1.04x faster                                              |
| go                       | 301 ms                                                                | 290 ms: 1.04x faster                                                |
| comprehensions           | 30.3 us                                                               | 29.2 us: 1.04x faster                                               |
| xml_etree_iterparse      | 109 ms                                                                | 106 ms: 1.03x faster                                                |
| crypto_pyaes             | 111 ms                                                                | 107 ms: 1.03x faster                                                |
| sqlite_synth             | 2.51 us                                                               | 2.44 us: 1.03x faster                                               |
| genshi_text              | 39.9 ms                                                               | 38.8 ms: 1.03x faster                                               |
| telco                    | 9.71 ms                                                               | 9.43 ms: 1.03x faster                                               |
| pickle_list              | 4.88 us                                                               | 4.74 us: 1.03x faster                                               |
| dulwich_log              | 104 ms                                                                | 101 ms: 1.03x faster                                                |
| logging_silent           | 215 ns                                                                | 210 ns: 1.03x faster                                                |
| typing_runtime_protocols | 246 us                                                                | 240 us: 1.02x faster                                                |
| sympy_str                | 539 ms                                                                | 526 ms: 1.02x faster                                                |
| sympy_integrate          | 32.9 ms                                                               | 32.2 ms: 1.02x faster                                               |
| thrift                   | 1.26 ms                                                               | 1.23 ms: 1.02x faster                                               |
| pathlib                  | 22.2 ms                                                               | 21.6 ms: 1.02x faster                                               |
| docutils                 | 3.32 sec                                                              | 3.25 sec: 1.02x faster                                              |
| sqlglot_parse            | 2.88 ms                                                               | 2.82 ms: 1.02x faster                                               |
| sympy_expand             | 1.06 sec                                                              | 1.03 sec: 1.02x faster                                              |
| meteor_contest           | 139 ms                                                                | 137 ms: 1.02x faster                                                |
| sqlglot_transpile        | 3.33 ms                                                               | 3.26 ms: 1.02x faster                                               |
| html5lib                 | 104 ms                                                                | 102 ms: 1.02x faster                                                |
| xml_etree_parse          | 134 ms                                                                | 131 ms: 1.02x faster                                                |
| tornado_http             | 163 ms                                                                | 161 ms: 1.02x faster                                                |
| json_dumps               | 15.3 ms                                                               | 15.1 ms: 1.02x faster                                               |
| 2to3                     | 413 ms                                                                | 408 ms: 1.01x faster                                                |
| async_generators         | 492 ms                                                                | 487 ms: 1.01x faster                                                |
| logging_simple           | 12.0 us                                                               | 11.9 us: 1.01x faster                                               |
| sympy_sum                | 379 ms                                                                | 376 ms: 1.01x faster                                                |
| asyncio_websockets       | 523 ms                                                                | 520 ms: 1.01x faster                                                |
| unpickle_list            | 5.05 us                                                               | 5.07 us: 1.00x slower                                               |
| generators               | 41.5 ms                                                               | 42.0 ms: 1.01x slower                                               |
| asyncio_tcp              | 575 ms                                                                | 581 ms: 1.01x slower                                                |
| bench_mp_pool            | 70.7 ms                                                               | 71.7 ms: 1.01x slower                                               |
| python_startup_no_site   | 10.1 ms                                                               | 10.3 ms: 1.02x slower                                               |
| python_startup           | 15.5 ms                                                               | 15.7 ms: 1.02x slower                                               |
| regex_effbot             | 2.96 ms                                                               | 3.05 ms: 1.03x slower                                               |
| mdp                      | 3.07 sec                                                              | 3.21 sec: 1.05x slower                                              |
| regex_v8                 | 24.5 ms                                                               | 25.8 ms: 1.05x slower                                               |
| asyncio_tcp_ssl          | 1.70 sec                                                              | 1.83 sec: 1.07x slower                                              |
| bench_thread_pool        | 3.17 ms                                                               | 3.45 ms: 1.09x slower                                               |
| regex_dna                | 170 ms                                                                | 191 ms: 1.13x slower                                                |
| pidigits                 | 187 ms                                                                | 223 ms: 1.19x slower                                                |
| Geometric mean           | (ref)                                                                 | 1.04x faster                                                        |

Benchmark hidden because not significant (6): unpickle, pylint, create_gc_cycles, gc_traversal, logging_format, pickle

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.02x