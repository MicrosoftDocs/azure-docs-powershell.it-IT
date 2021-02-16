---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176662"
---
# <span data-ttu-id="fd53d-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="fd53d-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="fd53d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd53d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd53d-103">Aggiunge un'azione all'oggetto gruppo di azioni ManagementPolicy di input oppure crea un oggetto gruppo di azioni ManagementPolicy con l'azione.</span><span class="sxs-lookup"><span data-stu-id="fd53d-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="fd53d-104">L'oggetto può essere usato in New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="fd53d-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="fd53d-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd53d-105">SYNTAX</span></span>

### <span data-ttu-id="fd53d-106">BaseBlob (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd53d-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd53d-107">Snapshot</span><span class="sxs-lookup"><span data-stu-id="fd53d-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd53d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fd53d-108">DESCRIPTION</span></span>
<span data-ttu-id="fd53d-109">Il cmdlet **Add-AzStorageAccountManagementPolicyAction** aggiunge un'azione all'oggetto gruppo di azioni ManagementPolicy di input oppure crea un oggetto Gruppo azione ManagementPolicy con l'azione.</span><span class="sxs-lookup"><span data-stu-id="fd53d-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="fd53d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd53d-110">EXAMPLES</span></span>

### <span data-ttu-id="fd53d-111">Esempio 1: crea un oggetto Gruppo di azioni ManagementPolicy con 4 azioni, quindi lo aggiunge a una regola dei criteri di gestione e impostato su un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fd53d-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="fd53d-112">Il primo comando crea un oggetto ManagementPolicy Action Group, i tre comandi seguenti aggiungono 3 azioni all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fd53d-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="fd53d-113">Quindi aggiungerla a una regola dei criteri di gestione e impostarla su un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fd53d-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="fd53d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd53d-114">PARAMETERS</span></span>

### <span data-ttu-id="fd53d-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="fd53d-115">-BaseBlobAction</span></span>
<span data-ttu-id="fd53d-116">Azione dei criteri di gestione per baseblob.</span><span class="sxs-lookup"><span data-stu-id="fd53d-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="fd53d-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="fd53d-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="fd53d-118">Valore intero che indica l'età in giorni dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="fd53d-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd53d-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="fd53d-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="fd53d-120">Valore intero che indica l'età in giorni dopo l'ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="fd53d-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="fd53d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd53d-121">-DefaultProfile</span></span>
<span data-ttu-id="fd53d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd53d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd53d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd53d-123">-InputObject</span></span>
<span data-ttu-id="fd53d-124">Se si input l'oggetto Azione ManagementPolicy, imposta l'azione sull'oggetto azione di input.</span><span class="sxs-lookup"><span data-stu-id="fd53d-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="fd53d-125">Se non è stato immesso, verrà creato un nuovo oggetto azione.</span><span class="sxs-lookup"><span data-stu-id="fd53d-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="fd53d-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="fd53d-126">-SnapshotAction</span></span>
<span data-ttu-id="fd53d-127">Azione dei criteri di gestione per lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="fd53d-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd53d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd53d-128">CommonParameters</span></span>
<span data-ttu-id="fd53d-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd53d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd53d-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd53d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd53d-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="fd53d-131">INPUTS</span></span>

### <span data-ttu-id="fd53d-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="fd53d-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="fd53d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd53d-133">OUTPUTS</span></span>

### <span data-ttu-id="fd53d-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="fd53d-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="fd53d-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="fd53d-135">NOTES</span></span>

## <span data-ttu-id="fd53d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd53d-136">RELATED LINKS</span></span>
