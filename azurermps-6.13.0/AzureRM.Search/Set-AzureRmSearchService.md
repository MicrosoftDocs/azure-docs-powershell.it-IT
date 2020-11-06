---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/set-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
ms.openlocfilehash: c938dd611d9f6d731c07d5aee76cb390838f4679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513459"
---
# <span data-ttu-id="9ecc1-101">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="9ecc1-101">Set-AzureRmSearchService</span></span>

## <span data-ttu-id="9ecc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ecc1-102">SYNOPSIS</span></span>
<span data-ttu-id="9ecc1-103">Aggiornare un servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-103">Update an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ecc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ecc1-104">SYNTAX</span></span>

### <span data-ttu-id="9ecc1-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ecc1-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ecc1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ecc1-106">InputObjectParameterSet</span></span>
```
Set-AzureRmSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ecc1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ecc1-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ecc1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ecc1-108">DESCRIPTION</span></span>
<span data-ttu-id="9ecc1-109">Il cmdlet **set-AzureRmSearchService** modifica un servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-109">The **Set-AzureRmSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="9ecc1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ecc1-110">EXAMPLES</span></span>

### <span data-ttu-id="9ecc1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9ecc1-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="9ecc1-112">L'esempio cambia il conteggio delle partizioni e il conteggio delle repliche del servizio di ricerca di Azure su 2.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="9ecc1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ecc1-113">PARAMETERS</span></span>

### <span data-ttu-id="9ecc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ecc1-114">-DefaultProfile</span></span>
<span data-ttu-id="9ecc1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ecc1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ecc1-116">-InputObject</span></span>
<span data-ttu-id="9ecc1-117">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ecc1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ecc1-118">-Name</span></span>
<span data-ttu-id="9ecc1-119">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-119">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ecc1-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="9ecc1-120">-PartitionCount</span></span>
<span data-ttu-id="9ecc1-121">Conteggio delle partizioni del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="9ecc1-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="9ecc1-122">-ReplicaCount</span></span>
<span data-ttu-id="9ecc1-123">Conteggio della replica del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="9ecc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ecc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ecc1-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ecc1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ecc1-126">-ResourceId</span></span>
<span data-ttu-id="9ecc1-127">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-127">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ecc1-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9ecc1-128">-Confirm</span></span>
<span data-ttu-id="9ecc1-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ecc1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ecc1-130">-WhatIf</span></span>
<span data-ttu-id="9ecc1-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ecc1-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ecc1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ecc1-133">CommonParameters</span></span>
<span data-ttu-id="9ecc1-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ecc1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ecc1-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ecc1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ecc1-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ecc1-136">INPUTS</span></span>

### <span data-ttu-id="9ecc1-137">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9ecc1-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="9ecc1-138">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9ecc1-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9ecc1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9ecc1-139">System.String</span></span>

## <span data-ttu-id="9ecc1-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ecc1-140">OUTPUTS</span></span>

### <span data-ttu-id="9ecc1-141">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9ecc1-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="9ecc1-142">Note</span><span class="sxs-lookup"><span data-stu-id="9ecc1-142">NOTES</span></span>

## <span data-ttu-id="9ecc1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ecc1-143">RELATED LINKS</span></span>

[<span data-ttu-id="9ecc1-144">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="9ecc1-144">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="9ecc1-145">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="9ecc1-145">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="9ecc1-146">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="9ecc1-146">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
