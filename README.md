# PYAMAHA

[![Join the chat at https://gitter.im/rsc-dev/pyamaha](https://badges.gitter.im/rsc-dev/pyamaha.svg)](https://gitter.im/rsc-dev/pyamaha?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## About
Pyamaha is Python implementation of [Yamaha Extended Control API Specification](https://github.com/rsc-dev/pyamaha/blob/master/doc/YXC_API_Spec_Basic.pdf).
Please see Status for list of implemented functions.
Undocumented functions will be added in future.

## Instalation
```sh
pip install pyamaha
```
or
```sh
python setup.py install
```

## Usage
### API
```python
from pyamaha import Device, System

dev = Device('192.168.1.1')
res = dev.request(System.get_device_info())

print res.json() # JSON response
```

### CLI
```sh
> python -m pyamaha
yxc>device 192.168.1.106
yxc>system
yxc\system>getDeviceInfo
{u'api_version': 1.17,
 u'destination': u'BG',
 u'device_id': u'XXX',
 u'model_name': u'CD-NT670D',
 u'netmodule_checksum': u'XXX',
 u'netmodule_version': u'1130    ',
 u'operation_mode': u'normal',
 u'response_code': 0,
 u'system_id': u'XXX',
 u'system_version': 1.7,
 u'update_error_code': u'FFFFFFFF'}
yxc\system>
```

## Status
<table>
    <th>Function</th>
    <th>API</th>
    <th>CLI</th>
    <th>Info</th>
    <tr>
        <td colspan="4">SYSTEM</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/getDeviceInfo</td>
        <td>x</td>
        <td>x</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/getFeatures</td>
        <td>x</td>
        <td>x</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/getNetworkStatus</td>
        <td>x</td>
        <td>x</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/getFuncStatus</td>
        <td>x</td>
        <td>x</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setAutoPowerStandby</td>
        <td>x</td>
        <td>x</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/getLocationInfo</td>
        <td>x</td>
        <td>x</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/sendIrCode</td>
        <td>x</td>
        <td>x</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setWiredLan</td>
        <td>x</td>
        <td>x</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setWirelessLan</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setWirelessDirect</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>    
    <tr>
        <td>/YamahaExtendedControl/v1/system/setIpSettings</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setNetworkName</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr> 
    <tr>
        <td>/YamahaExtendedControl/v1/system/setAirPlayPin</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/getMacAddressFilter</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>  
    <tr>
        <td>/YamahaExtendedControl/v1/system/setMacAddressFilter</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>     
    <tr>
        <td>/YamahaExtendedControl/v1/system/getNetworkStandby</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>   
    <tr>
        <td>/YamahaExtendedControl/v1/system/setNetworkStandby</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/getBluetoothInfo</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>       
    <tr>
        <td>/YamahaExtendedControl/v1/system/setBluetoothStandby</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr> 
    <tr>
        <td>/YamahaExtendedControl/v1/system/setBluetoothTxSetting</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>     
    <tr>
        <td>/YamahaExtendedControl/v1/system/getBluetoothDeviceList</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/updateBluetoothDeviceList</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>    
    <tr>
        <td>/YamahaExtendedControl/v1/system/connectBluetoothDevice</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/disconnectBluetoothDevice</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setSpeakerA</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setSpeakerB</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setDimmer</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setZoneBVolumeSync</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/system/setHdmiOut1</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr> 
    <tr>
        <td>/YamahaExtendedControl/v1/system/setHdmiOut2</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>    
    <tr>
        <td>/YamahaExtendedControl/v1/system/getNameText</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
        <tr>
        <td>/YamahaExtendedControl/v1/system/setNameText</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td colspan="4">ZONE</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/getStatus</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/getSoundProgramList</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setPower</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setSleep</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setVolume</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setMute</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setInput</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setSoundProgram</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/prepareInputChange</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/set3dSurround</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setDirect</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setPureDirect</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setEnhancer</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setToneControl</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setEqualizer</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setBalance</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setDialogueLevel</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setDialogueLift</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setClearVoice</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>  
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setSubwooferVolume</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>    
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/setBassExtension</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>      
    <tr>
        <td>/YamahaExtendedControl/v1/{zone}/getSignalInfo</td>
        <td>x</td>
        <td>-</td>
        <td>Documented</td>
    </tr>    
<tr><td colspan="4">TUNER</td></tr>
<tr>
<td>/YamahaExtendedControl/v1/tuner/getPresetInfo</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/tuner/getPlayInfo</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/tuner/setFreq</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/tuner/recallPreset</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/tuner/switchPreset</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/tuner/storePreset</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/tuner/setDabService</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr><td colspan="4">NETWORK/USB</td></tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/getPresetInfo</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/getPlayInfo</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/setPlayback</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/toggleRepeat</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/toggleShuffle</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/getListInfo</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/setListControl</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/setSearchString</td>
<td>-</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/recallPreset</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/storePreset</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/getAccountStatus</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/switchAccount</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/netusb/getServiceInfo</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr><td colspan="4">CD</td></tr>
<tr>
<td>/YamahaExtendedControl/v1/cd/getPlayInfo</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/cd/setPlayback</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/cd/toggleTray</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/cd/toggleRepeat</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
<td>/YamahaExtendedControl/v1/cd/toggleShuffle</td>
<td>x</td>
<td>-</td>
<td>Documented</td>
</tr>
<tr>
        <td colspan="4">DIST</td>
</tr>
<tr>
    <td>/YamahaExtendedControl/v1/dist/getDistributionInfo</td>
    <td>x</td>
    <td>-</td>
    <td>Documented</td>
</tr>
<tr>
    <td>/YamahaExtendedControl/v1/dist/setServerInfo</td>
    <td>x</td>
    <td>-</td>
    <td>Documented</td>
</tr>
<tr>
    <td>/YamahaExtendedControl/v1/dist/setClientInfo</td>
    <td>x</td>
    <td>-</td>
    <td>Documented</td>
</tr>
<tr>
    <td>/YamahaExtendedControl/v1/dist/startDistribution</td>
    <td>x</td>
    <td>-</td>
    <td>Documented</td>
</tr>
<tr>
    <td>/YamahaExtendedControl/v1/dist/stopDistribution</td>
    <td>x</td>
    <td>-</td>
    <td>Documented</td>
</tr>
<tr>
    <td>/YamahaExtendedControl/v1/dist/setGroupName</td>
    <td>x</td>
    <td>-</td>
    <td>Documented</td>
</tr>
</table>

## License
Code is released under [MIT license](https://github.com/rsc-dev/pyamaha/blob/master/LICENSE) © [Radoslaw '[rsc]' Matusiak](https://rm2084.blogspot.com/).