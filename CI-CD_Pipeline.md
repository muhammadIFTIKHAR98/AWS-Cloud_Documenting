## CI/CD
  # WHAT IS CI/CD 
    - Building automated workflows for faster releases.
    - CI/CD stands for Continuous Integration and Continuous Deployment (or Continuous Delivery). 
    - It's a set of practices and tools designed to improve the software development process by automating builds, testing and deployment, enabling you to ship code changes faster and reliably.
    - Continuous Integration (CI) -> Automatically builds, tests and integrates code changes within a shared repository.
    - Continuous Delivery (CD) -> Automatically delivers code changes to production ready environments for approval.
    - Continuous Deployment (CD) -> Automatically Deployes code changes to customers directly.
    - Automation is a core principle for achieving DevOps sucess and CI/CD is a critical component. CI/CD comprises of continuous integration and continuous delivery or continuous deployment.
      put together, they form a "CI/CD Pipeline" - A series of Automated workflows that help DevOps team cut down on manual tasks.
      
  # Continuous Deployment VS. Continuous Delivery
    - When someone says CI/CD, the “CD” they’re referring to is usually continuous delivery, not continuous deployment. 
    - What’s the difference? In a CI/CD pipeline that uses continuous delivery, automation pauses when developers push to production. 
        A human—your operations, security, or compliance team—still needs to manually sign off before final release, adding more delays. On the other hand, 
        continuous deployment automates the entire release process. Code changes are deployed to customers as soon as they pass all the required tests.
    - Continuous deployment is the ultimate example of DevOps automation. That doesn’t mean it’s the only way to do CI/CD, or the “right” way. 
        Since continuous deployment relies on rigorous testing tools and a mature testing culture, most software teams start with continuous delivery and 
        integrate more automated testing over time.

  # Why CI/CD
    - The shortest answer: speed. While faster development is the most well-known benefit of CI/CD, a continuous integration and continuous delivery pipeline enables much more.
      ~ Development velocity: Ongoing feedback allows developers to commit smaller changes more often, versus waiting for one release.
      ~ Stability and reliability: Automated, continuous testing ensures that codebases remain stable and release-ready at any time.
      ~ Business growth: Freed up from manual tasks, organizations can focus resources on innovation, customer satisfaction, and paying down technical debt.

  # Building your CI/CD toolkit
    - Teams make CI/CD part of their development workflow with a combination of automated process, steps, and tools.

        ~ Version control: CI begins in shared repositories, where teams collaborate on code using version control systems (VCS) like Git. 
            A VCS tracks code changes, simplifies reversions, and supports config as code for managing testing and infrastructure. Learn more about version control

        ~ Builds: CI build tools automatically package up files and components into release artifacts and run tests for quality, performance, and other requirements. 
            After clearing required checks, CD tools send builds off to the operations team for further testing and staging. Learn more about CI testing

        ~ Reviews and approvals: Treating code review as a best practice improves code quality, encourages collaboration, and helps even the most experienced developers make better commits. 
            In a CI/CD workflow, teams review and approve code or leverage integrated development environments for pair programming. Learn more about code review
        
        ~ Environments: CI/CD tests and deploys code in environments, from where developers build code to where operations teams make applications publicly available. 
            Environments often have their own specific variables and protection rules to meet security and compliance requirements. Learn more about protected environments.

  # Example CI/CD workflow
    - CI/CD doesn’t have to be complicated, or mean adding a host of tools on top of your current workflow. At mabl, developers deploy to production about 80 times a week 
        using only two CI/CD integrations: The mabl testing suite and GitHub Actions. Here’s how it works. 
        Developers open pull requests to trigger initial builds and unit tests

        1) Approved commits are deployed to a preview environment
        
        2) Custom-built GitHub Actions install the mabl CLI and run headless tests
        
        3) GitHub Apps provide live check results within pull requests
        
        4) Approved commits are merged to the main branch for additional tests or deployed to production.

  # What makes CI/CD successful
    - You’ll find different tools and integrations everywhere you look, but effective CI/CD workflows all share the same markers of success.

        1) Automation: CI/CD can be done manually—but that’s not the goal. A good CI/CD workflow automates builds, testing, 
            and deployment so you have more time for code, not more tasks to do.
  
        2) Transparency: If a build fails, developers need to be able to quickly assess what went wrong and why. Logs, visual workflow builders, 
            and deeply integrated tooling make it easier for developers to troubleshoot, understand complex workflows, and share their status with the larger team.
  
        3) Speed: CI/CD contributes to your overall DevOps performance, particularly speed. DevOps experts gauge speed using two DORA metrics: 
            Lead time for changes (how quickly commits are made to code in production) and deployment frequency (how often you commit code).
  
        4) Resilience: When used with other approaches like test coverage, observability tooling, and feature flags, CI/CD makes software more resistant to errors. 
            DORA measures this stability by tracking mean time to resolution (how quickly incidents are resolved) and change failure rate (the number of software rollbacks).
  
        5) Security: Automation includes security. With DevSecOps gaining traction, a future-proof CI/CD pipeline has checks in place for code and permissions, 
            and provides a virtual paper trail for auditing failures, security breaches, non-compliance events.
  
        6) Scalability: CI/CD isn't just about automation; it's also about ensuring scalability. A robust CI/CD setup should effortlessly expand with your growing development 
            team and project complexity. This means it can efficiently handle increased workloads as your software development efforts grow, maintaining productivity and efficiency.

            
        
