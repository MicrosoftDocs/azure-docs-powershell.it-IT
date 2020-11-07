---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 283ca228ba44d2ec87cd926d23e0217eb67434eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677058"
---
# <span data-ttu-id="bc6a3-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="bc6a3-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="bc6a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6a3-103">Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="bc6a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc6a3-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc6a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc6a3-105">DESCRIPTION</span></span>
<span data-ttu-id="bc6a3-106">Usare **Update-AzServiceFabricDurability** per aggiornare la durabilità o il SKU del cluster.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="bc6a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc6a3-107">EXAMPLES</span></span>

### <span data-ttu-id="bc6a3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc6a3-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="bc6a3-109">Questo comando modifica il livello di durabilità di NodeType ' NT1' in Silver.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="bc6a3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc6a3-110">PARAMETERS</span></span>

### <span data-ttu-id="bc6a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6a3-111">-DefaultProfile</span></span>
<span data-ttu-id="bc6a3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc6a3-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="bc6a3-113">-DurabilityLevel</span></span>
<span data-ttu-id="bc6a3-114">Specificare il livello di durabilità.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-114">Specify durability level.</span></span>

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

### <span data-ttu-id="bc6a3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc6a3-115">-Name</span></span>
<span data-ttu-id="bc6a3-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="bc6a3-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="bc6a3-117">-NodeType</span></span>
<span data-ttu-id="bc6a3-118">Specificare il nome del tipo di nodo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="bc6a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc6a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="bc6a3-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bc6a3-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="bc6a3-121">-Sku</span></span>
<span data-ttu-id="bc6a3-122">Specificare l'USK del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="bc6a3-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc6a3-123">-Confirm</span></span>
<span data-ttu-id="bc6a3-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc6a3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc6a3-125">-WhatIf</span></span>
<span data-ttu-id="bc6a3-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc6a3-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc6a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6a3-128">CommonParameters</span></span>
<span data-ttu-id="bc6a3-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc6a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6a3-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc6a3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6a3-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc6a3-131">INPUTS</span></span>

### <span data-ttu-id="bc6a3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bc6a3-132">System.String</span></span>

### <span data-ttu-id="bc6a3-133">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="bc6a3-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="bc6a3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc6a3-134">OUTPUTS</span></span>

### <span data-ttu-id="bc6a3-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="bc6a3-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bc6a3-136">Note</span><span class="sxs-lookup"><span data-stu-id="bc6a3-136">NOTES</span></span>

## <span data-ttu-id="bc6a3-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc6a3-137">RELATED LINKS</span></span>
