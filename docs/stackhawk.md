# StackHawk Security Scanning

This repository uses [StackHawk](https://www.stackhawk.com/) for automated Dynamic Application Security Testing (DAST).

## What is StackHawk?

StackHawk is a dynamic application security testing tool that scans running applications for vulnerabilities. It performs real security tests against your application to identify issues like:

- SQL injection
- Cross-site scripting (XSS)
- Authentication and authorization flaws
- API security issues
- And many other OWASP Top 10 vulnerabilities

## Automated Scanning

StackHawk scans run automatically via GitHub Actions on:
- Every pull request to the main branch
- Pushes to the main branch
- Weekly on Mondays at 2 AM UTC
- Manual trigger via GitHub Actions workflow dispatch

The scan results are uploaded to GitHub Security tab as SARIF reports.

## Configuration

The StackHawk configuration is defined in `stackhawk.yml` at the root of the repository. This configuration:

- Targets the security reviewer proxy service (port 4000)
- Scans health check endpoints and API proxy routes
- Reports findings of MEDIUM severity and above
- Fails the build on HIGH or CRITICAL severity findings

## Running StackHawk Locally

To run StackHawk scans locally:

1. **Install StackHawk CLI**:
   ```bash
   # macOS
   brew install stackhawk/tap/hawkscan
   
   # Or download from https://download.stackhawk.com/hawk/latest/hawkscan-latest.zip
   ```

2. **Set up your API key**:
   ```bash
   export STACKHAWK_API_KEY=your-api-key-here
   ```

3. **Start the proxy service**:
   ```bash
   cd agents/security-reviewer/proxy
   go build -o proxy main.go
   
   export PROXY_LISTEN_ADDR=:4000
   export PROXY_CLIENT_TOKEN=test-token
   export OPENAI_API_KEY=sk-test-key
   export ANTHROPIC_API_KEY=sk-ant-test-key
   
   ./proxy
   ```

4. **Run the scan** (in a new terminal):
   ```bash
   cd /home/runner/work/mcp-registry/mcp-registry
   hawkscan
   ```

## GitHub Secrets Required

To enable StackHawk scanning in CI/CD, the following secret must be configured:

- `STACKHAWK_API_KEY`: Your StackHawk API key from the StackHawk platform

To set this up:
1. Sign up for a StackHawk account at https://app.stackhawk.com
2. Create an application in StackHawk
3. Generate an API key
4. Add the API key as a GitHub repository secret named `STACKHAWK_API_KEY`

## Viewing Results

Scan results can be viewed in multiple places:

1. **GitHub Security Tab**: Navigate to Security → Code scanning alerts
2. **StackHawk Dashboard**: View detailed results at https://app.stackhawk.com
3. **GitHub Actions Logs**: Check the workflow run logs for scan output

## Configuring Scans

To modify the scan configuration, edit `stackhawk.yml`. Common customizations include:

- Adding or removing routes to scan
- Adjusting severity thresholds
- Configuring authentication
- Excluding paths from scanning

For more information, see the [StackHawk documentation](https://docs.stackhawk.com/).
