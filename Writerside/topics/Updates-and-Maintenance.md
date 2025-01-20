# Updates and Maintenance

## Updates and Distribution Upgrades

We aim to have `seps-app01` as frequently updated as possible. See the table below for ideal timeframes:

| Trigger                               | Timeframe to update                            |
|---------------------------------------|------------------------------------------------|
| Weekly Updating Schedule              | On every Friday morning, in line with Lab PCs. |
| Discovery of Zero-Day Vulnerabilities | As soon as a hotfix is released.               |

### Updates via `apt`

Most of our software is maintained via `apt`. to update system packages, run `sudo apt update && sudo apt upgrade -y`.

### Docker Image Updates

Check with the Image maintainer for any released updates, however we typically only target Zero-Day fixes.

### Distribution Upgrades

We run `seps-app01` on the LTS Ubuntu Release Branch, which means we will be updating the distribution once it is available.

To upgrade the distribution, leave it a few days after it has been released. Most bugs will have been caught by the community
and most likely already fixed. After that period has elapsed, you will need to *physically* log in to the Server. Once
you are at the terminal prompt, run `sudo do-release-upgrade` and follow the on-screen instructions. Once the upgrade has completed
reboot the server using `sudo reboot now`.