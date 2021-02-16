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
# <span data-ttu-id="e3f14-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="e3f14-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="e3f14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3f14-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f14-103">Crea/aggiorna un oggetto ACL dell'elemento Gen2 di DataLake, che può essere usato nel cmdlet Update-AzDataLakeGen2Item dati.</span><span class="sxs-lookup"><span data-stu-id="e3f14-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="e3f14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3f14-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="e3f14-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3f14-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f14-106">Il cmdlet **Set-AzDataLakeGen2ItemAclObject** crea/aggiorna un oggetto ACL dell'elemento DataLake gen2, che può essere usato Update-AzDataLakeGen2Item cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3f14-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="e3f14-107">Se la nuova voce ACL con lo stesso AccessControlType/EntityId/DefaultScope non esiste nell'ACL di input, creerà una nuova voce ACL, altrimenti aggiornare l'autorizzazione della voce ACL esistente.</span><span class="sxs-lookup"><span data-stu-id="e3f14-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="e3f14-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3f14-108">EXAMPLES</span></span>

### <span data-ttu-id="e3f14-109">Esempio 1: Creare un oggetto ACL con 3 voci ACL e aggiornare l'ACL in una directory</span><span class="sxs-lookup"><span data-stu-id="e3f14-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="e3f14-110">Questo comando crea un oggetto ACL con 3 voci ACL (usare il parametro -InputObject per aggiungere una voce acl all'oggetto acl esistente) e aggiorna l'ACL in una directory.</span><span class="sxs-lookup"><span data-stu-id="e3f14-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="e3f14-111">Esempio 2: Creare un oggetto ACL con 4 voci ACL e aggiornare l'autorizzazione di una voce ACL esistente</span><span class="sxs-lookup"><span data-stu-id="e3f14-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="e3f14-112">Questo comando crea prima un oggetto ACL con 4 voci ACL, quindi esegue di nuovo il cmdlet con autorizzazioni diverse ma lo stesso AccessControlType/EntityId/DefaultScope di una voce ACL esistente.</span><span class="sxs-lookup"><span data-stu-id="e3f14-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="e3f14-113">Quindi, l'autorizzazione della voce ACL viene aggiornata, ma non viene aggiunta alcuna nuova voce ACL.</span><span class="sxs-lookup"><span data-stu-id="e3f14-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="e3f14-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3f14-114">PARAMETERS</span></span>

### <span data-ttu-id="e3f14-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="e3f14-115">-AccessControlType</span></span>
<span data-ttu-id="e3f14-116">Esistono quattro tipi: "utente" concede i diritti al proprietario o a un utente denominato, "gruppo" concede i diritti al gruppo proprietario o a un gruppo denominato, "maschera" limita i diritti agli utenti denominati e ai membri dei gruppi, "altro" concede i diritti a tutti gli utenti non presenti in nessuna delle altre voci.</span><span class="sxs-lookup"><span data-stu-id="e3f14-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="e3f14-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="e3f14-117">-DefaultScope</span></span>
<span data-ttu-id="e3f14-118">Impostare questo parametro per indicare che la ACE appartiene all'ACL predefinito per una directory; in caso contrario l'ambito è implicito e la ACE appartiene all'ACL di accesso.</span><span class="sxs-lookup"><span data-stu-id="e3f14-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="e3f14-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="e3f14-119">-EntityId</span></span>
<span data-ttu-id="e3f14-120">L'identificatore dell'utente o del gruppo.</span><span class="sxs-lookup"><span data-stu-id="e3f14-120">The user or group identifier.</span></span>
<span data-ttu-id="e3f14-121">Viene omesso per le voci AccessControlType "mask" e "other".</span><span class="sxs-lookup"><span data-stu-id="e3f14-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="e3f14-122">L'identificatore utente o gruppo viene inoltre omesso per il proprietario e il gruppo proprietario.</span><span class="sxs-lookup"><span data-stu-id="e3f14-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="e3f14-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3f14-123">-InputObject</span></span>
<span data-ttu-id="e3f14-124">Se l'input dell'oggetto PSPathAccessControlEntry, aggiungerà il nuovo ACL come nuovo \[ \] elemento dell'oggetto PSPathAccessControlEntry di \[ \] input.</span><span class="sxs-lookup"><span data-stu-id="e3f14-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="e3f14-125">-Permission</span><span class="sxs-lookup"><span data-stu-id="e3f14-125">-Permission</span></span>
<span data-ttu-id="e3f14-126">Il campo delle autorizzazioni è una sequenza di 3 caratteri in cui il primo carattere è "r" per concedere l'accesso in lettura, il secondo carattere è "w" per concedere l'accesso in scrittura e il terzo carattere è "x" per concedere l'autorizzazione di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e3f14-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="e3f14-127">Se l'accesso non viene concesso, il carattere "-" viene usato per indicare che l'autorizzazione è negata.</span><span class="sxs-lookup"><span data-stu-id="e3f14-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="e3f14-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f14-128">CommonParameters</span></span>
<span data-ttu-id="e3f14-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f14-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f14-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f14-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f14-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3f14-131">INPUTS</span></span>

### <span data-ttu-id="e3f14-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3f14-132">None</span></span>

## <span data-ttu-id="e3f14-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3f14-133">OUTPUTS</span></span>

### <span data-ttu-id="e3f14-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="e3f14-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="e3f14-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3f14-135">NOTES</span></span>

## <span data-ttu-id="e3f14-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3f14-136">RELATED LINKS</span></span>
