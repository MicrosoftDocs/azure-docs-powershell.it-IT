---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: af502cd4115ba9ef7467c15aa09b78e5e33c2337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998772"
---
# <span data-ttu-id="1a21a-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="1a21a-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="1a21a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a21a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a21a-103">Creare o aggiornare un'associazione.</span><span class="sxs-lookup"><span data-stu-id="1a21a-103">Create or update an association.</span></span>

## <span data-ttu-id="1a21a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a21a-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a21a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1a21a-105">DESCRIPTION</span></span>
<span data-ttu-id="1a21a-106">Creare o aggiornare un'associazione.</span><span class="sxs-lookup"><span data-stu-id="1a21a-106">Create or update an association.</span></span>

## <span data-ttu-id="1a21a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a21a-107">EXAMPLES</span></span>

### <span data-ttu-id="1a21a-108">Esempio 1: Creare un'associazione di provider personalizzata</span><span class="sxs-lookup"><span data-stu-id="1a21a-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="1a21a-109">Creare un'associazione di provider personalizzata. Il provioder di destinazione associato deve essere configurato correttamente con un percorso per le "associazioni"</span><span class="sxs-lookup"><span data-stu-id="1a21a-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="1a21a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a21a-110">PARAMETERS</span></span>

### <span data-ttu-id="1a21a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a21a-111">-AsJob</span></span>
<span data-ttu-id="1a21a-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1a21a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1a21a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a21a-113">-DefaultProfile</span></span>
<span data-ttu-id="1a21a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a21a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a21a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1a21a-115">-Name</span></span>
<span data-ttu-id="1a21a-116">Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="1a21a-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a21a-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1a21a-117">-NoWait</span></span>
<span data-ttu-id="1a21a-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1a21a-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1a21a-119">-Scope</span><span class="sxs-lookup"><span data-stu-id="1a21a-119">-Scope</span></span>
<span data-ttu-id="1a21a-120">Ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="1a21a-120">The scope of the association.</span></span>
<span data-ttu-id="1a21a-121">L'ambito può essere qualsiasi istanza di risorsa REST valida.</span><span class="sxs-lookup"><span data-stu-id="1a21a-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="1a21a-122">Ad esempio, usare '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' per una risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1a21a-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a21a-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1a21a-123">-TargetResourceId</span></span>
<span data-ttu-id="1a21a-124">Istanza della risorsa REST della risorsa di destinazione per questa associazione.</span><span class="sxs-lookup"><span data-stu-id="1a21a-124">The REST resource instance of the target resource for this association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a21a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a21a-125">-Confirm</span></span>
<span data-ttu-id="1a21a-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a21a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a21a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a21a-127">-WhatIf</span></span>
<span data-ttu-id="1a21a-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a21a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a21a-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a21a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a21a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a21a-130">CommonParameters</span></span>
<span data-ttu-id="1a21a-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a21a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a21a-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a21a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a21a-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="1a21a-133">INPUTS</span></span>

## <span data-ttu-id="1a21a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a21a-134">OUTPUTS</span></span>

### <span data-ttu-id="1a21a-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="1a21a-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="1a21a-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="1a21a-136">NOTES</span></span>

<span data-ttu-id="1a21a-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1a21a-137">ALIASES</span></span>

## <span data-ttu-id="1a21a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a21a-138">RELATED LINKS</span></span>

