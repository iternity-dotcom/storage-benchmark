# Storage Benchmark

(Originally forked from dvassallo/s3-benchmark)

The performance of a storage system depends on 3 things:
1. Your distance to the storage endpoint.
2. The size of your objects.
3. The number of parallel transfers you can make.

With this tool you can measure the performance of different file and object (S3) operations using different thread counts and object sizes.

## Usage

### Download

#### macOS
```
curl -OL https://github.com/iternity-dotcom/storage-benchmark/raw/master/build/darwin-amd64/storage-benchmark
```

#### Linux 64-bit x86

```
curl -OL https://github.com/iternity-dotcom/storage-benchmark/raw/master/build/linux-amd64/storage-benchmark
```

#### Linux 64-bit ARM

```
curl -OL https://github.com/iternity-dotcom/storage-benchmark/raw/master/build/linux-arm64/storage-benchmark
```

#### Windows 64-bit x86

```
curl -OL https://github.com/iternity-dotcom/storage-benchmark/raw/master/build/windows-amd64/storage-benchmark.exe
```

### S3 Credentials

For testing S3 endpoints the tool needs credentials with full S3 permissions. The tool will try to find the credentials [from the usual places](https://aws.amazon.com/blogs/security/a-new-and-standardized-way-to-manage-credentials-in-the-aws-sdks/).

### Run

Make the file executable:

```
chmod +x storage-benchmark
```

Run the --help command to get an overview of the possible parameters
```
./storage-benchmark --help
```

### Build

1. Install [Go](https://golang.org/)
    ```
    sudo apt-get install golang-go
    ```
    or
    ```
    sudo yum install go
    ```
    may work too. 
    
2. Setup Go environment variables (Usually GOPATH and GOBIN) and test Go installation 
3. Clone the repo
4. Install [```dep```](https://golang.github.io/dep/) 
	```
	go get -u github.com/golang/dep/cmd/dep
	```
5. Go to source directory and run ```dep ensure```
6. Run ```go run main.go```

## License

This project is released under the [MIT License](LICENSE).
