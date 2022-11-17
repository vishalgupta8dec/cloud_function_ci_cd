Deploy cloud function:
    gcloud builds submit --config cloudbuild.yaml

Test Cloud Function Command Line:
    curl -m 70 -X POST https://us-central1-marine-foundry-355407.cloudfunctions.net/hello_world -H "Authorization: bearer $(gcloud auth print-identity-token)" -H "Content-Type: application/json" -d '{}'