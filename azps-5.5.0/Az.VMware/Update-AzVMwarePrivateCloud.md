---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: dbea608c24d8da8fa292316653b3e16953aed8b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208891"
---
# Update-AzVMwarePrivateCloud

## SYNOPSIS
Aggiornare un cloud privato

## SINTASSI

### UpdateExpanded (impostazione predefinita)
```
Update-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIZIONE
Aggiornare un cloud privato

## ESEMPI

### Esempio 1: Aggiornare le dimensioni del cloud privato in base al nome
```powershell
PS C:\> Update-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

Aggiornare le dimensioni del cloud privato in base al nome

### Esempio 2: Aggiornare le dimensioni del cloud privato in base all'oggetto di input
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMwarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

Aggiornare le dimensioni del cloud privato in base all'oggetto di input

## PARAMETERS

### -AsJob
Eseguire il comando come processo

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

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentitySource
vCenter Single Sign On Identity Sources To construct, vedere la sezione NOTES per le proprietà IDENTITYSOURCE e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Internet
La connettività a Internet è abilitata o disabilitata

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementClusterSize
Le dimensioni del cluster

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome del cloud privato

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Eseguire il comando in modo asincrono

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

### -ResourceGroupName
Nome del gruppo di risorse.
Per il nome non viene distinzione tra maiuscole e minuscole.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID della sottoscrizione di destinazione.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: False
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


IDENTITYSOURCE <IIdentitySource[]>: origini identità Single #A0 vCenter
  - `[Alias <String>]`: nome Net PIÙ.SEE del dominio
  - `[BaseGroupDn <String>]`: nome distinto di base per i gruppi
  - `[BaseUserDn <String>]`: nome distinto di base per gli utenti
  - `[Domain <String>]`: nome dns del dominio
  - `[Name <String>]`: nome dell'origine dell'identità
  - `[Password <String>]`: la password dell'utente di Active Directory con almeno l'accesso in sola lettura al DN di base per utenti e gruppi.
  - `[PrimaryServer <String>]`: URL server principale
  - `[SecondaryServer <String>]`: URL server secondario
  - `[Ssl <SslEnum?>]`: per proteggere le comunicazioni LDAP con un certificato SSL (LDAPS)
  - `[Username <String>]`: ID di un utente di Active Directory con almeno l'accesso in sola lettura al DN di base per utenti e gruppi

INPUTOBJECT <IVMwareIdentity> : parametro identity
  - `[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato
  - `[ClusterName <String>]`: nome del cluster nel cloud privato
  - `[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato
  - `[Id <String>]`: percorso di identità della risorsa
  - `[Location <String>]`: Area geografica Azure
  - `[PrivateCloudName <String>]`: nome del cloud privato
  - `[ResourceGroupName <String>]`: nome del gruppo di risorse. Per il nome non viene distinzione tra maiuscole e minuscole.
  - `[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.

## COLLEGAMENTI CORRELATI

