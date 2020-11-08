---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 871583629936afe763032d1ce3e98ed4464298f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021678"
---
# <span data-ttu-id="d8afe-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="d8afe-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="d8afe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8afe-102">SYNOPSIS</span></span>
<span data-ttu-id="d8afe-103">Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="d8afe-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="d8afe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8afe-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8afe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8afe-105">DESCRIPTION</span></span>
<span data-ttu-id="d8afe-106">Usare **Update-AzServiceFabricDurability** per aggiornare la durabilità o il SKU del cluster.</span><span class="sxs-lookup"><span data-stu-id="d8afe-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="d8afe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8afe-107">EXAMPLES</span></span>

### <span data-ttu-id="d8afe-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8afe-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="d8afe-109">Questo comando modifica il livello di durabilità di NodeType ' NT1' in Silver.</span><span class="sxs-lookup"><span data-stu-id="d8afe-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="d8afe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8afe-110">PARAMETERS</span></span>

### <span data-ttu-id="d8afe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8afe-111">-DefaultProfile</span></span>
<span data-ttu-id="d8afe-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8afe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8afe-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="d8afe-113">-DurabilityLevel</span></span>
<span data-ttu-id="d8afe-114">Specificare il livello di durabilità.</span><span class="sxs-lookup"><span data-stu-id="d8afe-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8afe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8afe-115">-Name</span></span>
<span data-ttu-id="d8afe-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="d8afe-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8afe-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="d8afe-117">-NodeType</span></span>
<span data-ttu-id="d8afe-118">Specificare il nome del tipo di nodo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d8afe-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8afe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8afe-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8afe-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8afe-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8afe-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="d8afe-121">-Sku</span></span>
<span data-ttu-id="d8afe-122">Specificare l'USK del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="d8afe-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8afe-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d8afe-123">-Confirm</span></span>
<span data-ttu-id="d8afe-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8afe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8afe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8afe-125">-WhatIf</span></span>
<span data-ttu-id="d8afe-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8afe-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8afe-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8afe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8afe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8afe-128">CommonParameters</span></span>
<span data-ttu-id="d8afe-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8afe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8afe-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8afe-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8afe-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8afe-131">INPUTS</span></span>

### <span data-ttu-id="d8afe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d8afe-132">System.String</span></span>

### <span data-ttu-id="d8afe-133">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="d8afe-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="d8afe-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8afe-134">OUTPUTS</span></span>

### <span data-ttu-id="d8afe-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="d8afe-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d8afe-136">Note</span><span class="sxs-lookup"><span data-stu-id="d8afe-136">NOTES</span></span>

## <span data-ttu-id="d8afe-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8afe-137">RELATED LINKS</span></span>
