---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: a2acea388b34b23d4977fa65ae6e6e6d4702525b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979374"
---
# <span data-ttu-id="b3504-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="b3504-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="b3504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3504-102">SYNOPSIS</span></span>
<span data-ttu-id="b3504-103">Aggiorna l'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="b3504-103">Updates managed application</span></span>

## <span data-ttu-id="b3504-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3504-104">SYNTAX</span></span>

### <span data-ttu-id="b3504-105">SetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3504-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3504-106">SetById</span><span class="sxs-lookup"><span data-stu-id="b3504-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3504-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b3504-107">DESCRIPTION</span></span>
<span data-ttu-id="b3504-108">Il cmdlet **Set-AzManagedApplication** aggiorna le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="b3504-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="b3504-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3504-109">EXAMPLES</span></span>

### <span data-ttu-id="b3504-110">Esempio 1: Aggiornare la descrizione della definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="b3504-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="b3504-111">Questo comando aggiorna la descrizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="b3504-111">This command updates the managed application description</span></span>

## <span data-ttu-id="b3504-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3504-112">PARAMETERS</span></span>

### <span data-ttu-id="b3504-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b3504-113">-ApiVersion</span></span>
<span data-ttu-id="b3504-114">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="b3504-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b3504-115">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="b3504-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b3504-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3504-116">-DefaultProfile</span></span>
<span data-ttu-id="b3504-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3504-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3504-118">-Id</span><span class="sxs-lookup"><span data-stu-id="b3504-118">-Id</span></span>
<span data-ttu-id="b3504-119">ID applicazione gestita completo, inclusa la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b3504-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="b3504-120">ad esempio /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3504-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="b3504-121">-Kind</span></span>
<span data-ttu-id="b3504-122">Il tipo di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="b3504-122">The managed application kind.</span></span>
<span data-ttu-id="b3504-123">Uno dei marketplace o servicecatalog</span><span class="sxs-lookup"><span data-stu-id="b3504-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="b3504-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b3504-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="b3504-125">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="b3504-125">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3504-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="b3504-127">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="b3504-127">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b3504-128">-Name</span></span>
<span data-ttu-id="b3504-129">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="b3504-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b3504-130">-Parameter</span></span>
<span data-ttu-id="b3504-131">Stringa di parametri in formato JSON per l'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="b3504-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="b3504-132">Può trattarsi del percorso di un nome file o di un URI contenente i parametri oppure dei parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="b3504-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="b3504-133">-Plan</span></span>
<span data-ttu-id="b3504-134">Tabella hash che rappresenta le proprietà del piano di applicazioni gestite.</span><span class="sxs-lookup"><span data-stu-id="b3504-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="b3504-135">-Pre</span></span>
<span data-ttu-id="b3504-136">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b3504-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b3504-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3504-137">-ResourceGroupName</span></span>
<span data-ttu-id="b3504-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3504-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3504-139">-Tag</span></span>
<span data-ttu-id="b3504-140">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3504-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3504-141">-Confirm</span></span>
<span data-ttu-id="b3504-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3504-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3504-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3504-143">-WhatIf</span></span>
<span data-ttu-id="b3504-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3504-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3504-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3504-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3504-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3504-146">CommonParameters</span></span>
<span data-ttu-id="b3504-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3504-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3504-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3504-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3504-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="b3504-149">INPUTS</span></span>

### <span data-ttu-id="b3504-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b3504-150">System.String</span></span>

### <span data-ttu-id="b3504-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b3504-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b3504-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3504-152">OUTPUTS</span></span>

### <span data-ttu-id="b3504-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b3504-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b3504-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="b3504-154">NOTES</span></span>

## <span data-ttu-id="b3504-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3504-155">RELATED LINKS</span></span>
