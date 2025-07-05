// without multi branch pipelines.
// @Library('jenkins-shared-library')

// //create variable of map type and set the values
// def configMap =[
//     type: "nodejsEKS",
//     component: "frontend",
//     project: "expense"
// ]

// pipelineDecision.decidePipeline(configMap)


//with multi branch pipelines.
@Library('expense-jenkins-shared-library')

//create variable of map type and set the values
def configMap =[
    type: "nodejsEKS",
    component: "frontend",
    project: "expense"
]
//Here ‘!’ is for not equal to main branch, means 
if(!env.BRANCH_NAME.equalsIgnoreCase('main')){
    pipelineDecision.decidePipeline(configMap)   //for non-prod pipeline like feature branch pipelines.
}
else{
    echo "Proceed with CR or NON-PROD pipeline" //for Prod pipelines
}