# winlogbeat-msi
Below you will find a set of instructions on how to wrap Elastic winlogbeat in an MSI installer package using Visual Studio and WiX. At the bottom of this readme you will find a link to download a pre-built winlogbeat MSI that uses the default configuration as it ships from Elastic. After installation, the winlogbeat service will be started automatically.

## Things you'll need:
1. Visual Studio - https://www.visualstudio.com/vs/community/
2. WiX Toolset - http://wixtoolset.org/releases/
3. WiX Toolset VS extension - https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension
4. Latest winlogbeat version from Elastic - https://www.elastic.co/downloads/beats/winlogbeat
5. The modified install powershell script and license.rtf copy located in this repo.

## Steps to Create the Package Yourself:
1. After downloading and installing all requirements above, create new WiX project in Visual Studio.
2. Add the following references:
   - WixPSExtension
   - WixUIExtension
   - WixUtilExtension
3. Copy and and paste the Product.wxs code into your project.
4. Copy and paste the contents of the winlogbeat folder downloaded from Elastic into your Wix project folder.
5. Replace the default install powershell script with the one from this repo.
6. Place the License.rtf in your wix project folder (this file is used when intalling winlogbeat via the installer GUI).
6. Make adjustments to the winlogbeat.yml to match your envirnoment. 
7. Create new GUIDs (there's is a GUID generator add-on for VS available here https://marketplace.visualstudio.com/items?itemName=kylebahrke.GenerateGUIDforVisualStudio2015)
8. Modify the Product.wxs as you need
9. Build the solution

## Download:
You can download the insaller with default settings (as if you had downloaded it from Elastic) here:

