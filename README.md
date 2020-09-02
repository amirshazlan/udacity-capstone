# capstone-project-cloud-devops

<h2>Project Overview</h2>

<p> For the capstone project, I applied the knowledge which I have learned throughout the Cloud DevOps Nanodegree program. Among them are -</p>

<ul>
	<li>Working in AWS</li>
	<li>Using Jenkins to implement Continuous Integration and Continuous Deployment</li>
	<li>Working with CloudFormation to deploy infrastructure</li>
	<li>Building Kubernetes clusters</li>
	<li>Building Docker containers in pipelines</li>
</ul>

***

<p>In this project I developed a CI/CD pipeline for microservices applications with blue/green deployment. What I did was to -</p>

<ul>
	<li>Take an app server and containerized it using Docker</li>
	<li>Push the built Docker images to the Docker Hub</li>
	<li>Lastly use Jenkins Pipeline to deploy the images into a Kubernetes cluster that is hosted in AWS EKS</li>
</ul>

***

<p>Project folder and files structure</p>

<ul>
	<li>AWS - includes eksctl command</li>
	<li>green - image green for blue-green deployment</li>
	<li>blue - image blue for blue-green deployment</li>
	<li>Jenkinsfile - pipeline for the project</li>
	<li>screenshots - images from project building</li>
	<li>blue-green-service.json - service file</li>
</ul>

***

<p>How to build</p>

<ol type='1'>
	<li>Enter into Jenkins instance via SSH and run command to create Kubernates clusters</li>
	<li>After Cloudformation creates resources, run the Jenkins pipeline</li>
	<li>Jenkins pipeline will create Docker images and upload to DockerHub</li>
	<li>Jenkins will pull images from DockerHub and deploy them into pods</li>
	<li>Open page from LoadBalancer link on port 8000</li>
	<li>Update the blue-green service JSON file to redirect service. Jenkins pipeline will run automatically</li>
</ol>
