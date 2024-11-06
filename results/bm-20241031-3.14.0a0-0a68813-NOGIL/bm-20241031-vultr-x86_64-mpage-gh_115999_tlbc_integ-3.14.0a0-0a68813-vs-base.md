# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_integ
- machine: linux-x86_64
- commit hash: 0a68813
- commit date: 2024-10-31
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 413 ms                                                                | 407 ms: 1.01x faster                                                 |
| docutils       | 3.32 sec                                                              | 3.20 sec: 1.04x faster                                               |
| html5lib       | 104 ms                                                                | 101 ms: 1.03x faster                                                 |
| tornado_http   | 163 ms                                                                | 159 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines         | 32.1 ms                                                               | 26.9 ms: 1.20x faster                                                |
| asyncio_websockets | 523 ms                                                                | 518 ms: 1.01x faster                                                 |
| async_generators   | 492 ms                                                                | 489 ms: 1.01x faster                                                 |
| asyncio_tcp        | 575 ms                                                                | 582 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl    | 1.70 sec                                                              | 1.80 sec: 1.06x slower                                               |
| Geometric mean     | (ref)                                                                 | 1.03x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 224 ms                                                                | 191 ms: 1.18x faster                                                 |
| float          | 154 ms                                                                | 144 ms: 1.07x faster                                                 |
| pidigits       | 187 ms                                                                | 183 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.09x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 228 ms                                                                | 201 ms: 1.14x faster                                                 |
| regex_v8       | 24.5 ms                                                               | 25.9 ms: 1.06x slower                                                |
| regex_effbot   | 2.96 ms                                                               | 3.15 ms: 1.06x slower                                                |
| regex_dna      | 170 ms                                                                | 188 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 419 us                                                                | 353 us: 1.18x faster                                                 |
| pickle_pure_python   | 617 us                                                                | 530 us: 1.16x faster                                                 |
| xml_etree_generate   | 114 ms                                                                | 104 ms: 1.10x faster                                                 |
| xml_etree_process    | 93.6 ms                                                               | 85.2 ms: 1.10x faster                                                |
| xml_etree_iterparse  | 109 ms                                                                | 100 ms: 1.09x faster                                                 |
| tomli_loads          | 3.31 sec                                                              | 3.07 sec: 1.08x faster                                               |
| pickle               | 11.0 us                                                               | 10.4 us: 1.06x faster                                                |
| json_dumps           | 15.3 ms                                                               | 14.6 ms: 1.05x faster                                                |
| pickle_dict          | 32.4 us                                                               | 31.1 us: 1.04x faster                                                |
| json_loads           | 29.7 us                                                               | 28.7 us: 1.03x faster                                                |
| pickle_list          | 4.88 us                                                               | 4.79 us: 1.02x faster                                                |
| unpickle_list        | 5.05 us                                                               | 5.16 us: 1.02x slower                                                |
| Geometric mean       | (ref)                                                                 | 1.06x faster                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 15.5 ms                                                               | 15.8 ms: 1.02x slower                                                |
| python_startup_no_site | 10.1 ms                                                               | 10.3 ms: 1.02x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.02x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 65.0 ms                                                               | 56.5 ms: 1.15x faster                                                |
| genshi_xml      | 82.7 ms                                                               | 73.3 ms: 1.13x faster                                                |
| mako            | 20.9 ms                                                               | 18.6 ms: 1.13x faster                                                |
| genshi_text     | 39.9 ms                                                               | 35.6 ms: 1.12x faster                                                |
| Geometric mean  | (ref)                                                                 | 1.13x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| deepcopy_memo            | 53.8 us                                                               | 42.7 us: 1.26x faster                                                |
| pprint_safe_repr         | 1.35 sec                                                              | 1.09 sec: 1.24x faster                                               |
| deepcopy_reduce          | 4.64 us                                                               | 3.77 us: 1.23x faster                                                |
| pprint_pformat           | 2.80 sec                                                              | 2.28 sec: 1.23x faster                                               |
| scimark_lu               | 246 ms                                                                | 202 ms: 1.22x faster                                                 |
| spectral_norm            | 179 ms                                                                | 147 ms: 1.21x faster                                                 |
| deepcopy                 | 439 us                                                                | 362 us: 1.21x faster                                                 |
| coroutines               | 32.1 ms                                                               | 26.9 ms: 1.20x faster                                                |
| typing_runtime_protocols | 246 us                                                                | 207 us: 1.19x faster                                                 |
| unpickle_pure_python     | 419 us                                                                | 353 us: 1.18x faster                                                 |
| nbody                    | 224 ms                                                                | 191 ms: 1.18x faster                                                 |
| sqlglot_normalize        | 179 ms                                                                | 152 ms: 1.17x faster                                                 |
| chaos                    | 131 ms                                                                | 112 ms: 1.17x faster                                                 |
| sqlglot_optimize         | 90.0 ms                                                               | 76.9 ms: 1.17x faster                                                |
| pickle_pure_python       | 617 us                                                                | 530 us: 1.16x faster                                                 |
| bpe_tokeniser            | 6.25 sec                                                              | 5.38 sec: 1.16x faster                                               |
| django_template          | 65.0 ms                                                               | 56.5 ms: 1.15x faster                                                |
| scimark_fft              | 456 ms                                                                | 400 ms: 1.14x faster                                                 |
| regex_compile            | 228 ms                                                                | 201 ms: 1.14x faster                                                 |
| genshi_xml               | 82.7 ms                                                               | 73.3 ms: 1.13x faster                                                |
| mako                     | 20.9 ms                                                               | 18.6 ms: 1.13x faster                                                |
| raytrace                 | 648 ms                                                                | 577 ms: 1.12x faster                                                 |
| genshi_text              | 39.9 ms                                                               | 35.6 ms: 1.12x faster                                                |
| hexiom                   | 12.4 ms                                                               | 11.2 ms: 1.11x faster                                                |
| scimark_sparse_mat_mult  | 6.16 ms                                                               | 5.54 ms: 1.11x faster                                                |
| richards_super           | 110 ms                                                                | 99.7 ms: 1.10x faster                                                |
| xml_etree_generate       | 114 ms                                                                | 104 ms: 1.10x faster                                                 |
| scimark_monte_carlo      | 132 ms                                                                | 120 ms: 1.10x faster                                                 |
| xml_etree_process        | 93.6 ms                                                               | 85.2 ms: 1.10x faster                                                |
| xml_etree_iterparse      | 109 ms                                                                | 100 ms: 1.09x faster                                                 |
| richards                 | 89.9 ms                                                               | 82.6 ms: 1.09x faster                                                |
| nqueens                  | 119 ms                                                                | 110 ms: 1.08x faster                                                 |
| logging_silent           | 215 ns                                                                | 199 ns: 1.08x faster                                                 |
| tomli_loads              | 3.31 sec                                                              | 3.07 sec: 1.08x faster                                               |
| deltablue                | 9.05 ms                                                               | 8.43 ms: 1.07x faster                                                |
| pyflate                  | 795 ms                                                                | 741 ms: 1.07x faster                                                 |
| float                    | 154 ms                                                                | 144 ms: 1.07x faster                                                 |
| sqlite_synth             | 2.51 us                                                               | 2.36 us: 1.06x faster                                                |
| pycparser                | 1.74 sec                                                              | 1.64 sec: 1.06x faster                                               |
| coverage                 | 106 ms                                                                | 99.8 ms: 1.06x faster                                                |
| scimark_sor              | 279 ms                                                                | 264 ms: 1.06x faster                                                 |
| pickle                   | 11.0 us                                                               | 10.4 us: 1.06x faster                                                |
| comprehensions           | 30.3 us                                                               | 28.8 us: 1.05x faster                                                |
| sympy_integrate          | 32.9 ms                                                               | 31.3 ms: 1.05x faster                                                |
| sympy_str                | 539 ms                                                                | 513 ms: 1.05x faster                                                 |
| logging_simple           | 12.0 us                                                               | 11.4 us: 1.05x faster                                                |
| json_dumps               | 15.3 ms                                                               | 14.6 ms: 1.05x faster                                                |
| logging_format           | 13.1 us                                                               | 12.5 us: 1.05x faster                                                |
| pathlib                  | 22.2 ms                                                               | 21.1 ms: 1.05x faster                                                |
| meteor_contest           | 139 ms                                                                | 133 ms: 1.05x faster                                                 |
| sympy_expand             | 1.06 sec                                                              | 1.01 sec: 1.05x faster                                               |
| json                     | 5.44 ms                                                               | 5.22 ms: 1.04x faster                                                |
| go                       | 301 ms                                                                | 288 ms: 1.04x faster                                                 |
| pickle_dict              | 32.4 us                                                               | 31.1 us: 1.04x faster                                                |
| fannkuch                 | 584 ms                                                                | 561 ms: 1.04x faster                                                 |
| sqlglot_transpile        | 3.33 ms                                                               | 3.20 ms: 1.04x faster                                                |
| pylint                   | 416 ms                                                                | 400 ms: 1.04x faster                                                 |
| docutils                 | 3.32 sec                                                              | 3.20 sec: 1.04x faster                                               |
| sqlglot_parse            | 2.88 ms                                                               | 2.78 ms: 1.04x faster                                                |
| thrift                   | 1.26 ms                                                               | 1.22 ms: 1.04x faster                                                |
| json_loads               | 29.7 us                                                               | 28.7 us: 1.03x faster                                                |
| dulwich_log              | 104 ms                                                                | 100 ms: 1.03x faster                                                 |
| sympy_sum                | 379 ms                                                                | 367 ms: 1.03x faster                                                 |
| tornado_http             | 163 ms                                                                | 159 ms: 1.03x faster                                                 |
| html5lib                 | 104 ms                                                                | 101 ms: 1.03x faster                                                 |
| crypto_pyaes             | 111 ms                                                                | 107 ms: 1.03x faster                                                 |
| pidigits                 | 187 ms                                                                | 183 ms: 1.02x faster                                                 |
| telco                    | 9.71 ms                                                               | 9.52 ms: 1.02x faster                                                |
| pickle_list              | 4.88 us                                                               | 4.79 us: 1.02x faster                                                |
| 2to3                     | 413 ms                                                                | 407 ms: 1.01x faster                                                 |
| unpack_sequence          | 143 ns                                                                | 142 ns: 1.01x faster                                                 |
| asyncio_websockets       | 523 ms                                                                | 518 ms: 1.01x faster                                                 |
| async_generators         | 492 ms                                                                | 489 ms: 1.01x faster                                                 |
| asyncio_tcp              | 575 ms                                                                | 582 ms: 1.01x slower                                                 |
| bench_mp_pool            | 70.7 ms                                                               | 71.7 ms: 1.01x slower                                                |
| python_startup           | 15.5 ms                                                               | 15.8 ms: 1.02x slower                                                |
| python_startup_no_site   | 10.1 ms                                                               | 10.3 ms: 1.02x slower                                                |
| generators               | 41.5 ms                                                               | 42.5 ms: 1.02x slower                                                |
| unpickle_list            | 5.05 us                                                               | 5.16 us: 1.02x slower                                                |
| mdp                      | 3.07 sec                                                              | 3.15 sec: 1.03x slower                                               |
| regex_v8                 | 24.5 ms                                                               | 25.9 ms: 1.06x slower                                                |
| asyncio_tcp_ssl          | 1.70 sec                                                              | 1.80 sec: 1.06x slower                                               |
| regex_effbot             | 2.96 ms                                                               | 3.15 ms: 1.06x slower                                                |
| bench_thread_pool        | 3.17 ms                                                               | 3.44 ms: 1.09x slower                                                |
| regex_dna                | 170 ms                                                                | 188 ms: 1.11x slower                                                 |
| Geometric mean           | (ref)                                                                 | 1.07x faster                                                         |

Benchmark hidden because not significant (4): create_gc_cycles, xml_etree_parse, gc_traversal, unpickle

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.03x