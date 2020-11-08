---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188726"
---
# <span data-ttu-id="8bb07-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="8bb07-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="8bb07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bb07-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb07-103">Crea/aggiorna un oggetto ACL dell'elemento datalake Gen2, che può essere usato nel cmdlet Update-AzDataLakeGen2Item.</span><span class="sxs-lookup"><span data-stu-id="8bb07-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="8bb07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bb07-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="8bb07-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bb07-105">DESCRIPTION</span></span>
<span data-ttu-id="8bb07-106">Il cmdlet **set-AzDataLakeGen2ItemAclObject** Crea/aggiorna un oggetto ACL datalake Gen2 Item, che può essere usato nel cmdlet Update-AzDataLakeGen2Item.</span><span class="sxs-lookup"><span data-stu-id="8bb07-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="8bb07-107">Se la nuova voce ACL con lo stesso valore AccessControlType/EntityId/DefaultScope non esiste nell'ACL di input, creerà una nuova voce ACL, else l'autorizzazione di aggiornamento della voce ACL esistente.</span><span class="sxs-lookup"><span data-stu-id="8bb07-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="8bb07-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bb07-108">EXAMPLES</span></span>

### <span data-ttu-id="8bb07-109">Esempio 1: creare un oggetto ACL con 3 voci ACL e aggiornare l'ACL in una directory</span><span class="sxs-lookup"><span data-stu-id="8bb07-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="8bb07-110">Questo comando crea un oggetto ACL con 3 voci ACL (parametro Use-InputObject per aggiungere la voce ACL all'oggetto ACL esistente) e aggiorna ACL in una directory.</span><span class="sxs-lookup"><span data-stu-id="8bb07-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="8bb07-111">Esempio 2: creare un oggetto ACL con 4 voci ACL e l'autorizzazione di aggiornamento di una voce ACL esistente</span><span class="sxs-lookup"><span data-stu-id="8bb07-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="8bb07-112">Questo comando crea prima di tutto un oggetto ACL con 4 voci ACL, quindi Esegui di nuovo il cmdlet con un'autorizzazione diversa, ma lo stesso AccessControlType/EntityId/DefaultScope di una voce ACL esistente.</span><span class="sxs-lookup"><span data-stu-id="8bb07-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="8bb07-113">L'autorizzazione della voce ACL viene quindi aggiornata, ma non viene aggiunta una nuova voce ACL.</span><span class="sxs-lookup"><span data-stu-id="8bb07-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="8bb07-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bb07-114">PARAMETERS</span></span>

### <span data-ttu-id="8bb07-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="8bb07-115">-AccessControlType</span></span>
<span data-ttu-id="8bb07-116">Esistono quattro tipi: "utente" concede diritti al proprietario o a un utente denominato, "Raggruppa" concede i diritti al gruppo proprietario o a un gruppo denominato, "mask" limita i diritti concessi agli utenti denominati e i membri dei gruppi e "altro" concede i diritti a tutti gli utenti non presenti in nessuna delle altre voci.</span><span class="sxs-lookup"><span data-stu-id="8bb07-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="8bb07-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="8bb07-117">-DefaultScope</span></span>
<span data-ttu-id="8bb07-118">Imposta questo parametro per indicare che l'ACE appartiene all'ACL predefinito per una directory. in caso contrario, l'ambito è implicito e l'ACE appartiene all'ACL di Access.</span><span class="sxs-lookup"><span data-stu-id="8bb07-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="8bb07-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="8bb07-119">-EntityId</span></span>
<span data-ttu-id="8bb07-120">Identificatore dell'utente o del gruppo.</span><span class="sxs-lookup"><span data-stu-id="8bb07-120">The user or group identifier.</span></span>
<span data-ttu-id="8bb07-121">Viene omesso per le voci di AccessControlType "mask" e "other".</span><span class="sxs-lookup"><span data-stu-id="8bb07-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="8bb07-122">L'identificatore dell'utente o del gruppo viene omesso anche per il proprietario e il gruppo di appartenenza.</span><span class="sxs-lookup"><span data-stu-id="8bb07-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="8bb07-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bb07-123">-InputObject</span></span>
<span data-ttu-id="8bb07-124">Se input l' \[ \] oggetto PSPathAccessControlEntry, aggiungerà il nuovo ACL come nuovo elemento dell'oggetto PSPathAccessControlEntry di input \[ \] .</span><span class="sxs-lookup"><span data-stu-id="8bb07-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="8bb07-125">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="8bb07-125">-Permission</span></span>
<span data-ttu-id="8bb07-126">Il campo permission è una sequenza di 3 caratteri in cui il primo carattere è "r" per concedere l'accesso in lettura, il secondo carattere è "w" per concedere l'accesso in scrittura e il terzo carattere è "x" per concedere l'autorizzazione di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8bb07-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="8bb07-127">Se l'accesso non viene concesso, il carattere "-" viene usato per indicare che l'autorizzazione è negata.</span><span class="sxs-lookup"><span data-stu-id="8bb07-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="8bb07-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb07-128">CommonParameters</span></span>
<span data-ttu-id="8bb07-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb07-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb07-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb07-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb07-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bb07-131">INPUTS</span></span>

### <span data-ttu-id="8bb07-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8bb07-132">None</span></span>

## <span data-ttu-id="8bb07-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bb07-133">OUTPUTS</span></span>

### <span data-ttu-id="8bb07-134">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="8bb07-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="8bb07-135">Note</span><span class="sxs-lookup"><span data-stu-id="8bb07-135">NOTES</span></span>

## <span data-ttu-id="8bb07-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bb07-136">RELATED LINKS</span></span>
