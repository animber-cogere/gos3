# gos3 : Simple no frills AWS S3 Library using REST with V4 Signing

## Overview [![GoDoc](https://godoc.org/github.com/animber-coder/gos3?status.svg)](https://godoc.org/github.com/animber-coder/gos3) [![Go Report Card](https://goreportcard.com/badge/github.com/animber-coder/gos3)](https://goreportcard.com/report/github.com/animber-coder/gos3)

GoS3 is a golang library for uploading and deleting objects on S3 buckets using the REST API calls signed using AWS Signature Version 4

## Install

```sh
go get github.com/animber-coder/gos3
```

## Example

```go
testTxt, _ := os.Open("test.txt")
defer testTxt.Close()

s3 := gos3.New(Region, AWSAccessKey, AWSSecretKey)
err := s3.FileUpload(gos3.UploadInput{
    Bucket:      AWSBucket,
    ObjectKey:   "test.txt",
    ContentType: "text/plain",
    FileName:    "test.txt",
    Body:        testTxt,
}
```

## Contributing

ToDo.

## Contributors

ToDo.

## Author

ToDo.

## License

MIT.