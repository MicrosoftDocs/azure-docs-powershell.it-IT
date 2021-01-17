---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488955"
---
# <span data-ttu-id="8a52a-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a52a-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="8a52a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a52a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a52a-103">Rimuove un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="8a52a-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="8a52a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a52a-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a52a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a52a-105">DESCRIPTION</span></span>
<span data-ttu-id="8a52a-106">Il cmdlet **Remove-AzPrivateEndpoint** rimuove un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="8a52a-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="8a52a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a52a-107">EXAMPLES</span></span>

### <span data-ttu-id="8a52a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8a52a-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="8a52a-109">In questo esempio viene rimosso un endpoint privato denominato MyPrivateEndpoint1.</span><span class="sxs-lookup"><span data-stu-id="8a52a-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="8a52a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a52a-110">PARAMETERS</span></span>

### <span data-ttu-id="8a52a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a52a-111">-AsJob</span></span>
<span data-ttu-id="8a52a-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8a52a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a52a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a52a-113">-DefaultProfile</span></span>
<span data-ttu-id="8a52a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a52a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a52a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a52a-115">-Force</span></span>
<span data-ttu-id="8a52a-116">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="8a52a-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8a52a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a52a-117">-Name</span></span>
<span data-ttu-id="8a52a-118">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="8a52a-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="8a52a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a52a-119">-PassThru</span></span>
<span data-ttu-id="8a52a-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8a52a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a52a-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8a52a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8a52a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a52a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a52a-123">Il nome del gruppo di risorse dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="8a52a-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="8a52a-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a52a-124">-Confirm</span></span>
<span data-ttu-id="8a52a-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a52a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a52a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a52a-126">-WhatIf</span></span>
<span data-ttu-id="8a52a-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a52a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a52a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a52a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a52a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a52a-129">CommonParameters</span></span>
<span data-ttu-id="8a52a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a52a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a52a-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a52a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a52a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a52a-132">INPUTS</span></span>

### <span data-ttu-id="8a52a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8a52a-133">System.String</span></span>

## <span data-ttu-id="8a52a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a52a-134">OUTPUTS</span></span>

### <span data-ttu-id="8a52a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a52a-135">System.Boolean</span></span>

## <span data-ttu-id="8a52a-136">Note</span><span class="sxs-lookup"><span data-stu-id="8a52a-136">NOTES</span></span>

## <span data-ttu-id="8a52a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a52a-137">RELATED LINKS</span></span>

[<span data-ttu-id="8a52a-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a52a-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="8a52a-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a52a-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)