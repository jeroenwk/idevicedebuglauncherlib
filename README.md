# idevicedebuglauncherlib

idevicedebuglauncherlib is a small helper package that allows an app to request being debugged by idevicedebuglauncher

    if await idevicedebuglauncherlib().findAndConnect() {
        print("i'm being debugged")
    }

The Info.plist must contain:

    <key>NSLocalNetworkUsageDescription</key>
    <string>This app uses the local network to find and use a remote debugger</string>
    <key>NSBonjourServices</key>
    <array>
        <string>_idevicedebuglauncher._tcp</string>
    </array>
