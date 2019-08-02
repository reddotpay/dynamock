# dynamock
--
    import "github.com/reddotpay/dynamock"


## Usage

#### type BatchGetItemExpectation

```go
type BatchGetItemExpectation struct {
}
```

BatchGetItemExpectation struct hold expectation field, err, and result

#### func (*BatchGetItemExpectation) WillReturns

```go
func (e *BatchGetItemExpectation) WillReturns(res dynamodb.BatchGetItemOutput) *BatchGetItemExpectation
```
WillReturns - method for set desired result

#### func (*BatchGetItemExpectation) WithRequest

```go
func (e *BatchGetItemExpectation) WithRequest(input map[string]*dynamodb.KeysAndAttributes) *BatchGetItemExpectation
```
WithRequest - method for set Request expectation

#### type BatchWriteItemExpectation

```go
type BatchWriteItemExpectation struct {
}
```

BatchWriteItemExpectation struct hold expectation field, err, and result

#### func (*BatchWriteItemExpectation) WillReturns

```go
func (e *BatchWriteItemExpectation) WillReturns(res dynamodb.BatchWriteItemOutput) *BatchWriteItemExpectation
```
WillReturns - method for set desired result

#### func (*BatchWriteItemExpectation) WithRequest

```go
func (e *BatchWriteItemExpectation) WithRequest(input map[string][]*dynamodb.WriteRequest) *BatchWriteItemExpectation
```
WithRequest - method for set Request expectation

#### type CreateTableExpectation

```go
type CreateTableExpectation struct {
}
```

CreateTableExpectation struct hold expectation field, err, and result

#### func (*CreateTableExpectation) KeySchema

```go
func (e *CreateTableExpectation) KeySchema(keySchema []*dynamodb.KeySchemaElement) *CreateTableExpectation
```
KeySchema - method for set KeySchema expectation

#### func (*CreateTableExpectation) Name

```go
func (e *CreateTableExpectation) Name(table string) *CreateTableExpectation
```
Name - method for set Name expectation

#### func (*CreateTableExpectation) WillReturns

```go
func (e *CreateTableExpectation) WillReturns(res dynamodb.CreateTableOutput) *CreateTableExpectation
```
WillReturns - method for set desired result

#### type DeleteItemExpectation

```go
type DeleteItemExpectation struct {
}
```

DeleteItemExpectation struct hold expectation field, err, and result

#### func (*DeleteItemExpectation) ToTable

```go
func (e *DeleteItemExpectation) ToTable(table string) *DeleteItemExpectation
```
ToTable - method for set Table expectation

#### func (*DeleteItemExpectation) WillReturns

```go
func (e *DeleteItemExpectation) WillReturns(res dynamodb.DeleteItemOutput) *DeleteItemExpectation
```
WillReturns - method for set desired result

#### func (*DeleteItemExpectation) WithKeys

```go
func (e *DeleteItemExpectation) WithKeys(keys map[string]*dynamodb.AttributeValue) *DeleteItemExpectation
```
WithKeys - method for set Keys expectation

#### type DescribeTableExpectation

```go
type DescribeTableExpectation struct {
}
```

DescribeTableExpectation struct hold expectation field, err, and result

#### func (*DescribeTableExpectation) Table

```go
func (e *DescribeTableExpectation) Table(table string) *DescribeTableExpectation
```
Table - method for set Table expectation

#### func (*DescribeTableExpectation) WillReturns

```go
func (e *DescribeTableExpectation) WillReturns(res dynamodb.DescribeTableOutput) *DescribeTableExpectation
```
WillReturns - method for set desired result

#### type DynaMock

```go
type DynaMock struct {
	GetItemExpect        []GetItemExpectation
	BatchGetItemExpect   []BatchGetItemExpectation
	UpdateItemExpect     []UpdateItemExpectation
	PutItemExpect        []PutItemExpectation
	DeleteItemExpect     []DeleteItemExpectation
	BatchWriteItemExpect []BatchWriteItemExpectation
	CreateTableExpect    []CreateTableExpectation
	DescribeTableExpect  []DescribeTableExpectation
	WaitTableExistExpect []WaitTableExistExpectation
	ScanExpect           []ScanExpectation
	QueryExpect          []QueryExpectation
}
```

