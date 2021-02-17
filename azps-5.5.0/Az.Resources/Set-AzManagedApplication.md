---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186327"
---
# <span data-ttu-id="87a06-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="87a06-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="87a06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a06-102">SYNOPSIS</span></span>
<span data-ttu-id="87a06-103">Aggiorna l'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="87a06-103">Updates managed application</span></span>

## <span data-ttu-id="87a06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87a06-104">SYNTAX</span></span>

### <span data-ttu-id="87a06-105">SetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87a06-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87a06-106">SetById</span><span class="sxs-lookup"><span data-stu-id="87a06-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87a06-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="87a06-107">DESCRIPTION</span></span>
<span data-ttu-id="87a06-108">Il cmdlet **Set-AzManagedApplication** aggiorna le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="87a06-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="87a06-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87a06-109">EXAMPLES</span></span>

### <span data-ttu-id="87a06-110">Esempio 1: Aggiornare la descrizione della definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="87a06-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="87a06-111">Questo comando aggiorna la descrizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="87a06-111">This command updates the managed application description</span></span>

## <span data-ttu-id="87a06-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87a06-112">PARAMETERS</span></span>

### <span data-ttu-id="87a06-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="87a06-113">-ApiVersion</span></span>
<span data-ttu-id="87a06-114">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="87a06-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="87a06-115">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="87a06-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="87a06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a06-116">-DefaultProfile</span></span>
<span data-ttu-id="87a06-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87a06-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87a06-118">-Id</span><span class="sxs-lookup"><span data-stu-id="87a06-118">-Id</span></span>
<span data-ttu-id="87a06-119">ID applicazione gestita completo, inclusa la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="87a06-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="87a06-120">ad esempio /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a06-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="87a06-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="87a06-121">-Kind</span></span>
<span data-ttu-id="87a06-122">Il tipo di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="87a06-122">The managed application kind.</span></span>
<span data-ttu-id="87a06-123">Uno dei marketplace o servicecatalog</span><span class="sxs-lookup"><span data-stu-id="87a06-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="87a06-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="87a06-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="87a06-125">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="87a06-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="87a06-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a06-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="87a06-127">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="87a06-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="87a06-128">-Name</span><span class="sxs-lookup"><span data-stu-id="87a06-128">-Name</span></span>
<span data-ttu-id="87a06-129">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="87a06-129">The managed application name.</span></span>

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

### <span data-ttu-id="87a06-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="87a06-130">-Parameter</span></span>
<span data-ttu-id="87a06-131">Stringa di parametri in formato JSON per l'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="87a06-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="87a06-132">Può trattarsi del percorso di un nome file o di un URI contenente i parametri oppure dei parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="87a06-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="87a06-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="87a06-133">-Plan</span></span>
<span data-ttu-id="87a06-134">Tabella hash che rappresenta le proprietà del piano di applicazioni gestite.</span><span class="sxs-lookup"><span data-stu-id="87a06-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="87a06-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="87a06-135">-Pre</span></span>
<span data-ttu-id="87a06-136">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="87a06-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="87a06-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a06-137">-ResourceGroupName</span></span>
<span data-ttu-id="87a06-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87a06-138">The resource group name.</span></span>

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

### <span data-ttu-id="87a06-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="87a06-139">-Tag</span></span>
<span data-ttu-id="87a06-140">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="87a06-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="87a06-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87a06-141">-Confirm</span></span>
<span data-ttu-id="87a06-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87a06-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a06-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a06-143">-WhatIf</span></span>
<span data-ttu-id="87a06-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87a06-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87a06-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87a06-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a06-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a06-146">CommonParameters</span></span>
<span data-ttu-id="87a06-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a06-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a06-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="87a06-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a06-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="87a06-149">INPUTS</span></span>

### <span data-ttu-id="87a06-150">System.String</span><span class="sxs-lookup"><span data-stu-id="87a06-150">System.String</span></span>

### <span data-ttu-id="87a06-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="87a06-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87a06-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87a06-152">OUTPUTS</span></span>

### <span data-ttu-id="87a06-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="87a06-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="87a06-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="87a06-154">NOTES</span></span>

## <span data-ttu-id="87a06-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87a06-155">RELATED LINKS</span></span>
