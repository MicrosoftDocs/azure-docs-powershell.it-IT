---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 30e3e7f7b6ace383a2c492f4dcc088f65dfea08b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999822"
---
# <span data-ttu-id="28aba-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="28aba-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="28aba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28aba-102">SYNOPSIS</span></span>
<span data-ttu-id="28aba-103">Crea un'applicazione gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="28aba-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="28aba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28aba-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28aba-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="28aba-105">DESCRIPTION</span></span>
<span data-ttu-id="28aba-106">Il cmdlet **New-AzManagedApplication** crea un'applicazione gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="28aba-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="28aba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28aba-107">EXAMPLES</span></span>

### <span data-ttu-id="28aba-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28aba-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="28aba-109">Questo comando crea un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="28aba-109">This command creates a managed application</span></span>

## <span data-ttu-id="28aba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28aba-110">PARAMETERS</span></span>

### <span data-ttu-id="28aba-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="28aba-111">-ApiVersion</span></span>
<span data-ttu-id="28aba-112">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="28aba-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="28aba-113">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="28aba-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="28aba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28aba-114">-DefaultProfile</span></span>
<span data-ttu-id="28aba-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28aba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28aba-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="28aba-116">-Kind</span></span>
<span data-ttu-id="28aba-117">Il tipo di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="28aba-117">The managed application kind.</span></span>
<span data-ttu-id="28aba-118">Uno dei marketplace o servicecatalog</span><span class="sxs-lookup"><span data-stu-id="28aba-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28aba-119">-Location</span><span class="sxs-lookup"><span data-stu-id="28aba-119">-Location</span></span>
<span data-ttu-id="28aba-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="28aba-120">The resource location.</span></span>

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

### <span data-ttu-id="28aba-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="28aba-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="28aba-122">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="28aba-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="28aba-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28aba-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="28aba-124">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="28aba-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="28aba-125">-Name</span><span class="sxs-lookup"><span data-stu-id="28aba-125">-Name</span></span>
<span data-ttu-id="28aba-126">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="28aba-126">The managed application name.</span></span>

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

### <span data-ttu-id="28aba-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="28aba-127">-Parameter</span></span>
<span data-ttu-id="28aba-128">Stringa di parametri in formato JSON per l'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="28aba-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="28aba-129">Può trattarsi del percorso di un nome file o di un URI contenente i parametri oppure dei parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="28aba-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="28aba-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="28aba-130">-Plan</span></span>
<span data-ttu-id="28aba-131">Tabella hash che rappresenta le proprietà del piano di applicazioni gestite.</span><span class="sxs-lookup"><span data-stu-id="28aba-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="28aba-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="28aba-132">-Pre</span></span>
<span data-ttu-id="28aba-133">Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="28aba-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="28aba-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28aba-134">-ResourceGroupName</span></span>
<span data-ttu-id="28aba-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="28aba-135">The resource group name.</span></span>

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

### <span data-ttu-id="28aba-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="28aba-136">-Tag</span></span>
<span data-ttu-id="28aba-137">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="28aba-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="28aba-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28aba-138">-Confirm</span></span>
<span data-ttu-id="28aba-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28aba-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28aba-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28aba-140">-WhatIf</span></span>
<span data-ttu-id="28aba-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28aba-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28aba-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28aba-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28aba-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28aba-143">CommonParameters</span></span>
<span data-ttu-id="28aba-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28aba-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28aba-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28aba-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28aba-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="28aba-146">INPUTS</span></span>

### <span data-ttu-id="28aba-147">System.String</span><span class="sxs-lookup"><span data-stu-id="28aba-147">System.String</span></span>

### <span data-ttu-id="28aba-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="28aba-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="28aba-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28aba-149">OUTPUTS</span></span>

### <span data-ttu-id="28aba-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="28aba-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="28aba-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="28aba-151">NOTES</span></span>

## <span data-ttu-id="28aba-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28aba-152">RELATED LINKS</span></span>
