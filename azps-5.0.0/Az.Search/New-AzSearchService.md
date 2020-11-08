---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202611"
---
# <span data-ttu-id="d015f-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d015f-101">New-AzSearchService</span></span>

## <span data-ttu-id="d015f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d015f-102">SYNOPSIS</span></span>
<span data-ttu-id="d015f-103">Crea un servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="d015f-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="d015f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d015f-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d015f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d015f-105">DESCRIPTION</span></span>
<span data-ttu-id="d015f-106">Il cmdlet **New-AzSearchService** crea un servizio di ricerca di Azure con parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="d015f-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="d015f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d015f-107">EXAMPLES</span></span>

### <span data-ttu-id="d015f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d015f-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


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

<span data-ttu-id="d015f-109">Il comando crea un servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="d015f-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="d015f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d015f-110">PARAMETERS</span></span>

### <span data-ttu-id="d015f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d015f-111">-DefaultProfile</span></span>
<span data-ttu-id="d015f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d015f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d015f-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="d015f-113">-HostingMode</span></span>
<span data-ttu-id="d015f-114">Modalità di hosting del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d015f-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="d015f-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d015f-115">-Location</span></span>
<span data-ttu-id="d015f-116">Posizione del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d015f-116">Search Service location.</span></span>

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

### <span data-ttu-id="d015f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d015f-117">-Name</span></span>
<span data-ttu-id="d015f-118">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d015f-118">Search Service name.</span></span>

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

### <span data-ttu-id="d015f-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="d015f-119">-PartitionCount</span></span>
<span data-ttu-id="d015f-120">Conteggio delle partizioni del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d015f-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="d015f-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="d015f-121">-ReplicaCount</span></span>
<span data-ttu-id="d015f-122">Conteggio della replica del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d015f-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="d015f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d015f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d015f-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d015f-124">Resource Group name.</span></span>

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

### <span data-ttu-id="d015f-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="d015f-125">-Sku</span></span>
<span data-ttu-id="d015f-126">SKU del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d015f-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="d015f-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d015f-127">-Confirm</span></span>
<span data-ttu-id="d015f-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d015f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d015f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d015f-129">-WhatIf</span></span>
<span data-ttu-id="d015f-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d015f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d015f-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d015f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d015f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d015f-132">CommonParameters</span></span>
<span data-ttu-id="d015f-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d015f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d015f-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d015f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d015f-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d015f-135">INPUTS</span></span>

### <span data-ttu-id="d015f-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d015f-136">None</span></span>

## <span data-ttu-id="d015f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d015f-137">OUTPUTS</span></span>

### <span data-ttu-id="d015f-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d015f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="d015f-139">Note</span><span class="sxs-lookup"><span data-stu-id="d015f-139">NOTES</span></span>

## <span data-ttu-id="d015f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d015f-140">RELATED LINKS</span></span>

[<span data-ttu-id="d015f-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d015f-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="d015f-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d015f-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="d015f-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d015f-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)