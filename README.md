# FullStack_Stock_Management_WebSite
DEPLOYMENT CHECKLIST

 Add Spring Boot Actuator dependency
 Configure JVM memory flags in Dockerfile
 Update React build to output to Spring /static
 Create render.yaml blueprint
 Push to GitHub
 Connect Render to repo
 Verify health endpoint: /actuator/health
 Setup UptimeRobot monitor (prevent cold starts)
 Test API: curl https://your-app.onrender.com/api/

 JVM Flags Explained:

-Xms128m -Xmx400m: Heap 128MB-400MB (fit in 512MB RAM)
-XX:+UseSerialGC: Single-threaded GC (low CPU free tier)
-XX:MaxMetaspaceSize=128m: Limit class metadata
-Xss256k: Smaller stack per thread
-XX:TieredStopAtLevel=1: Disable expensive C2 compiler (faster startup)