DynaMock mock struct hold all expectation types

#### func  New

```go
func New() (dynamodbiface.DynamoDBAPI, *DynaMock)
```
New - constructor for mock instantiation Return : 1st => DynamoDBAPI
implementation, used to inject app object

    2nd => mock object, used to set expectation and desired result

#### func (*DynaMock) ExpectBatchGetItem

```go
func (e *DynaMock) ExpectBatchGetItem() *BatchGetItemExpectation
```
ExpectBatchGetItem - method to start do expectation

#### func (*DynaMock) ExpectBatchWriteItem

```go
func (e *DynaMock) ExpectBatchWriteItem() *BatchWriteItemExpectation
```
ExpectBatchWriteItem - method to start do expectation

#### func (*DynaMock) ExpectCreateTable

```go
func (e *DynaMock) ExpectCreateTable() *CreateTableExpectation
```
ExpectCreateTable - method to start do expectation

#### func (*DynaMock) ExpectDeleteItem

```go
func (e *DynaMock) ExpectDeleteItem() *DeleteItemExpectation
```
ExpectDeleteItem - method to start do expectation

#### func (*DynaMock) ExpectDescribeTable

```go
func (e *DynaMock) ExpectDescribeTable() *DescribeTableExpectation
```
ExpectDescribeTable - method to start do expectation

#### func (*DynaMock) ExpectGetItem

```go
func (e *DynaMock) ExpectGetItem() *GetItemExpectation
```
ExpectGetItem - method to start do expectation

#### func (*DynaMock) ExpectPutItem

```go
func (e *DynaMock) ExpectPutItem() *PutItemExpectation
```
ExpectPutItem - method to start do expectation

#### func (*DynaMock) ExpectQuery

```go
func (e *DynaMock) ExpectQuery() *QueryExpectation
```
ExpectQuery - method to start do expectation

#### func (*DynaMock) ExpectScan

```go
func (e *DynaMock) ExpectScan() *ScanExpectation
```
ExpectScan - method to start do expectation

#### func (*DynaMock) ExpectUpdateItem

```go
func (e *DynaMock) ExpectUpdateItem() *UpdateItemExpectation
```
ExpectUpdateItem - method to start do expectation

#### func (*DynaMock) ExpectWaitTableExist

```go
func (e *DynaMock) ExpectWaitTableExist() *WaitTableExistExpectation
```
ExpectWaitTableExist - method to start do expectation

#### type GetItemExpectation

```go
type GetItemExpectation struct {
}
```

GetItemExpectation struct hold expectation field, err, and result

#### func (*GetItemExpectation) ToTable

```go
func (e *GetItemExpectation) ToTable(table string) *GetItemExpectation
```
ToTable - method for set Table expectation

#### func (*GetItemExpectation) WillReturns

```go
func (e *GetItemExpectation) WillReturns(res dynamodb.GetItemOutput) *GetItemExpectation
```
WillReturns - method for set desired result

#### func (*GetItemExpectation) WithKeys

```go
func (e *GetItemExpectation) WithKeys(keys map[string]*dynamodb.AttributeValue) *GetItemExpectation
```
WithKeys - method for set Keys expectation

#### type MockDynamoDB

```go
type MockDynamoDB struct {
	dynamodbiface.DynamoDBAPI
}
```

MockDynamoDB struct hold DynamoDBAPI implementation and mock object

#### func (*MockDynamoDB) BatchGetItem

```go
func (e *MockDynamoDB) BatchGetItem(input *dynamodb.BatchGetItemInput) (*dynamodb.BatchGetItemOutput, error)
```
BatchGetItem - this func will be invoked when test running matching expectation
with actual input

#### func (*MockDynamoDB) BatchGetItemWithContext

