# Building A Standalone Binary

The DevKit [FAQ](https://microsoft.github.io/azure-iot-developer-kit/docs/faq/) provides some general guidance about how to get the boot.bin and python script to merge the binaries together.  I found that the latest version of python required a tweak to the script to make it work.

## Building the Binary

1. Open a WSL session in VSCode.
1. Run the `buildbinary.sh` script to generate the standalone binary.

```bash
./buildbinary.sh
```

1. The output binary, mxchip_mqttsample.bin will be located in the `binary` directory.