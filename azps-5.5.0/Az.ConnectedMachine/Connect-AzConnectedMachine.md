---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209930"
---
# Connect-AzConnectedMachine

## SYNOPSIS
API per registrare un nuovo computer e quindi creare una risorsa tracciata in ARM

## SINTASSI

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## DESCRIZIONE
API per registrare un nuovo computer e quindi creare una risorsa tracciata in ARM

## ESEMPI

### Esempio 1: eseguire l'onboards del computer in uso come computer connesso
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

Onboards il computer su cui ti stai collegando come computer connesso.

### Esempio 2: consente di aggiungere un computer remoto come dispositivo connesso
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

Consente di eseguire l'onboardmento di un computer remoto come dispositivo connesso con PowerShell.
Nota: al momento è supportato solo Windows come destinazione.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Posizione della macchina connessa creata.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome che verrà usato per il computer.
Il nome host viene usato per impostazione predefinita.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Proxy
URI da usare per il server proxy

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PSSession
Se specificato, il comando che esegue l'onboardamento dei computer in Azure verrà eseguito all'interno di ogni PSSession.
NOTA: per il momento questa operazione funziona solo in Windows.

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse a cui si vuole aggiungere il computer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID dell'abbonamento a cui si vuole aggiungere il computer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Tag di risorse.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

## OUTPUT

## NOTE

ALIAS

## COLLEGAMENTI CORRELATI

