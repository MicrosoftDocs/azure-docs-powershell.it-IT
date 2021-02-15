---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183118"
---
# <span data-ttu-id="7d4cc-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7d4cc-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="7d4cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4cc-103">Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un determinato servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="7d4cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d4cc-104">SYNTAX</span></span>

### <span data-ttu-id="7d4cc-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="7d4cc-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d4cc-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d4cc-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d4cc-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d4cc-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d4cc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d4cc-108">DESCRIPTION</span></span>
<span data-ttu-id="7d4cc-109">Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un determinato servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="7d4cc-110">Può essere usato anche per elencare gli attributi di ogni gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="7d4cc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d4cc-111">EXAMPLES</span></span>

### <span data-ttu-id="7d4cc-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d4cc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="7d4cc-113">Questo comando recupera tutti i gruppi di sincronizzazione contenuti nel servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="7d4cc-114">Specificare -Name per restituire un nome specifico.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="7d4cc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d4cc-115">PARAMETERS</span></span>

### <span data-ttu-id="7d4cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4cc-116">-DefaultProfile</span></span>
<span data-ttu-id="7d4cc-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d4cc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7d4cc-118">-Name</span></span>
<span data-ttu-id="7d4cc-119">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d4cc-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7d4cc-120">-ParentObject</span></span>
<span data-ttu-id="7d4cc-121">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d4cc-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7d4cc-122">-ParentResourceId</span></span>
<span data-ttu-id="7d4cc-123">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d4cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d4cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d4cc-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d4cc-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="7d4cc-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="7d4cc-127">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d4cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4cc-128">CommonParameters</span></span>
<span data-ttu-id="7d4cc-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d4cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4cc-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d4cc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4cc-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d4cc-131">INPUTS</span></span>

### <span data-ttu-id="7d4cc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7d4cc-132">System.String</span></span>

### <span data-ttu-id="7d4cc-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="7d4cc-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="7d4cc-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d4cc-134">OUTPUTS</span></span>

### <span data-ttu-id="7d4cc-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7d4cc-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="7d4cc-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d4cc-136">NOTES</span></span>

## <span data-ttu-id="7d4cc-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d4cc-137">RELATED LINKS</span></span>
