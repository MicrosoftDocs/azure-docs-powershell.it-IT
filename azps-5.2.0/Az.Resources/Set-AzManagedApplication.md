---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351760"
---
# <span data-ttu-id="a11e4-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="a11e4-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="a11e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a11e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a11e4-103">Applicazione gestita degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="a11e4-103">Updates managed application</span></span>

## <span data-ttu-id="a11e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a11e4-104">SYNTAX</span></span>

### <span data-ttu-id="a11e4-105">SetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a11e4-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a11e4-106">SetById</span><span class="sxs-lookup"><span data-stu-id="a11e4-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a11e4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a11e4-107">DESCRIPTION</span></span>
<span data-ttu-id="a11e4-108">Il cmdlet **set-AzManagedApplication** aggiorna le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="a11e4-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="a11e4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a11e4-109">EXAMPLES</span></span>

### <span data-ttu-id="a11e4-110">Esempio 1: aggiornare la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="a11e4-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="a11e4-111">Questo comando Aggiorna la descrizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="a11e4-111">This command updates the managed application description</span></span>

## <span data-ttu-id="a11e4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a11e4-112">PARAMETERS</span></span>

### <span data-ttu-id="a11e4-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a11e4-113">-ApiVersion</span></span>
<span data-ttu-id="a11e4-114">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a11e4-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a11e4-115">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="a11e4-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a11e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11e4-116">-DefaultProfile</span></span>
<span data-ttu-id="a11e4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a11e4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a11e4-118">-ID</span><span class="sxs-lookup"><span data-stu-id="a11e4-118">-Id</span></span>
<span data-ttu-id="a11e4-119">ID applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a11e4-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="a11e4-120">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11e4-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="a11e4-121">-Tipo</span><span class="sxs-lookup"><span data-stu-id="a11e4-121">-Kind</span></span>
<span data-ttu-id="a11e4-122">Tipo di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="a11e4-122">The managed application kind.</span></span>
<span data-ttu-id="a11e4-123">Uno di Marketplace o servicecatalog</span><span class="sxs-lookup"><span data-stu-id="a11e4-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="a11e4-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a11e4-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="a11e4-125">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="a11e4-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="a11e4-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11e4-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="a11e4-127">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="a11e4-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="a11e4-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="a11e4-128">-Name</span></span>
<span data-ttu-id="a11e4-129">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="a11e4-129">The managed application name.</span></span>

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

### <span data-ttu-id="a11e4-130">Parametro-</span><span class="sxs-lookup"><span data-stu-id="a11e4-130">-Parameter</span></span>
<span data-ttu-id="a11e4-131">Stringa formattata JSON di parametri per l'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="a11e4-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="a11e4-132">Può trattarsi di un percorso di un nome file o di un URI che contiene i parametri oppure i parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="a11e4-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="a11e4-133">-Piano</span><span class="sxs-lookup"><span data-stu-id="a11e4-133">-Plan</span></span>
<span data-ttu-id="a11e4-134">Tabella hash che rappresenta le proprietà del piano applicazione gestite.</span><span class="sxs-lookup"><span data-stu-id="a11e4-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="a11e4-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="a11e4-135">-Pre</span></span>
<span data-ttu-id="a11e4-136">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a11e4-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a11e4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11e4-137">-ResourceGroupName</span></span>
<span data-ttu-id="a11e4-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a11e4-138">The resource group name.</span></span>

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

### <span data-ttu-id="a11e4-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a11e4-139">-Tag</span></span>
<span data-ttu-id="a11e4-140">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a11e4-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="a11e4-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a11e4-141">-Confirm</span></span>
<span data-ttu-id="a11e4-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a11e4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a11e4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a11e4-143">-WhatIf</span></span>
<span data-ttu-id="a11e4-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a11e4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a11e4-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a11e4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a11e4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11e4-146">CommonParameters</span></span>
<span data-ttu-id="a11e4-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a11e4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11e4-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a11e4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11e4-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a11e4-149">INPUTS</span></span>

### <span data-ttu-id="a11e4-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a11e4-150">System.String</span></span>

### <span data-ttu-id="a11e4-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a11e4-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a11e4-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a11e4-152">OUTPUTS</span></span>

### <span data-ttu-id="a11e4-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a11e4-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a11e4-154">Note</span><span class="sxs-lookup"><span data-stu-id="a11e4-154">NOTES</span></span>

## <span data-ttu-id="a11e4-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a11e4-155">RELATED LINKS</span></span>
