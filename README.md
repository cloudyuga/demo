# Upstream project
https://github.com/apache/incubator-openwhisk-deploy-openshift

# Deploying OpenWhisk with ephemeral storage
oc process -f https://gitlab.com/opendatahub/serverless/raw/master/templates/template.yml | oc create -f -

# Deploying OpenWhisk with persistent storage
oc process -f https://gitlab.com/opendatahub/serverless/raw/master/templates/persistent-template.yml | oc create -f -

# Deploying OpenWhisk with persistent storage for a larger environment
oc process -f https://gitlab.com/opendatahub/serverless/raw/master/templates/persistent-template.yml --param-file=https://gitlab.com/opendatahub/serverless/raw/master/templates/larger.env | oc create -f -
