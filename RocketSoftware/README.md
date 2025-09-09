# Module 3: Rocket Software Hands-On

## Setting up Rocket Enterprise Developer
Rocket Enterprise Developer is an IDE for COBOL/PL/I that integrates with AWS.

### Installing IDE
1. Request/download from **Rocket Software portal** (license required).  
2. Install on **Windows/Linux workstation**.  
3. Configure IDE with:
   - COBOL/PL/I compiler settings.  
   - Connection to AWS Mainframe Modernization service.  
   - Local debug environment.  

### Writing & Debugging COBOL Code
- Create a new COBOL project.  
- Add sample COBOL program (e.g., `HELLO.cob`).  
- Compile and debug within IDE.  
- Use step-through debugging and breakpoints.  

### Integration with Git
- Connect IDE to **GitHub** or **AWS CodeCommit**.  
- Enable version control for COBOL source code.  
- Commit, push, and manage branches for collaborative development.  

## Setting up Rocket Enterprise Server
Rocket Enterprise Server is the **COBOL/PL/I runtime** inside AWS M2.

### Deploying on AWS M2 Environment
1. In AWS Console → **Mainframe Modernization → Environments → Create Environment**.  
2. Select **Rocket runtime**.  
3. Choose compute size (e.g., `m5.large`).  
4. Attach IAM role, VPC, subnets, and security groups.  
5. Wait until status = **Available**.  

### Configuring Runtime (COBOL/JCL support)
- Upload COBOL application package (via S3).  
- Configure **JCL scripts** for batch processing.  
- Validate runtime by executing test jobs.  
- Enable database connectivity (Aurora, DynamoDB, etc.).  

##  Using Rocket Analyzer
Rocket Analyzer helps understand legacy code before migration.

### Scanning COBOL/PL/I Applications
- Point Analyzer to application source directory.  
- Generate analysis reports:  
  - Call hierarchy  
  - Data usage  
  - Control flow  

### Identifying Dependencies & Dead Code
- Detect interdependent modules.  
- Highlight unused COBOL programs or variables.  
- Provide migration complexity score.  
- Use reports to plan modernization effort.  

## Building CI/CD with Rocket + AWS CodePipeline
1. **Source**: GitHub / CodeCommit stores COBOL code.  
2. **Build**: AWS CodeBuild compiles COBOL using Rocket Developer tools.  
3. **Deploy**: CodePipeline pushes artifacts to AWS M2 Rocket runtime.  

### Benefits
- Automated builds for COBOL applications.  
- Continuous deployment to Rocket runtime.  
- Integration with testing frameworks.  

**Example Pipeline Flow:**
```bash
GitHub → CodeBuild (Rocket COBOL compile) → Deploy to M2 Runtime → CloudWatch Monitoring
```


