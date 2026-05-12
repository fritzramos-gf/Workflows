## 1. Standard GitOps / Staging to Production Workflow

This workflow illustrates a classic **GitOps-based deployment pipeline** from development to production.

### Step-by-Step Process:

1. **Step 1: Developer**  
   Developer starts working on changes or new features.

2. **Step 2: Feature Branch**  
   Work is done in an isolated feature branch.

3. **Step 3: Pull Request**  
   Changes are submitted via a Pull Request for review.

4. **Step 4: AI Agent Code Review & Security Scan**  
   Automated AI review and security scanning is performed.

5. **Step 5: Request Changes** *(if needed)*  
   Issues found by the AI agent are addressed.

6. **Step 6: CI / Automated Tests**  
   Continuous Integration and automated testing run.

7. **Step 7: Human Approval #1**  
   First human review and approval.

8. **Step 8: Main Branch (Single Source of Truth)**  
   Code is merged into the main branch.

9. **Step 9: GitOps Agent Detects Change**  
   GitOps agent identifies the changes in the repository.

10. **Step 10: Deploy to Staging**  
    Changes are automatically deployed to the Staging environment.

11. **Step 11: Staging Tests**  
    Comprehensive tests are executed in the staging environment.

12. **Step 12: Rollback / Fix** *(if failed)*  
    If tests fail, changes are rolled back or fixed.

13. **Step 13: Human Approval #2**  
    Final human approval for production deployment.

14. **Step 14: Sync to Production**  
    GitOps agent synchronizes the approved changes to the Production environment.

15. **Step 15: Production Environment**  
    Changes go live in production.

---

**Notes:**
- Both workflows follow **GitOps principles** (declarative, version-controlled, automated).
- The first workflow is specialized for **Tanium Enforce** policy management with compliance focus.
- The second is a **general software deployment*
