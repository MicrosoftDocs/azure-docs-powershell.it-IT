---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021084"
---
# <span data-ttu-id="027c5-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="027c5-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="027c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="027c5-102">SYNOPSIS</span></span>
<span data-ttu-id="027c5-103">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="027c5-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="027c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="027c5-104">SYNTAX</span></span>

### <span data-ttu-id="027c5-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="027c5-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="027c5-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="027c5-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="027c5-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="027c5-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="027c5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="027c5-108">DESCRIPTION</span></span>
<span data-ttu-id="027c5-109">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="027c5-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="027c5-110">Viene usato un gruppo di sincronizzazione per descrivere una topologia di percorsi, denominati endpoint, che sincronizzano tutti i file archiviati in uno degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="027c5-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="027c5-111">Un gruppo di sincronizzazione contiene endpoint di tipo cloud, che fanno riferimento a condivisioni di file Azure e contiene anche endpoint server che fanno riferimento a un percorso locale specifico in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="027c5-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="027c5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="027c5-112">EXAMPLES</span></span>

### <span data-ttu-id="027c5-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="027c5-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="027c5-114">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="027c5-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="027c5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="027c5-115">PARAMETERS</span></span>

### <span data-ttu-id="027c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027c5-116">-DefaultProfile</span></span>
<span data-ttu-id="027c5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="027c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="027c5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="027c5-118">-Name</span></span>
<span data-ttu-id="027c5-119">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="027c5-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="027c5-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="027c5-120">-ParentObject</span></span>
<span data-ttu-id="027c5-121">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="027c5-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="027c5-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="027c5-122">-ParentResourceId</span></span>
<span data-ttu-id="027c5-123">ID risorsa padre di StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="027c5-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="027c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="027c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="027c5-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="027c5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="027c5-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="027c5-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="027c5-127">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="027c5-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="027c5-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="027c5-128">-Confirm</span></span>
<span data-ttu-id="027c5-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="027c5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="027c5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="027c5-130">-WhatIf</span></span>
<span data-ttu-id="027c5-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="027c5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="027c5-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="027c5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="027c5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027c5-133">CommonParameters</span></span>
<span data-ttu-id="027c5-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="027c5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027c5-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="027c5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027c5-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="027c5-136">INPUTS</span></span>

### <span data-ttu-id="027c5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="027c5-137">System.String</span></span>

### <span data-ttu-id="027c5-138">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="027c5-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="027c5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="027c5-139">OUTPUTS</span></span>

### <span data-ttu-id="027c5-140">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="027c5-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="027c5-141">Note</span><span class="sxs-lookup"><span data-stu-id="027c5-141">NOTES</span></span>

## <span data-ttu-id="027c5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="027c5-142">RELATED LINKS</span></span>
