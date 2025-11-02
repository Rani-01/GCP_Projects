Steps to replicate this projects in Google cloud Console

1. Go to Google cloud console
2. Search for dataflow --> Jobs --> (Enable Dataflow API) --> Create job from template --> Give a job name, region, and template (choose text files from cloud storage to Bigquery)
3. New fields will be present in the options below.
4. First create a new storage bucket by searching for cloud storage(use different tab) --> create bucket --> name, region (create).
5. Upload the files employee_data.csv, bq.json, udf.js into the bucket. This will be used now in the new fileds that are present in dataflow job.
6. Go to dataflow job tab, in the source tab --> browse --> YOUR_BUCKET --> employee_data.csv.
7. similarly, choose target as bq.json
8. Then search for bigquery and open it in new tab and create a new dataset with new name and inside thenew dataset, create new table (choose empty table, give an appropriate table name and leave the column fields empty and save the table)
9. Go to dataflow tab and choose new table that was created as bigquery output table
10. Choose the cloud storage bucket as temp directory for bigquery loading process
11. Choose same bucket as temp location but ise /temp at the end.
12. Go to optional parameters at the bottom, and choose udf.js as javascript udf pah in cloud storage.
13. Finally, select the run job
14. The job should start running and it will take around 5 mins for the c=job to complete.
15. Once the job is completed, you should see the data in the bigquery table you created.


Credits to @vishal-bulbule
link - [YouTube Demos/Dataflow](https://github.com/vishal-bulbule/Learn-Google-Cloud/tree/master/YouTube%20Demos/Dataflow)
