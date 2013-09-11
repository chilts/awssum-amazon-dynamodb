# awssum-amazon-__SERVICE__ #

This is an ```AwsSum``` plugin!

You'll need to add [awssum-amazon-dynamodb](https://github.com/awssum/awssum-amazon-dynamodb/) to your package.json
dependencies. Both [awssum](https://github.com/awssum/awssum/) and
[awssum-amazon](https://github.com/awssum/awssum-amazon/) are pulled in as peer dependencies.

```
dependencies : {
    "awssum-amazon-dynamodb" : "1.x",
},
```

## Example ##

List all your tables

```
var fmt = require('fmt');
var amazonDynamoDB = require('awssum-amazon-dynamodb');

var dynamodb = new amazonDynamoDB.DynamoDB({
    'accessKeyId'     : process.env.ACCESS_KEY_ID,
    'secretAccessKey' : process.env.SECRET_ACCESS_KEY,
    'region'          : amazonDynamoDB.US_EAST_1
});

dynamodb.ListTables(function(err, data) {
    fmt.dump(err, 'err');
    fmt.dump(data, 'data');
});
```

## Operations ##

* BatchGetItem
* BatchWriteItem
* CreateTable
* DeleteItem
* DeleteTable
* DescribeTable
* GetItem
* ListTables
* PutItem
* Query
* Scan
* UpdateItem
* UpdateTable 

# Author #

Written by [Andrew Chilton](http://chilts.org/) - [Blog](http://chilts.org/blog/) -
[Twitter](https://twitter.com/andychilton).

# License #

* [Copyright 2011-2013 Apps Attic Ltd.  All rights reserved.](http://appsattic.mit-license.org/2011/)
* [Copyright 2013 Andrew Chilton.  All rights reserved.](http://chilts.mit-license.org/2013/)

(Ends)
