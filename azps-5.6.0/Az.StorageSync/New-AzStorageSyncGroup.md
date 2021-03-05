---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: e96b4360247937ace5a0e2894f3bfac19fc1da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011406"
---
# <span data-ttu-id="17fe9-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="17fe9-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="17fe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="17fe9-103">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="17fe9-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="17fe9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17fe9-104">SYNTAX</span></span>

### <span data-ttu-id="17fe9-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="17fe9-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17fe9-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17fe9-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17fe9-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="17fe9-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17fe9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="17fe9-108">DESCRIPTION</span></span>
<span data-ttu-id="17fe9-109">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="17fe9-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="17fe9-110">Un gruppo di sincronizzazione viene usato per descrivere una topologia di posizioni, definite endpoint, che sincroniranno tutti i file archiviati all'interno di uno degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="17fe9-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="17fe9-111">Un gruppo di sincronizzazione contiene endpoint cloud, che fanno riferimento alle condivisioni file di Azure, e contiene anche endpoint server che fanno riferimento a un percorso locale specifico in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="17fe9-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="17fe9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17fe9-112">EXAMPLES</span></span>

### <span data-ttu-id="17fe9-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17fe9-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="17fe9-114">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="17fe9-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="17fe9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17fe9-115">PARAMETERS</span></span>

### <span data-ttu-id="17fe9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fe9-116">-DefaultProfile</span></span>
<span data-ttu-id="17fe9-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17fe9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17fe9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="17fe9-118">-Name</span></span>
<span data-ttu-id="17fe9-119">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="17fe9-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17fe9-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="17fe9-120">-ParentObject</span></span>
<span data-ttu-id="17fe9-121">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="17fe9-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="17fe9-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="17fe9-122">-ParentResourceId</span></span>
<span data-ttu-id="17fe9-123">ID risorsa padre StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="17fe9-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="17fe9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17fe9-124">-ResourceGroupName</span></span>
<span data-ttu-id="17fe9-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17fe9-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="17fe9-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="17fe9-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="17fe9-127">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="17fe9-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="17fe9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17fe9-128">-Confirm</span></span>
<span data-ttu-id="17fe9-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fe9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17fe9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17fe9-130">-WhatIf</span></span>
<span data-ttu-id="17fe9-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17fe9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17fe9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17fe9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17fe9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fe9-133">CommonParameters</span></span>
<span data-ttu-id="17fe9-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17fe9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fe9-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17fe9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fe9-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="17fe9-136">INPUTS</span></span>

### <span data-ttu-id="17fe9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="17fe9-137">System.String</span></span>

### <span data-ttu-id="17fe9-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="17fe9-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="17fe9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17fe9-139">OUTPUTS</span></span>

### <span data-ttu-id="17fe9-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="17fe9-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="17fe9-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="17fe9-141">NOTES</span></span>

## <span data-ttu-id="17fe9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17fe9-142">RELATED LINKS</span></span>
