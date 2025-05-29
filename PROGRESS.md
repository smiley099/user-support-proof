## AI-Assisted Debugging Examples

### Issue: PostgreSQL Authentication Failure
**Error:** `peer authentication failed for user`
**AI Tool Used:** ChatGPT
**Solution:**
```bash
# Edited pg_hba.conf:
# Changed from 'peer' to 'md5'
sudo nano /etc/postgresql/16/main/pg_hba.conf
sudo systemctl restart postgresql
```

### Issue: Docker Permission Denied
**AI Diagnosis:** "Your user lacks docker group permissions"
**Fix:**
```bash
sudo usermod -aG docker $USER
newgrp docker
```
