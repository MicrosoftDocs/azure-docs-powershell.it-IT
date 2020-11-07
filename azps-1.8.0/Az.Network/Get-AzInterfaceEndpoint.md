---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678521"
---
# <span data-ttu-id="99a06-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="99a06-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="99a06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99a06-102">SYNOPSIS</span></span>
<span data-ttu-id="99a06-103">Il cmdlet Get-AzInterfaceEndpoint ottiene un endpoint di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="99a06-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="99a06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99a06-104">SYNTAX</span></span>

### <span data-ttu-id="99a06-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99a06-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99a06-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99a06-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99a06-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99a06-107">DESCRIPTION</span></span>
<span data-ttu-id="99a06-108">Il cmdlet **Get-AzInterfaceEndpoint** ottiene un endpoint di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="99a06-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="99a06-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99a06-109">EXAMPLES</span></span>

### <span data-ttu-id="99a06-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99a06-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="99a06-111">Questo comando ottiene l'endpoint di interfaccia denominato InterfaceEndpoint1 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="99a06-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="99a06-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="99a06-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="99a06-113">Questo comando ottiene l'endpoint dell'interfaccia con resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 e lo archivia nella variabile $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="99a06-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="99a06-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="99a06-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="99a06-115">Questo comando consente di ottenere gli endpoint di interfaccia che iniziano con "InterfaceEndpoint"</span><span class="sxs-lookup"><span data-stu-id="99a06-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="99a06-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99a06-116">PARAMETERS</span></span>

### <span data-ttu-id="99a06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a06-117">-DefaultProfile</span></span>
<span data-ttu-id="99a06-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99a06-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99a06-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="99a06-119">-Name</span></span>
<span data-ttu-id="99a06-120">Nome dell'endpoint di interfaccia</span><span class="sxs-lookup"><span data-stu-id="99a06-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="99a06-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a06-121">-ResourceGroupName</span></span>
<span data-ttu-id="99a06-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99a06-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="99a06-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99a06-123">-ResourceId</span></span>
<span data-ttu-id="99a06-124">ID dell'endpoint dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="99a06-124">The ID of the interface endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a06-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99a06-125">-Confirm</span></span>
<span data-ttu-id="99a06-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99a06-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99a06-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99a06-127">-WhatIf</span></span>
<span data-ttu-id="99a06-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99a06-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99a06-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99a06-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99a06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a06-130">CommonParameters</span></span>
<span data-ttu-id="99a06-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a06-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99a06-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a06-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99a06-133">INPUTS</span></span>

### <span data-ttu-id="99a06-134">System. String</span><span class="sxs-lookup"><span data-stu-id="99a06-134">System.String</span></span>

## <span data-ttu-id="99a06-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99a06-135">OUTPUTS</span></span>

### <span data-ttu-id="99a06-136">Microsoft. Azure. Commands. Network. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="99a06-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="99a06-137">Note</span><span class="sxs-lookup"><span data-stu-id="99a06-137">NOTES</span></span>

## <span data-ttu-id="99a06-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99a06-138">RELATED LINKS</span></span>
