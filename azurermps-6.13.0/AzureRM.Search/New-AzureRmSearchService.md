---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
ms.openlocfilehash: 934ba85d438178ee636d5042f1fa145e63d60291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513464"
---
# <span data-ttu-id="e9ad6-101">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="e9ad6-101">New-AzureRmSearchService</span></span>

## <span data-ttu-id="e9ad6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ad6-103">Crea un servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-103">Creates an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9ad6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9ad6-104">SYNTAX</span></span>

```
New-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9ad6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ad6-106">Il cmdlet **New-AzureRmSearchService** crea un servizio di ricerca di Azure con parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-106">The **New-AzureRmSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="e9ad6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9ad6-107">EXAMPLES</span></span>

### <span data-ttu-id="e9ad6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9ad6-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="e9ad6-109">Il comando crea un servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="e9ad6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9ad6-110">PARAMETERS</span></span>

### <span data-ttu-id="e9ad6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ad6-111">-DefaultProfile</span></span>
<span data-ttu-id="e9ad6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ad6-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="e9ad6-113">-HostingMode</span></span>
<span data-ttu-id="e9ad6-114">Modalità di hosting del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-114">Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ad6-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e9ad6-115">-Location</span></span>
<span data-ttu-id="e9ad6-116">Posizione del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-116">Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ad6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9ad6-117">-Name</span></span>
<span data-ttu-id="e9ad6-118">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-118">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ad6-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="e9ad6-119">-PartitionCount</span></span>
<span data-ttu-id="e9ad6-120">Conteggio delle partizioni del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-120">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ad6-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="e9ad6-121">-ReplicaCount</span></span>
<span data-ttu-id="e9ad6-122">Conteggio della replica del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-122">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ad6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9ad6-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9ad6-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ad6-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="e9ad6-125">-Sku</span></span>
<span data-ttu-id="e9ad6-126">SKU del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-126">Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ad6-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e9ad6-127">-Confirm</span></span>
<span data-ttu-id="e9ad6-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9ad6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9ad6-129">-WhatIf</span></span>
<span data-ttu-id="e9ad6-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9ad6-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9ad6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ad6-132">CommonParameters</span></span>
<span data-ttu-id="e9ad6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9ad6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ad6-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9ad6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ad6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9ad6-135">INPUTS</span></span>

### <span data-ttu-id="e9ad6-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e9ad6-136">None</span></span>

## <span data-ttu-id="e9ad6-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9ad6-137">OUTPUTS</span></span>

### <span data-ttu-id="e9ad6-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="e9ad6-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="e9ad6-139">Note</span><span class="sxs-lookup"><span data-stu-id="e9ad6-139">NOTES</span></span>

## <span data-ttu-id="e9ad6-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9ad6-140">RELATED LINKS</span></span>

[<span data-ttu-id="e9ad6-141">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="e9ad6-141">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="e9ad6-142">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="e9ad6-142">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="e9ad6-143">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="e9ad6-143">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
