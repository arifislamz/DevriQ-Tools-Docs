# Troubleshooting Guide

**Solve common issues with DevriQ Tools** — Comprehensive troubleshooting guide for all platform features.

---

## 📋 Quick Reference

- [Tool Loading Issues](#-tool-loading-issues)
- [File Upload Problems](#-file-upload-problems)
- [Processing Issues](#-processing-issues)
- [Download Problems](#-download-problems)
- [Browser Compatibility](#-browser-compatibility)
- [Performance Issues](#-performance-issues)
- [Contact Support](#-contact-support)

---

## 🔧 Tool Loading Issues

### Issue: Tool page won't load

**Symptoms:** Blank page, loading spinner stuck, 404 error

**Solutions:**
1. **Refresh page** → F5 or Ctrl+R
2. **Clear browser cache** → Ctrl+Shift+Delete
3. **Try different browser** → Chrome, Firefox, Safari, Edge
4. **Disable extensions** → Extensions may interfere
5. **Check internet** → Try loading other websites

**If still not working:**
- [Contact support →](https://devriq.in/contact-us)

---

## 📁 File Upload Problems

### Issue: File upload returns error

**Common Causes:**
1. **Unsupported format** → Check tool's supported formats
2. **File too large** → Tool has size limits
3. **Connection interrupted** → Internet dropped
4. **Browser security** → Security settings blocking
5. **Temporary issue** → Server-side problem

**Solutions:**
1. **Check format:**
   - PDF tools need .pdf files
   - Image tools need image formats
   - See tool description for list

2. **Reduce file size:**
   - Compress first if possible
   - Split into smaller chunks
   - Try simplified version

3. **Verify connection:**
   - Test other uploads
   - Check internet speed
   - Try at different time

4. **Change browser:**
   - Try Chrome/Firefox/Safari
   - Disable browser extensions
   - Try incognito/private mode

### Issue: Drag-and-drop not working

**Solutions:**
1. Use file browser button instead
2. Try different browser
3. Disable browser extensions
4. Try different PDF/file

### Issue: Upload seems to work but tool shows error

**Solutions:**
1. Wait longer (large files take time)
2. Try smaller file first
3. Refresh and retry
4. Clear browser cache

---

## ⚙️ Processing Issues

### Issue: Tool processing is very slow

**Symptoms:** Spinner running for long time, no results

**Causes:**
- Large file size
- Slow internet connection
- Browser memory pressure
- Server load

**Solutions:**
1. **Reduce file size** → Use smaller file
2. **Close tabs** → Reduce browser load
3. **Restart browser** → Clear memory
4. **Wait longer** → Large files take time
5. **Try later** → Peak usage times slower

### Issue: Tool crashes during processing

**Symptoms:** Browser freeze, tab closes, error message

**Solutions:**
1. **Try smaller file** → Reduce input size
2. **Use simpler input** → Complex files may crash
3. **Try different browser** → Chrome vs Firefox
4. **Clear cache** → Browser storage issue
5. **Restart browser** → Memory leak

### Issue: Tool shows wrong output

**Symptoms:** Tool completes but output incorrect

**Verification:**
1. **Check input** → Verify input data correct
2. **Review settings** → Did you configure correctly?
3. **Read help** → Tool description may explain
4. **Try sample** → Test with known data
5. **Test again** → May be one-time issue

---

## 💾 Download Problems

### Issue: Download doesn't start

**Symptoms:** Click download but nothing happens

**Solutions:**
1. **Check browser settings** → Downloads may be blocked
2. **Allow popups** → Download may be popup
3. **Try different browser** → Chrome vs Firefox
4. **Check file size** → Very large files may timeout
5. **Try again** → Temporary glitch

### Issue: Downloaded file is corrupted

**Symptoms:** Can't open downloaded file, file appears broken

**Solutions:**
1. **Download again** → First attempt may have failed
2. **Try different browser** → Browser-specific issue
3. **Try different format** → If format option available
4. **Check tool settings** → Wrong format selected?
5. **Try smaller file** → Test file may be corrupt

### Issue: File won't open in native application

**Symptoms:** "File appears to be corrupted" or won't open

**Solutions:**
1. **Use correct application** → Right tool for format
2. **Verify format** → File extension correct?
3. **Try online viewer** → Web-based viewers often work
4. **Check file size** → Should match preview size
5. **Verify complete download** → Did download finish?

---

## 🌐 Browser Compatibility

### Issue: Tool works in one browser but not another

**Solution:** Compatibility varies by browser

**Recommended Browsers:**
- ✅ Chrome (latest) — Best compatibility
- ✅ Firefox (latest) — Excellent support
- ✅ Safari (latest) — Good Mac support
- ✅ Edge (latest) — Windows support
- ⚠️ IE (not supported) — Use modern browser

**Browser Solution:**
1. Update to latest version
2. Try Chrome if unsupported
3. Disable extensions
4. Try incognito/private mode

### Issue: Tool looks weird/broken on mobile

**Solutions:**
1. **Rotate device** → Try landscape mode
2. **Zoom out** → Click controls may be off-screen
3. **Use desktop browser** → Mobile view may be limited
4. **Wait for mobile app** → Coming soon

---

## ⚡ Performance Issues

### General Slowness

**Diagnosis:**
1. **Close browser tabs** → Reduces memory usage
2. **Clear cache** → Removes temporary files
3. **Restart browser** → Clears memory
4. **Check internet** → Test speed.test.net
5. **Restart computer** → Frees system resources

### Tool-Specific Slowness

**Large files:**
- Reduce file size first
- Compress before processing
- Process in smaller batches
- Try at slower times

**Complex operations:**
- PDF merging many files → Merge fewer at once
- Image processing → Use smaller images
- Encoding large data → Encode sections

---

## 🔒 Privacy & Security Issues

### Issue: Concerned about privacy

**Verification:**
1. **Check Privacy Policy** → [Privacy →](../PRIVACY_FIRST.md)
2. **Review network traffic** → Browser dev tools
3. **Watch for uploads** → Files shouldn't upload
4. **Check encryption** → Should see HTTPS 🔒
5. **Read architecture** → [Architecture →](../ARCHITECTURE.md)

**What to look for:**
✅ HTTPS lock icon (🔒)  
✅ No uploads in network tab  
✅ Local browser processing  
✅ Instant operation (no server wait)  

---

## 🆘 When to Contact Support

**Contact support if:**
- Issue persists after troubleshooting
- Error message shows
- Tool specific problem
- Feature request
- Security concern

**How to contact:**
- 📧 Email: [support@devriq.in](mailto:support@devriq.in)
- 🌐 Form: [devriq.in/contact](https://devriq.in/contact-us)
- 💬 Request feature: [Feature request →](https://tools.devriq.in/request-tool/)

**Provide:**
- Tool name
- Browser/OS
- Exact steps to reproduce
- Error messages (screenshot)
- File type/size (if applicable)

---

## 📝 Common Solutions Quick Reference

| Issue | First Try | Second Try | Contact Support |
|-------|-----------|-----------|-----------------|
| Won't load | Refresh | Clear cache | Email support |
| Upload fails | Different format | Smaller file | Email support |
| Slow processing | Close tabs | Restart browser | Email support |
| Output wrong | Check input | Try sample file | Email support |
| Download fails | Download again | Different browser | Email support |
| Concerned privacy | Read docs | Check network | Support email |

---

## 🎓 Getting Help

### Documentation
- [Getting Started](../GETTING_STARTED.md)
- [Best Practices](./best-practices.md)
- [Privacy Guide](../PRIVACY_FIRST.md)
- [FAQ](../FAQ.md)

### Support
- Email: [support@devriq.in](mailto:support@devriq.in)
- Contact: [devriq.in/contact](https://devriq.in/contact-us)
- Features: [Request tool →](https://tools.devriq.in/request-tool/)

---

**Last Updated**: April 2, 2026  
**Status**: Current ✅

---

**Still stuck?** [Email support →](mailto:support@devriq.in)  
**Have a solution?** [Share →](https://devriq.in/contact-us)

---

© 2026 DevriQ Tools. All rights reserved.