```go
func (e *MockDynamoDB) BatchGetItemWithContext(ctx aws.Context, input *dynamodb.BatchGetItemInput, opt ...request.Option) (*dynamodb.BatchGetItemOutput, error)
```
BatchGetItemWithContext - this func will be invoked when test running matching
expectation with actual input

#### func (*MockDynamoDB) BatchWriteItem

```go
func (e *MockDynamoDB) BatchWriteItem(input *dynamodb.BatchWriteItemInput) (*dynamodb.BatchWriteItemOutput, error)
```
BatchWriteItem - this func will be invoked when test running matching
expectation with actual input

#### func (*MockDynamoDB) CreateTable

```go
func (e *MockDynamoDB) CreateTable(input *dynamodb.CreateTableInput) (*dynamodb.CreateTableOutput, error)
```
CreateTable - this func will be invoked when test running matching expectation
with actual input

#### func (*MockDynamoDB) DeleteItem

```go
func (e *MockDynamoDB) DeleteItem(input *dynamodb.DeleteItemInput) (*dynamodb.DeleteItemOutput, error)
```
DeleteItem - this func will be invoked when test running matching expectation
with actual input

#### func (*MockDynamoDB) DeleteItemWithContext

```go
func (e *MockDynamoDB) DeleteItemWithContext(ctx aws.Context, input *dynamodb.DeleteItemInput, options ...request.Option) (*dynamodb.DeleteItemOutput, error)
```
DeleteItemWithContext - this func will be invoked when test running matching
expectation with actual input

#### func (*MockDynamoDB) DescribeTable

```go
func (e *MockDynamoDB) DescribeTable(input *dynamodb.DescribeTableInput) (*dynamodb.DescribeTableOutput, error)
```
DescribeTable - this func will be invoked when test running matching expectation
with actual input

#### func (*MockDynamoDB) GetItem

```go
func (e *MockDynamoDB) GetItem(input *dynamodb.GetItemInput) (*dynamodb.GetItemOutput, error)
```
GetItem - this func will be invoked when test running matching expectation with
actual input

#### func (*MockDynamoDB) GetItemWithContext

```go
func (e *MockDynamoDB) GetItemWithContext(ctx aws.Context, input *dynamodb.GetItemInput, opt ...request.Option) (*dynamodb.GetItemOutput, error)
```
GetItemWithContext - this func will be invoked when test running matching
expectation with actual input

#### func (*MockDynamoDB) PutItem

```go
func (e *MockDynamoDB) PutItem(input *dynamodb.PutItemInput) (*dynamodb.PutItemOutput, error)
```
PutItem - this func will be invoked when test running matching expectation with
actual input

#### func (*MockDynamoDB) PutItemWithContext

```go
func (e *MockDynamoDB) PutItemWithContext(ctx aws.Context, input *dynamodb.PutItemInput, opt ...request.Option) (*dynamodb.PutItemOutput, error)
```
PutItemWithContext - this func will be invoked when test running matching
expectation with actual input

#### func (*MockDynamoDB) Query

```go
func (e *MockDynamoDB) Query(input *dynamodb.QueryInput) (*dynamodb.QueryOutput, error)
```
Query - this func will be invoked when test running matching expectation with
actual input

#### func (*MockDynamoDB) QueryWithContext

```go
func (e *MockDynamoDB) QueryWithContext(ctx aws.Context, input *dynamodb.QueryInput, options ...request.Option) (*dynamodb.QueryOutput, error)
```
QueryWithContext - this func will be invoked when test running matching
expectation with actual input

#### func (*MockDynamoDB) Scan

```go
func (e *MockDynamoDB) Scan(input *dynamodb.ScanInput) (*dynamodb.ScanOutput, error)
```
Scan - this func will be invoked when test running matching expectation with
actual input

#### func (*MockDynamoDB) UpdateItem

```go
func (e *MockDynamoDB) UpdateItem(input *dynamodb.UpdateItemInput) (*dynamodb.UpdateItemOutput, error)
```
UpdateItem - this func will be invoked when test running matching expectation
with actual input

