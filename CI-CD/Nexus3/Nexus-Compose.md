# Nexus-Compose
```yaml
version: "3.5"  
services:  
  nexus:  
    image: sonatype/nexus3:${NEXUS_VERSION:-latest}  
    environment:  
      - NEXUS_PORT=${NEXUS_PORT:-10000}  
    volumes:  
      - "nexus-data:/nexus-data"  
 ports:  
      - "${NEXUS_PORT:-10000}:8081"  
volumes:  
  nexus-data:
```