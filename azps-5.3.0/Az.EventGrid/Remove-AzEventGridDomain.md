---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473907"
---
# <span data-ttu-id="9508b-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="9508b-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="9508b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9508b-102">SYNOPSIS</span></span>
<span data-ttu-id="9508b-103">Rimuove un dominio della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="9508b-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="9508b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9508b-104">SYNTAX</span></span>

### <span data-ttu-id="9508b-105">DomainNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9508b-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9508b-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9508b-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9508b-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9508b-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9508b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9508b-108">DESCRIPTION</span></span>
<span data-ttu-id="9508b-109">Rimuove un dominio della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="9508b-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="9508b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9508b-110">EXAMPLES</span></span>

### <span data-ttu-id="9508b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9508b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="9508b-112">Rimuove il dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9508b-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9508b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9508b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="9508b-114">Rimuove il dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9508b-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="9508b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9508b-115">PARAMETERS</span></span>

### <span data-ttu-id="9508b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9508b-116">-DefaultProfile</span></span>
<span data-ttu-id="9508b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9508b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9508b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9508b-118">-InputObject</span></span>
<span data-ttu-id="9508b-119">Oggetto di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9508b-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9508b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9508b-120">-Name</span></span>
<span data-ttu-id="9508b-121">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="9508b-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9508b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9508b-122">-PassThru</span></span>
<span data-ttu-id="9508b-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9508b-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9508b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9508b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9508b-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9508b-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9508b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9508b-126">-ResourceId</span></span>
<span data-ttu-id="9508b-127">Identificatore delle risorse che rappresenta il dominio della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="9508b-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9508b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9508b-128">-Confirm</span></span>
<span data-ttu-id="9508b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9508b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9508b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9508b-130">-WhatIf</span></span>
<span data-ttu-id="9508b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9508b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9508b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9508b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9508b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9508b-133">CommonParameters</span></span>
<span data-ttu-id="9508b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9508b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9508b-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9508b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9508b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9508b-136">INPUTS</span></span>

### <span data-ttu-id="9508b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9508b-137">System.String</span></span>

### <span data-ttu-id="9508b-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="9508b-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="9508b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9508b-139">OUTPUTS</span></span>

### <span data-ttu-id="9508b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9508b-140">System.Boolean</span></span>

## <span data-ttu-id="9508b-141">Note</span><span class="sxs-lookup"><span data-stu-id="9508b-141">NOTES</span></span>

## <span data-ttu-id="9508b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9508b-142">RELATED LINKS</span></span>
