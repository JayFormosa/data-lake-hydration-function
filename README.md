# data-lake-hydration-function

An AWS state machine that will hydrate a data lake of options data along with the market data for the underlying security.

![alt text][image-1]

[image-1]: images/state-machine-graph.png "step 1"


```
SELECT * FROM "AwsDataCatalog"."options-data"."options_data_able" 
WHERE col1 LIKE 'TLT220715P%' AND col3 = '133.0' 
ORDER BY col2;
```

refs:

https://docs.aws.amazon.com/step-functions/latest/dg/tutorial-create-iterate-pattern-section.html

https://docs.aws.amazon.com/step-functions/latest/dg/input-output-example.html

https://docs.aws.amazon.com/athena/latest/ug/glue-best-practices.html#schema-csv-headers
