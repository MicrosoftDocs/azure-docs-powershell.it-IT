---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200383"
---
# Remove-AzIoTDeviceProvisioningServiceEnrollment

## SYNOPSIS
Eliminare un record di registrazione del dispositivo.

## SINTASSI

### ResourceSet (impostazione predefinita)
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectSet
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdSet
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Eliminare una registrazione del dispositivo in un servizio di provisioning dei dispositivi Hub IoT di Azure.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

Eliminare un record di registrazione specificato.

### Esempio 2
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

Eliminare tutti i record di registrazione.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DpsName
Nome del servizio di provisioning dei dispositivi IoT

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DpsObject
Oggetto del servizio di provisioning dispositivi IoT

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Consente di restituire l'oggetto booleano.
Per impostazione predefinita, questo cmdlet non genera alcun output.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistrationId
ID registrazione individuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa del servizio di provisioning dispositivi IoT

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription

### System.String

## OUTPUT

### System.Boolean

## NOTE

## COLLEGAMENTI CORRELATI
