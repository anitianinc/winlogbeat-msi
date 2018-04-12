# winlogbeat-msi
Elastic Winlogbeat MSI

## Things you'll need:

1. Visual Basic - https://www.visualstudio.com/vs/community/
2. WiX Toolset - http://wixtoolset.org/releases/
3. WiX Toolset VB extension - https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension
4. Latest winlogbeat version from Elastic - https://www.elastic.co/downloads/beats/winlogbeat
5. The modified install powershell script and license.rtf copy located in this repo.

## Steps to Create the Package Yourself:

1. After downloading and installing all requirements above, create new WiX project in VB.
2. Add the following references:
  - WixPSExtension
  - WixUIExtension
  - WixUtilExtension
3. Copy and and paste the Product.wxs code into your project.
4. Copy and paste the contents of the winlogbeat folder downloaded from Elastic into your Wix project folder.
5. Replace the default install powershell script with the one from this repo.
6. Place the License.rtf in your wix project folder (this file is used when intalling winlogbeat via the installer GUI).
6. Make adjustments to the winlogbeat.yml to match your envirnoment. 
7. Create new GUIDs (there's is a GUID generator add-on for VB available here)
8. Modify the Product.wxs as you need.
9. Build the solution.
