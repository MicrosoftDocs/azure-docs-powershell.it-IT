---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 8d0bd6f046bbff99d93b0ed5dc7385d8ec772811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005422"
---
# <span data-ttu-id="3da85-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="3da85-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="3da85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3da85-102">SYNOPSIS</span></span>
<span data-ttu-id="3da85-103">Rimuovere un tipo di nodo completo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="3da85-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="3da85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3da85-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3da85-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3da85-105">DESCRIPTION</span></span>
<span data-ttu-id="3da85-106">Usare **Remove-AzServiceFabricNodeType** per rimuovere tutti i nodi da uno specifico tipo di nodo e il tipo di nodo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="3da85-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="3da85-107">Questo comando non può essere usato per eliminare il tipo di nodo primario.</span><span class="sxs-lookup"><span data-stu-id="3da85-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="3da85-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3da85-108">EXAMPLES</span></span>

### <span data-ttu-id="3da85-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3da85-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="3da85-110">Questo comando rimuove nodeType 'nt1' dal cluster.</span><span class="sxs-lookup"><span data-stu-id="3da85-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="3da85-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3da85-111">PARAMETERS</span></span>

### <span data-ttu-id="3da85-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da85-112">-DefaultProfile</span></span>
<span data-ttu-id="3da85-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3da85-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3da85-114">-Name</span><span class="sxs-lookup"><span data-stu-id="3da85-114">-Name</span></span>
<span data-ttu-id="3da85-115">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="3da85-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="3da85-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="3da85-116">-NodeType</span></span>
<span data-ttu-id="3da85-117">Nome del tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="3da85-117">The node type name</span></span>

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

### <span data-ttu-id="3da85-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da85-118">-ResourceGroupName</span></span>
<span data-ttu-id="3da85-119">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3da85-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="3da85-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3da85-120">-Confirm</span></span>
<span data-ttu-id="3da85-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3da85-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3da85-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3da85-122">-WhatIf</span></span>
<span data-ttu-id="3da85-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3da85-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3da85-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3da85-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3da85-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da85-125">CommonParameters</span></span>
<span data-ttu-id="3da85-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da85-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da85-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3da85-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da85-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="3da85-128">INPUTS</span></span>

### <span data-ttu-id="3da85-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3da85-129">System.String</span></span>

## <span data-ttu-id="3da85-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3da85-130">OUTPUTS</span></span>

### <span data-ttu-id="3da85-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="3da85-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="3da85-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="3da85-132">NOTES</span></span>

## <span data-ttu-id="3da85-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3da85-133">RELATED LINKS</span></span>
