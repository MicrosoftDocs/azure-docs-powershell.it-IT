---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: b83e6738ec16b8f2700f71e066430148332ca3ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854545"
---
# <span data-ttu-id="0c778-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0c778-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="0c778-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c778-102">SYNOPSIS</span></span>
<span data-ttu-id="0c778-103">Rimuovere un tipo di nodo completo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="0c778-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="0c778-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c778-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c778-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c778-105">DESCRIPTION</span></span>
<span data-ttu-id="0c778-106">Usa il **Remove-AzServiceFabricNodeType** per rimuovere tutti i nodi da un tipo di nodo specifico e il tipo di nodo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="0c778-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="0c778-107">Questo comando non può essere usato per eliminare il tipo di nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0c778-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="0c778-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c778-108">EXAMPLES</span></span>

### <span data-ttu-id="0c778-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c778-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="0c778-110">Questo comando consente di rimuovere NodeType ' NT1' dal cluster.</span><span class="sxs-lookup"><span data-stu-id="0c778-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="0c778-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c778-111">PARAMETERS</span></span>

### <span data-ttu-id="0c778-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c778-112">-DefaultProfile</span></span>
<span data-ttu-id="0c778-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c778-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c778-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c778-114">-Name</span></span>
<span data-ttu-id="0c778-115">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="0c778-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="0c778-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0c778-116">-NodeType</span></span>
<span data-ttu-id="0c778-117">Nome del tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="0c778-117">The node type name</span></span>

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

### <span data-ttu-id="0c778-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c778-118">-ResourceGroupName</span></span>
<span data-ttu-id="0c778-119">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c778-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0c778-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c778-120">-Confirm</span></span>
<span data-ttu-id="0c778-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c778-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c778-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c778-122">-WhatIf</span></span>
<span data-ttu-id="0c778-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c778-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c778-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c778-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c778-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c778-125">CommonParameters</span></span>
<span data-ttu-id="0c778-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c778-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c778-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c778-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c778-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c778-128">INPUTS</span></span>

### <span data-ttu-id="0c778-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0c778-129">System.String</span></span>

## <span data-ttu-id="0c778-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c778-130">OUTPUTS</span></span>

### <span data-ttu-id="0c778-131">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0c778-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0c778-132">Note</span><span class="sxs-lookup"><span data-stu-id="0c778-132">NOTES</span></span>

## <span data-ttu-id="0c778-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c778-133">RELATED LINKS</span></span>
