---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98485792"
---
# <span data-ttu-id="8357b-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="8357b-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="8357b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8357b-102">SYNOPSIS</span></span>
<span data-ttu-id="8357b-103">Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="8357b-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="8357b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8357b-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8357b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8357b-105">DESCRIPTION</span></span>
<span data-ttu-id="8357b-106">Usare **Update-AzServiceFabricDurability** per aggiornare la durabilità o il SKU del cluster.</span><span class="sxs-lookup"><span data-stu-id="8357b-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="8357b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8357b-107">EXAMPLES</span></span>

### <span data-ttu-id="8357b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8357b-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="8357b-109">Questo comando modifica il livello di durabilità di NodeType ' NT1' in Silver.</span><span class="sxs-lookup"><span data-stu-id="8357b-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="8357b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8357b-110">PARAMETERS</span></span>

### <span data-ttu-id="8357b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8357b-111">-DefaultProfile</span></span>
<span data-ttu-id="8357b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8357b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8357b-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="8357b-113">-DurabilityLevel</span></span>
<span data-ttu-id="8357b-114">Specificare il livello di durabilità.</span><span class="sxs-lookup"><span data-stu-id="8357b-114">Specify durability level.</span></span>

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

### <span data-ttu-id="8357b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8357b-115">-Name</span></span>
<span data-ttu-id="8357b-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="8357b-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8357b-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="8357b-117">-NodeType</span></span>
<span data-ttu-id="8357b-118">Specificare il nome del tipo di nodo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8357b-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="8357b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8357b-119">-ResourceGroupName</span></span>
<span data-ttu-id="8357b-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8357b-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8357b-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="8357b-121">-Sku</span></span>
<span data-ttu-id="8357b-122">Specificare l'USK del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="8357b-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="8357b-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8357b-123">-Confirm</span></span>
<span data-ttu-id="8357b-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8357b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8357b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8357b-125">-WhatIf</span></span>
<span data-ttu-id="8357b-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8357b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8357b-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8357b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8357b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8357b-128">CommonParameters</span></span>
<span data-ttu-id="8357b-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8357b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8357b-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8357b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8357b-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8357b-131">INPUTS</span></span>

### <span data-ttu-id="8357b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8357b-132">System.String</span></span>

### <span data-ttu-id="8357b-133">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="8357b-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="8357b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8357b-134">OUTPUTS</span></span>

### <span data-ttu-id="8357b-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="8357b-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="8357b-136">Note</span><span class="sxs-lookup"><span data-stu-id="8357b-136">NOTES</span></span>

## <span data-ttu-id="8357b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8357b-137">RELATED LINKS</span></span>
