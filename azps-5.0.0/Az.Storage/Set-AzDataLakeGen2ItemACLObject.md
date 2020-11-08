---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193739"
---
# Set-AzDataLakeGen2ItemAclObject

## Sinossi
Crea/aggiorna un oggetto ACL dell'elemento datalake Gen2, che può essere usato nel cmdlet Update-AzDataLakeGen2Item.

## SINTASSI

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzDataLakeGen2ItemAclObject** Crea/aggiorna un oggetto ACL datalake Gen2 Item, che può essere usato nel cmdlet Update-AzDataLakeGen2Item.
Se la nuova voce ACL con lo stesso valore AccessControlType/EntityId/DefaultScope non esiste nell'ACL di input, creerà una nuova voce ACL, else l'autorizzazione di aggiornamento della voce ACL esistente.

## ESEMPI

### Esempio 1: creare un oggetto ACL con 3 voci ACL e aggiornare l'ACL in una directory
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

Questo comando crea un oggetto ACL con 3 voci ACL (parametro Use-InputObject per aggiungere la voce ACL all'oggetto ACL esistente) e aggiorna ACL in una directory.

### Esempio 2: creare un oggetto ACL con 4 voci ACL e l'autorizzazione di aggiornamento di una voce ACL esistente
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

Questo comando crea prima di tutto un oggetto ACL con 4 voci ACL, quindi Esegui di nuovo il cmdlet con un'autorizzazione diversa, ma lo stesso AccessControlType/EntityId/DefaultScope di una voce ACL esistente.
L'autorizzazione della voce ACL viene quindi aggiornata, ma non viene aggiunta una nuova voce ACL.

## PARAMETRI

### -AccessControlType
Esistono quattro tipi: "utente" concede diritti al proprietario o a un utente denominato, "Raggruppa" concede i diritti al gruppo proprietario o a un gruppo denominato, "mask" limita i diritti concessi agli utenti denominati e i membri dei gruppi e "altro" concede i diritti a tutti gli utenti non presenti in nessuna delle altre voci.

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
Imposta questo parametro per indicare che l'ACE appartiene all'ACL predefinito per una directory. in caso contrario, l'ambito è implicito e l'ACE appartiene all'ACL di Access.

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
Identificatore dell'utente o del gruppo.
Viene omesso per le voci di AccessControlType "mask" e "other".
L'identificatore dell'utente o del gruppo viene omesso anche per il proprietario e il gruppo di appartenenza.

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
Se input l' \[ \] oggetto PSPathAccessControlEntry, aggiungerà il nuovo ACL come nuovo elemento dell'oggetto PSPathAccessControlEntry di input \[ \] .

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

### -Autorizzazione
Il campo permission è una sequenza di 3 caratteri in cui il primo carattere è "r" per concedere l'accesso in lettura, il secondo carattere è "w" per concedere l'accesso in scrittura e il terzo carattere è "x" per concedere l'autorizzazione di esecuzione.
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSPathAccessControlEntry

## Note

## COLLEGAMENTI CORRELATI
