# StackHawk Security Status Report

**Generated:** 2025-11-13  
**Organization ID:** cab1a6e8-1e1b-4865-8739-abbadefe57b2

## Executive Summary

This report provides a comprehensive overview of the current security status of applications monitored by StackHawk.

### Overall Security Status

- **Total Applications:** 21
- **High Risk Applications:** 1
- **Low Risk Applications:** 20
- **Sensitive Data Findings:** 0 (in last 30 days)
- **Current Repository (mcp-registry):** Not monitored by StackHawk

## Application Risk Breakdown

### High Risk Applications (Requires Immediate Attention)

1. **javaspringvulny** (ID: 68364212-549b-43cb-9062-1aaaffc7216c)
   - Risk Level: HIGH
   - Status: ACTIVE
   - Data Type: NONE
   - Application Type: STANDARD
   - **Action Required:** Review and remediate vulnerabilities immediately

### Low Risk Applications

The following 20 applications are currently classified as LOW risk:

1. **ADO JavaSpringVulny** (ID: dde157fb-70e9-4f1b-8cf2-f6c56fbbb514)
   - Status: ACTIVE
   - Data Type: NONE

2. **authelia** (ID: f1596be5-095b-4631-be1c-e5642cf4f137)
   - Status: ENV_INCOMPLETE
   - Data Type: NONE

3. **django-DefectDojo** (ID: 2e48febd-e584-4ef9-b4eb-1d41e8a0b725)
   - Status: ENV_INCOMPLETE
   - Data Type: NONE

4. **GitLab JavaSpringVulny** (ID: d844f853-2718-46f3-a412-3b767b0bcdda)
   - Status: ACTIVE
   - Data Type: NONE

5. **grafana** (ID: af969b7f-b321-486d-8545-cc170a7ca551)
   - Status: ENV_INCOMPLETE
   - Data Type: NONE

6. **grafana** (ID: 9303b989-2113-4786-ac72-c361db1ae27b)
   - Status: ENV_INCOMPLETE
   - Data Type: NONE
   - Note: Duplicate entry

7. **javaspringvulny** (ID: 6f1efdf4-59a7-4df3-aa63-54c25a97ff2d)
   - Status: ACTIVE
   - Data Type: NONE
   - Note: Different instance than HIGH risk version

8. **JSV-april.conger** (ID: ebdfed0a-efbb-4a1c-a2f0-ad1bb7ae128b)
   - Status: ACTIVE
   - Data Type: NONE

9. **kubernetes** (ID: aa15048e-0f87-4d90-af76-bde9a02c881c)
   - Status: ENV_INCOMPLETE
   - Data Type: NONE

10. **kubernetes** (ID: 7958affc-2a89-42b7-9007-9469011d5b47)
    - Status: ENV_INCOMPLETE
    - Data Type: NONE
    - Note: Duplicate entry

11. **mealie** (ID: 9634f7cd-0bdf-4616-a1da-64a92b157204)
    - Status: ENV_INCOMPLETE
    - Data Type: NONE

12. **platform** (ID: b14b42a5-0ce4-4372-945f-accf077fa5e4)
    - Status: ENV_INCOMPLETE
    - Data Type: NONE

13. **postgrest** (ID: 6c56eb9f-929e-4b5f-89cf-b217a1e57d7b)
    - Status: ACTIVE
    - Data Type: NONE

14. **spring-framework** (ID: fb770130-5949-40be-8f12-b82f5dcf2af3)
    - Status: ENV_INCOMPLETE
    - Data Type: NONE

15. **Test** (ID: 6d7bc80d-348e-4d4d-be21-362782d6644c)
    - Status: ACTIVE
    - Data Type: HIPAA
    - **Note:** Contains HIPAA data - ensure compliance

16. **TEST** (ID: b3239e66-68a3-469b-a3fa-43d7e29173b3)
    - Status: ACTIVE
    - Data Type: NONE

