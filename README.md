# Asssignment

Answer 1 
A. External storage never meant removable. It always meant accessible by the user by plugging in a USB cable and mounting it as a drive on a host computer.
B.Internal storage is storage that is not accessible by the user, except via installed apps (or by rooting their device).

Answer 2
Android 8.0 (API level 26) gives better guidance and behaviors around cached data. Each app is now given a disk space quota for cached data, as returned by getCacheQuotaBytes(UUID).
When the system needs to free up disk space, it will start by deleting cached files from apps that are the most over their allocated quota. Thus, if you keep your cached data under your allocated quota, your cached files will be some of the last on the system to be cleared when necessary. When the system is deciding what cached files to delete inside your app, it will consider the oldest files first (as determined by modified time).
There are also two new behaviors that you can enable on a per-directory basis to control how the system frees up your cached data:

Answer 3

Normal permissions:
Many permissions are designated as PROTECTION_NORMAL, which indicates that there's 
no great risk to the user's privacy or security in letting apps have those permissions. 
For example, users would reasonably want to know whether an app can read their contact 
information, so users have to grant this permission explicitly. By contrast, there's no
great risk in allowing an app to vibrate the device, 
so that permission is designated as normal. examples
ACCESS_LOCATION_EXTRA_COMMANDS
ACCESS_NETWORK_STATE
ACCESS_NOTIFICATION_POLICY
ACCESS_WIFI_STATE
BLUETOOTH
BLUETOOTH_ADMIN
BROADCAST_STICKY


Critical permissions
cover areas where the app wants data or resources that involve the user's private information, 
or could potentially affect the user's stored data or the operation of other apps. For example,
the ability to read the user's contacts is a dangerous permission. If an app declares that it 
needs a dangerous permission, the user has to explicitly grant the permission to the app.Examples are
Camera
Contacts
Callender
