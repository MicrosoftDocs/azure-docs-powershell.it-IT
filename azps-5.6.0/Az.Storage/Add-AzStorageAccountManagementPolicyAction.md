---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 65bce04c3df14a6b9dc4397d47577d0642746c45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976189"
---
# <span data-ttu-id="aa2fa-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="aa2fa-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="aa2fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2fa-103">Aggiunge un'azione all'oggetto gruppo di azioni ManagementPolicy di input oppure crea un oggetto gruppo di azioni ManagementPolicy con l'azione.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="aa2fa-104">L'oggetto può essere usato in New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="aa2fa-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa2fa-105">SYNTAX</span></span>

### <span data-ttu-id="aa2fa-106">BaseBlob (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa2fa-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa2fa-107">Snapshot</span><span class="sxs-lookup"><span data-stu-id="aa2fa-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa2fa-108">BLOBVersion</span><span class="sxs-lookup"><span data-stu-id="aa2fa-108">BlobVersion</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BlobVersionAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa2fa-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aa2fa-109">DESCRIPTION</span></span>
<span data-ttu-id="aa2fa-110">Il cmdlet **Add-AzStorageAccountManagementPolicyAction** aggiunge un'azione all'oggetto gruppo di azioni ManagementPolicy di input oppure crea un oggetto Gruppo di azioni ManagementPolicy con l'azione.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-110">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="aa2fa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa2fa-111">EXAMPLES</span></span>

### <span data-ttu-id="aa2fa-112">Esempio 1: crea un oggetto Gruppo di azioni ManagementPolicy con 4 azioni, quindi lo aggiunge a una regola dei criteri di gestione e impostato su un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="aa2fa-112">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100
Version.TierToCool.DaysAfterCreationGreaterThan         : 
Version.TierToArchive.DaysAfterCreationGreaterThan      : 
Version.Delete.DaysAfterCreationGreaterThan             : 

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="aa2fa-113">Il primo comando crea un oggetto ManagementPolicy Action Group, i tre comandi seguenti aggiungono 3 azioni all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-113">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="aa2fa-114">Quindi aggiungerla a una regola dei criteri di gestione e impostarla su un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-114">Then add it to a management policy rule and set to a Storage account.</span></span>

### <span data-ttu-id="aa2fa-115">Esempio 2: crea un oggetto Gruppo di azioni ManagementPolicy con 6 azioni su snapshot e versione BLOB, quindi lo aggiunge a una regola dei criteri di gestione e impostato su un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="aa2fa-115">Example 2: Creates a ManagementPolicy Action Group object with 6 actions on snapshot and blob version, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction  -SnapshotAction Delete -daysAfterCreationGreaterThan 40
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToArchive -daysAfterCreationGreaterThan 50
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToCool -daysAfterCreationGreaterThan 60
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction Delete -daysAfterCreationGreaterThan 70
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToArchive -daysAfterCreationGreaterThan 80
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToCool -daysAfterCreationGreaterThan 90
PS C:\> $action

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 60
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 50
Snapshot.Delete.DaysAfterCreationGreaterThan            : 40
Version.TierToCool.DaysAfterCreationGreaterThan         : 90
Version.TierToArchive.DaysAfterCreationGreaterThan      : 80
Version.Delete.DaysAfterCreationGreaterThan             : 70

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="aa2fa-116">Il primo comando crea un oggetto ManagementPolicy Action Group, i 5 comandi seguenti aggiungono 5 azioni sull'oggetto snapshot e sulla versione BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-116">The first command create a ManagementPolicy Action Group object, the following 5 commands add 5 actions on snapshot and blob version to the object.</span></span> <span data-ttu-id="aa2fa-117">Quindi aggiungerla a una regola dei criteri di gestione e impostarla su un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-117">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="aa2fa-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa2fa-118">PARAMETERS</span></span>

### <span data-ttu-id="aa2fa-119">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="aa2fa-119">-BaseBlobAction</span></span>
<span data-ttu-id="aa2fa-120">Azione dei criteri di gestione per baseblob.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-120">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2fa-121">-BlobVersionAction</span><span class="sxs-lookup"><span data-stu-id="aa2fa-121">-BlobVersionAction</span></span>
<span data-ttu-id="aa2fa-122">Azione dei criteri di gestione per la versione BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-122">The management policy action for blob version.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobVersion
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2fa-123">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="aa2fa-123">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="aa2fa-124">Valore intero che indica l'età in giorni dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-124">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot, BlobVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2fa-125">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="aa2fa-125">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="aa2fa-126">Valore intero che indica l'età in giorni dopo l'ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-126">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2fa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2fa-127">-DefaultProfile</span></span>
<span data-ttu-id="aa2fa-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa2fa-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa2fa-129">-InputObject</span></span>
<span data-ttu-id="aa2fa-130">Se si input l'oggetto Azione ManagementPolicy, imposta l'azione sull'oggetto azione di input.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-130">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="aa2fa-131">Se non è stato immesso, verrà creato un nuovo oggetto azione.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-131">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa2fa-132">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="aa2fa-132">-SnapshotAction</span></span>
<span data-ttu-id="aa2fa-133">Azione dei criteri di gestione per lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-133">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2fa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2fa-134">CommonParameters</span></span>
<span data-ttu-id="aa2fa-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa2fa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2fa-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa2fa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2fa-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="aa2fa-137">INPUTS</span></span>

### <span data-ttu-id="aa2fa-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="aa2fa-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="aa2fa-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa2fa-139">OUTPUTS</span></span>

### <span data-ttu-id="aa2fa-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="aa2fa-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="aa2fa-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="aa2fa-141">NOTES</span></span>

## <span data-ttu-id="aa2fa-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa2fa-142">RELATED LINKS</span></span>
