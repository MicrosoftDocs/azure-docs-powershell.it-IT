---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: 53ee755daeb0e483b98c9e8449720acce6e38233
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973165"
---
# <span data-ttu-id="360a4-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="360a4-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="360a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="360a4-102">SYNOPSIS</span></span>
<span data-ttu-id="360a4-103">Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un determinato servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="360a4-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="360a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="360a4-104">SYNTAX</span></span>

### <span data-ttu-id="360a4-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="360a4-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="360a4-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="360a4-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="360a4-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="360a4-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="360a4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="360a4-108">DESCRIPTION</span></span>
<span data-ttu-id="360a4-109">Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un determinato servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="360a4-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="360a4-110">Può essere usato per elencare anche gli attributi di ogni gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="360a4-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="360a4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="360a4-111">EXAMPLES</span></span>

### <span data-ttu-id="360a4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="360a4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="360a4-113">Questo comando recupera tutti i gruppi di sincronizzazione contenuti nel servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="360a4-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="360a4-114">Specificare -Name per restituire un nome specifico.</span><span class="sxs-lookup"><span data-stu-id="360a4-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="360a4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="360a4-115">PARAMETERS</span></span>

### <span data-ttu-id="360a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360a4-116">-DefaultProfile</span></span>
<span data-ttu-id="360a4-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="360a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="360a4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="360a4-118">-Name</span></span>
<span data-ttu-id="360a4-119">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="360a4-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="360a4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="360a4-120">-ParentObject</span></span>
<span data-ttu-id="360a4-121">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="360a4-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="360a4-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="360a4-122">-ParentResourceId</span></span>
<span data-ttu-id="360a4-123">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="360a4-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="360a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="360a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="360a4-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="360a4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="360a4-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="360a4-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="360a4-127">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="360a4-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="360a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360a4-128">CommonParameters</span></span>
<span data-ttu-id="360a4-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="360a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360a4-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="360a4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360a4-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="360a4-131">INPUTS</span></span>

### <span data-ttu-id="360a4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="360a4-132">System.String</span></span>

### <span data-ttu-id="360a4-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="360a4-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="360a4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="360a4-134">OUTPUTS</span></span>

### <span data-ttu-id="360a4-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="360a4-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="360a4-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="360a4-136">NOTES</span></span>

## <span data-ttu-id="360a4-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="360a4-137">RELATED LINKS</span></span>