#### func (*MockDynamoDB) UpdateItemWithContext

```go
func (e *MockDynamoDB) UpdateItemWithContext(ctx aws.Context, input *dynamodb.UpdateItemInput, opt ...request.Option) (*dynamodb.UpdateItemOutput, error)
```
UpdateItemWithContext - this func will be invoked when test running matching
expectation with actual input

#### func (*MockDynamoDB) WaitUntilTableExists

```go
func (e *MockDynamoDB) WaitUntilTableExists(input *dynamodb.DescribeTableInput) error
```
WaitUntilTableExists - this func will be invoked when test running matching
expectation with actual input

#### type PutItemExpectation

```go
type PutItemExpectation struct {
}
```

PutItemExpectation struct hold expectation field, err, and result

#### func (*PutItemExpectation) ToTable

```go
func (e *PutItemExpectation) ToTable(table string) *PutItemExpectation
```
ToTable - method for set Table expectation

#### func (*PutItemExpectation) WillReturns

```go
func (e *PutItemExpectation) WillReturns(res dynamodb.PutItemOutput) *PutItemExpectation
```
WillReturns - method for set desired result

#### func (*PutItemExpectation) WithItems

```go
func (e *PutItemExpectation) WithItems(item map[string]*dynamodb.AttributeValue) *PutItemExpectation
```
WithItems - method for set Items expectation

#### type QueryExpectation

```go
type QueryExpectation struct {
}
```

QueryExpectation struct hold expectation field, err, and result

#### func (*QueryExpectation) Table

```go
func (e *QueryExpectation) Table(table string) *QueryExpectation
```
Table - method for set Table expectation

#### func (*QueryExpectation) WillReturns

```go
func (e *QueryExpectation) WillReturns(res dynamodb.QueryOutput) *QueryExpectation
```
WillReturns - method for set desired result

#### type ScanExpectation

```go
type ScanExpectation struct {
}
```

ScanExpectation struct hold expectation field, err, and result

#### func (*ScanExpectation) Table

```go
func (e *ScanExpectation) Table(table string) *ScanExpectation
```
Table - method for set Table expectation

#### func (*ScanExpectation) WillReturns

```go
func (e *ScanExpectation) WillReturns(res dynamodb.ScanOutput) *ScanExpectation
```
WillReturns - method for set desired result

#### type UpdateItemExpectation

```go
type UpdateItemExpectation struct {
}
```

UpdateItemExpectation struct hold expectation field, err, and result

#### func (*UpdateItemExpectation) ToTable

```go
func (e *UpdateItemExpectation) ToTable(table string) *UpdateItemExpectation
```
ToTable - method for set Table expectation

#### func (*UpdateItemExpectation) Updates

```go
func (e *UpdateItemExpectation) Updates(attrs map[string]*dynamodb.AttributeValueUpdate) *UpdateItemExpectation
```
Updates - method for set Updates expectation

#### func (*UpdateItemExpectation) WillReturns

```go
func (e *UpdateItemExpectation) WillReturns(res dynamodb.UpdateItemOutput) *UpdateItemExpectation
```
WillReturns - method for set desired result

#### func (*UpdateItemExpectation) WithKeys

```go
func (e *UpdateItemExpectation) WithKeys(keys map[string]*dynamodb.AttributeValue) *UpdateItemExpectation
```
WithKeys - method for set Keys expectation

#### type WaitTableExistExpectation

```go
type WaitTableExistExpectation struct {
}
```

WaitTableExistExpectation struct hold expectation field, err, and result

#### func (*WaitTableExistExpectation) Table

```go
func (e *WaitTableExistExpectation) Table(table string) *WaitTableExistExpectation
```
Table - method for set Table expectation

#### func (*WaitTableExistExpectation) WillReturns

```go
func (e *WaitTableExistExpectation) WillReturns(err error) *WaitTableExistExpectation
```
WillReturns - method for set desired result
