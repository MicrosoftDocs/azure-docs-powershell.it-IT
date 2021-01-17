---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340468"
---
# <span data-ttu-id="4e53b-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4e53b-101">Set-AzSearchService</span></span>

## <span data-ttu-id="4e53b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e53b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e53b-103">Aggiornare un servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e53b-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="4e53b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e53b-104">SYNTAX</span></span>

### <span data-ttu-id="4e53b-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e53b-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e53b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e53b-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e53b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e53b-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e53b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e53b-108">DESCRIPTION</span></span>
<span data-ttu-id="4e53b-109">Il cmdlet **set-AzSearchService** modifica un servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="4e53b-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="4e53b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e53b-110">EXAMPLES</span></span>

### <span data-ttu-id="4e53b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e53b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


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

<span data-ttu-id="4e53b-112">L'esempio cambia il conteggio delle partizioni e il conteggio delle repliche del servizio di ricerca di Azure su 2.</span><span class="sxs-lookup"><span data-stu-id="4e53b-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="4e53b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e53b-113">PARAMETERS</span></span>

### <span data-ttu-id="4e53b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e53b-114">-DefaultProfile</span></span>
<span data-ttu-id="4e53b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e53b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e53b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e53b-116">-InputObject</span></span>
<span data-ttu-id="4e53b-117">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4e53b-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="4e53b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e53b-118">-Name</span></span>
<span data-ttu-id="4e53b-119">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4e53b-119">Search Service name.</span></span>

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

### <span data-ttu-id="4e53b-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="4e53b-120">-PartitionCount</span></span>
<span data-ttu-id="4e53b-121">Conteggio delle partizioni del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4e53b-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="4e53b-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="4e53b-122">-ReplicaCount</span></span>
<span data-ttu-id="4e53b-123">Conteggio della replica del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4e53b-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="4e53b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e53b-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e53b-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e53b-125">Resource Group name.</span></span>

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

### <span data-ttu-id="4e53b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e53b-126">-ResourceId</span></span>
<span data-ttu-id="4e53b-127">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4e53b-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="4e53b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e53b-128">-Confirm</span></span>
<span data-ttu-id="4e53b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e53b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e53b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e53b-130">-WhatIf</span></span>
<span data-ttu-id="4e53b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e53b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e53b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e53b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e53b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e53b-133">CommonParameters</span></span>
<span data-ttu-id="4e53b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e53b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e53b-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e53b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e53b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e53b-136">INPUTS</span></span>

### <span data-ttu-id="4e53b-137">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4e53b-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="4e53b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4e53b-138">System.String</span></span>

## <span data-ttu-id="4e53b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e53b-139">OUTPUTS</span></span>

### <span data-ttu-id="4e53b-140">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4e53b-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="4e53b-141">Note</span><span class="sxs-lookup"><span data-stu-id="4e53b-141">NOTES</span></span>

## <span data-ttu-id="4e53b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e53b-142">RELATED LINKS</span></span>

[<span data-ttu-id="4e53b-143">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4e53b-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="4e53b-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4e53b-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="4e53b-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4e53b-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)