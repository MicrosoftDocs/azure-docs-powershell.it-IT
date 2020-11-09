---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298933"
---
# <span data-ttu-id="6231b-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="6231b-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="6231b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6231b-102">SYNOPSIS</span></span>
<span data-ttu-id="6231b-103">Creare o aggiornare un'associazione.</span><span class="sxs-lookup"><span data-stu-id="6231b-103">Create or update an association.</span></span>

## <span data-ttu-id="6231b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6231b-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6231b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6231b-105">DESCRIPTION</span></span>
<span data-ttu-id="6231b-106">Creare o aggiornare un'associazione.</span><span class="sxs-lookup"><span data-stu-id="6231b-106">Create or update an association.</span></span>

## <span data-ttu-id="6231b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6231b-107">EXAMPLES</span></span>

### <span data-ttu-id="6231b-108">Esempio 1: creare un'associazione di provider personalizzata</span><span class="sxs-lookup"><span data-stu-id="6231b-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="6231b-109">Creare un'associazione di provider personalizzata, la provioder di destinazione associata deve essere configurata correttamente con una route per "Associations"</span><span class="sxs-lookup"><span data-stu-id="6231b-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="6231b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6231b-110">PARAMETERS</span></span>

### <span data-ttu-id="6231b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6231b-111">-AsJob</span></span>
<span data-ttu-id="6231b-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6231b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6231b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6231b-113">-DefaultProfile</span></span>
<span data-ttu-id="6231b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6231b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6231b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6231b-115">-Name</span></span>
<span data-ttu-id="6231b-116">Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="6231b-116">The name of the association.</span></span>

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

### <span data-ttu-id="6231b-117">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="6231b-117">-NoWait</span></span>
<span data-ttu-id="6231b-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6231b-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6231b-119">-Ambito</span><span class="sxs-lookup"><span data-stu-id="6231b-119">-Scope</span></span>
<span data-ttu-id="6231b-120">Ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="6231b-120">The scope of the association.</span></span>
<span data-ttu-id="6231b-121">L'ambito può essere qualsiasi istanza valida della risorsa REST.</span><span class="sxs-lookup"><span data-stu-id="6231b-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="6231b-122">Ad esempio, USA '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' per una risorsa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6231b-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="6231b-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6231b-123">-TargetResourceId</span></span>
<span data-ttu-id="6231b-124">Istanza della risorsa REST della risorsa di destinazione per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="6231b-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="6231b-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6231b-125">-Confirm</span></span>
<span data-ttu-id="6231b-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6231b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6231b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6231b-127">-WhatIf</span></span>
<span data-ttu-id="6231b-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6231b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6231b-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6231b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6231b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6231b-130">CommonParameters</span></span>
<span data-ttu-id="6231b-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6231b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6231b-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6231b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6231b-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6231b-133">INPUTS</span></span>

## <span data-ttu-id="6231b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6231b-134">OUTPUTS</span></span>

### <span data-ttu-id="6231b-135">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="6231b-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="6231b-136">Note</span><span class="sxs-lookup"><span data-stu-id="6231b-136">NOTES</span></span>

<span data-ttu-id="6231b-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6231b-137">ALIASES</span></span>

## <span data-ttu-id="6231b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6231b-138">RELATED LINKS</span></span>

