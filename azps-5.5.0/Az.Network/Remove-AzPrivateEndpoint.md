---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191726"
---
# <span data-ttu-id="124b8-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="124b8-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="124b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="124b8-102">SYNOPSIS</span></span>
<span data-ttu-id="124b8-103">Rimuove un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="124b8-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="124b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="124b8-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="124b8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="124b8-105">DESCRIPTION</span></span>
<span data-ttu-id="124b8-106">Il cmdlet **Remove-AzPrivateEndpoint** rimuove un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="124b8-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="124b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="124b8-107">EXAMPLES</span></span>

### <span data-ttu-id="124b8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="124b8-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="124b8-109">Questo esempio rimuove un endpoint privato denominato MyPrivateEndpoint1.</span><span class="sxs-lookup"><span data-stu-id="124b8-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="124b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="124b8-110">PARAMETERS</span></span>

### <span data-ttu-id="124b8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="124b8-111">-AsJob</span></span>
<span data-ttu-id="124b8-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="124b8-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="124b8-113">-DefaultProfile</span></span>
<span data-ttu-id="124b8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="124b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="124b8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="124b8-115">-Force</span></span>
<span data-ttu-id="124b8-116">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="124b8-116">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124b8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="124b8-117">-Name</span></span>
<span data-ttu-id="124b8-118">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="124b8-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="124b8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="124b8-119">-PassThru</span></span>
<span data-ttu-id="124b8-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="124b8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="124b8-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="124b8-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124b8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="124b8-122">-ResourceGroupName</span></span>
<span data-ttu-id="124b8-123">Nome del gruppo di risorse dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="124b8-123">The resource group name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="124b8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="124b8-124">-Confirm</span></span>
<span data-ttu-id="124b8-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="124b8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="124b8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="124b8-126">-WhatIf</span></span>
<span data-ttu-id="124b8-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="124b8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="124b8-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="124b8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="124b8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="124b8-129">CommonParameters</span></span>
<span data-ttu-id="124b8-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="124b8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="124b8-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="124b8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="124b8-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="124b8-132">INPUTS</span></span>

### <span data-ttu-id="124b8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="124b8-133">System.String</span></span>

## <span data-ttu-id="124b8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="124b8-134">OUTPUTS</span></span>

### <span data-ttu-id="124b8-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="124b8-135">System.Boolean</span></span>

## <span data-ttu-id="124b8-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="124b8-136">NOTES</span></span>

## <span data-ttu-id="124b8-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="124b8-137">RELATED LINKS</span></span>

[<span data-ttu-id="124b8-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="124b8-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="124b8-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="124b8-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)