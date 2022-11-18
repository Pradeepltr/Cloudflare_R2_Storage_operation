 ### **R2 Image storage operation**
 You can add image in Cloudflare R2 database and also retrive your image with the help of your file name.

 >>#### **Steps**
 >>> **Step 1**
 >>>>Create Worker and R2 bucket

 >>>>>CLI Command:
 >>>>>>For Worker - *wrangler init*
 
 >>>>>>For R2 bucket - *wrangler r2 bucket create <YOUR_BUCKET_NAME>*

 >>> **Step 2**
 >>>>Need to bind R2 bucket with worker for access R2 database through worker
 >>>>>***[[r2_buckets]]***

 >>>>>***binding = "worker_variable_name"***
 
 >>>>>***bucket_name = "R2_bucket_name"***

 >>>>Put above binding configuration in wrangler.toml file for bindind worker with R2 Storage.

 >>#### **For input**
 >>>Endpoint - *r2_demo.pk6361439.workers.dev?filename=your_filename*
 >>>>Method - PUT
 
 >>>>body data - binary data

 >>#### **For get your file with the help of file name**
 >>>Endpoint - *r2_demo.pk6361439.workers.dev?filename=your_filename*
 >>>>Method - GET
 ### **Command for see all R2 bucket list**
 >> *wrangler r2 bucket list*