17. **tldr-api** (ID: fef61710-4423-4492-af03-95ab6650b4a3)
    - Status: ACTIVE
    - Data Type: NONE

18. **VamPI** (ID: 081b5301-cf88-4b5f-9df4-b351484fc48c)
    - Status: ACTIVE
    - Data Type: NONE

19. **vets-api** (ID: fa76a564-0ad6-4dd0-aebb-6973b8933273)
    - Status: ACTIVE
    - Data Type: NONE

20. **vets-api** (ID: df459cc0-f9a7-4c10-aeb6-f313ec40d445)
    - Status: ENV_INCOMPLETE
    - Data Type: NONE
    - Note: Duplicate entry

## Sensitive Data Analysis

### Current Status (Last 30 Days)
- **Total Sensitive Data Findings:** 0
- **Overall Risk Score:** 0
- **Critical Findings:** 0

### Data Type Breakdown
No sensitive data exposures detected in the monitored applications over the last 30 days.

## Repository Attack Surface

### Current Repository: mcp-registry
- **Found in StackHawk:** No
- **Has Sensitive Data:** N/A
- **Recommendation:** Repository 'mcp-registry' is not found in your StackHawk attack surface. Consider adding it for security monitoring if it contains application code.

## Key Findings

### Critical Issues
1. **High Risk Application:** The `javaspringvulny` application (ID: 68364212-549b-43cb-9062-1aaaffc7216c) has a HIGH risk level and requires immediate attention.

### Configuration Issues
1. **Incomplete Environments:** 11 applications have ENV_INCOMPLETE status, which may affect scanning coverage:
   - authelia
   - django-DefectDojo
   - grafana (2 instances)
   - kubernetes (2 instances)
   - mealie
   - platform
   - spring-framework
   - vets-api (1 instance)

2. **Duplicate Applications:** Several applications have duplicate entries that should be reviewed:
   - grafana (2 entries)
   - kubernetes (2 entries)
   - javaspringvulny (2 entries)
   - vets-api (2 entries)

### Positive Findings
- No sensitive data exposures in the last 30 days
- Only 1 out of 21 applications is classified as HIGH risk
- Majority of applications are actively monitored and classified as LOW risk

## Recommendations

### Immediate Actions
1. **Address High Risk Application:**
   - Review and remediate vulnerabilities in `javaspringvulny` (ID: 68364212-549b-43cb-9062-1aaaffc7216c)
   - Investigate the specific vulnerabilities causing the HIGH risk classification
   - Implement fixes and retest

2. **Complete Environment Configuration:**
   - Update the 11 applications with ENV_INCOMPLETE status
   - Ensure all applications are properly configured for comprehensive scanning

### Short-Term Actions
1. **Review HIPAA Compliance:**
   - Verify that the "Test" application (ID: 6d7bc80d-348e-4d4d-be21-362782d6644c) with HIPAA data type meets all compliance requirements

2. **Clean Up Duplicate Entries:**
   - Consolidate or remove duplicate application entries
   - Ensure proper naming conventions and unique identifiers

3. **Add Repository Monitoring:**
   - Consider adding the mcp-registry repository to StackHawk for security monitoring if applicable

### Long-Term Actions
1. **Establish Regular Review Cycle:**
   - Schedule monthly security reviews
   - Monitor trends in vulnerability counts and risk levels

2. **Implement Automated Alerting:**
   - Set up alerts for new HIGH risk applications
   - Configure notifications for sensitive data exposures

3. **Security Training:**
   - Provide training to development teams on secure coding practices
   - Share findings and remediation strategies across teams

## Next Steps

1. Access StackHawk dashboard to review detailed vulnerability findings for the HIGH risk application
2. Work with the development team to prioritize and remediate identified vulnerabilities
3. Complete environment configuration for incomplete applications
4. Schedule follow-up review in 30 days to track progress

---

**Report Generated By:** StackHawk MCP Server  
**Contact:** See StackHawk dashboard for detailed vulnerability information
