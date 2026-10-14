# ULX3S Constraint Files

Copied from [emard/ulx3s/doc/constraints](https://github.com/emard/ulx3s/tree/master/doc/constraints) 

located in `tt-support-tools` (https://github.com/ulx3s/tt-support-tools/tree/experimental/fpga/ulx3s)

Note that minor changes have been made in [ulx3s_v20.lpf](./ulx3s_v20.lpf) vs [the original](./ulx3s_v20_original.lpf)

| original                                                       | modified                                                       | description                             |
|----------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------|
| FREQUENCY PORT "gn[12]" 50 MHZ;                                | # FREQUENCY PORT "gn[12]" 50 MHZ;                              | commented out, duplicate. see line 393  |
| FREQUENCY PORT "gn12" 50 MHZ;                                  | # FREQUENCY PORT "gn12" 50 MHZ;                                | commented out, duplicate. see line 393  |
| IOBUF  PORT "shutdown" PULLMODE=DOWN IO_TYPE=LVCMOS33 DRIVE=4; | IOBUF  PORT "shutdown" PULLMODE=DOWN IO_TYPE=LVCMOS33 DRIVE=4; | not change, added final LF              |

## OSS CAD Suite version

The optional `oss-cad-suite-version` input defaults to `2026-07-20`.
Override it in the calling workflow if a different available release is required:

```yaml
with:
  oss-cad-suite-version: '2026-07-20'
```

The OSS CAD Suite setup uses the calling workflow's GitHub token for authenticated GitHub API requests.
