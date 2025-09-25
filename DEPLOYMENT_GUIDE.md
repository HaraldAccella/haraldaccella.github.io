# GitHub Pages Deployment Guide

## Quick Deployment Steps

### 1. Create GitHub Repository
1. Go to [GitHub.com](https://github.com) and create a new repository
2. Name it something like `arduino-opta-dashboard` or `mqtt-dashboard`
3. Make it public (required for free GitHub Pages)

### 2. Upload Files
1. Copy all files from the `WebDashboard` folder to your repository
2. Upload these files to the root of your repository:
   - `index.html`
   - `devices.json`
   - `README.md`
   - `DEPLOYMENT_GUIDE.md` (this file)

### 3. Enable GitHub Pages
1. Go to your repository on GitHub
2. Click on **Settings** tab
3. Scroll down to **Pages** section
4. Under **Source**, select **Deploy from a branch**
5. Select **main** branch and **/ (root)** folder
6. Click **Save**

### 4. Access Your Dashboard
- Your dashboard will be available at: `https://yourusername.github.io/repositoryname`
- It may take a few minutes to deploy initially

## Configuration Options

### For Local Network Access
1. **Port Forwarding**: Set up port forwarding on your router for port 9001
2. **Dynamic DNS**: Use a service like No-IP or DuckDNS for a permanent hostname
3. **VPN**: Set up a VPN to access your local network

### For Testing with Public Brokers
- Use HiveMQ or Eclipse public brokers for testing
- No authentication required
- Your Arduino device must also connect to the same broker

## Security Considerations

⚠️ **Important Security Notes:**
- Public brokers are not secure for production use
- Consider using authentication and encryption (WSS) for production
- Be careful when exposing your local MQTT broker to the internet
- Use strong passwords and consider IP whitelisting

## Troubleshooting

### Common Issues:
1. **Connection Failed**: Check if your MQTT broker is running and accessible
2. **CORS Errors**: Make sure your broker supports WebSocket connections
3. **Port Issues**: Ensure the correct port is open and forwarded

### Testing Your Setup:
1. Test locally first by opening `index.html` in your browser
2. Use a public broker to verify the dashboard works
3. Then configure your local broker access

## Next Steps

After deployment:
1. Test the dashboard with your Arduino device
2. Configure your local network access method
3. Share the GitHub Pages URL with others who need access
4. Consider setting up monitoring and logging for production use
