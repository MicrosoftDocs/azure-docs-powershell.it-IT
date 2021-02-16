---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 209cb5ded738faabfdafc113d3d9524f7c01e927
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209107"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
Crea/aggiorna un oggetto ACL dell'elemento Gen2 di DataLake, che può essere usato nel cmdlet Update-AzDataLakeGen2Item dati.

## SINTASSI

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzDataLakeGen2ItemAclObject** crea/aggiorna un oggetto ACL dell'elemento DataLake gen2, che può essere usato Update-AzDataLakeGen2Item cmdlet.
Se la nuova voce ACL con lo stesso AccessControlType/EntityId/DefaultScope non esiste nell'ACL di input, creerà una nuova voce ACL, altrimenti aggiornare l'autorizzazione della voce ACL esistente.

## ESEMPI

### Esempio 1: Creare un oggetto ACL con 3 voci ACL e aggiornare l'ACL in una directory
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

Questo comando crea un oggetto ACL con 3 voci ACL (usare il parametro -InputObject per aggiungere una voce acl all'oggetto acl esistente) e aggiorna l'ACL in una directory.

### Esempio 2: Creare un oggetto ACL con 4 voci ACL e aggiornare l'autorizzazione di una voce ACL esistente
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

Questo comando crea prima un oggetto ACL con 4 voci ACL, quindi esegue di nuovo il cmdlet con autorizzazioni diverse ma lo stesso AccessControlType/EntityId/DefaultScope di una voce ACL esistente.
Quindi, l'autorizzazione della voce ACL viene aggiornata, ma non viene aggiunta alcuna nuova voce ACL.

## PARAMETERS

### -AccessControlType
Esistono quattro tipi: "utente" concede i diritti al proprietario o a un utente denominato, "gruppo" concede i diritti al gruppo proprietario o a un gruppo denominato, "maschera" limita i diritti agli utenti denominati e ai membri dei gruppi, "altro" concede i diritti a tutti gli utenti non presenti in nessuna delle altre voci.

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
Impostare questo parametro per indicare che la ACE appartiene all'ACL predefinito per una directory; in caso contrario l'ambito è implicito e la ACE appartiene all'ACL di accesso.

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

### -EntityId
L'identificatore dell'utente o del gruppo.
Viene omesso per le voci AccessControlType "mask" e "other".
L'identificatore utente o gruppo viene inoltre omesso per il proprietario e il gruppo proprietario.

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

### -InputObject
Se l'input dell'oggetto PSPathAccessControlEntry, aggiungerà il nuovo ACL come nuovo \[ \] elemento dell'oggetto PSPathAccessControlEntry di \[ \] input.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Permission
Il campo delle autorizzazioni è una sequenza di 3 caratteri in cui il primo carattere è "r" per concedere l'accesso in lettura, il secondo carattere è "w" per concedere l'accesso in scrittura e il terzo carattere è "x" per concedere l'autorizzazione di esecuzione.
Se l'accesso non viene concesso, il carattere "-" viene usato per indicare che l'autorizzazione è negata.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry

## NOTE

## COLLEGAMENTI CORRELATI
