---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 870769c6bb2557b2a654b4625d3f2c7ea1b4293e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512323"
---
# <span data-ttu-id="dda49-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="dda49-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="dda49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dda49-102">SYNOPSIS</span></span>
<span data-ttu-id="dda49-103">Applicazione gestita degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="dda49-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dda49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dda49-104">SYNTAX</span></span>

### <span data-ttu-id="dda49-105">SetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dda49-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dda49-106">SetById</span><span class="sxs-lookup"><span data-stu-id="dda49-106">SetById</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda49-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dda49-107">DESCRIPTION</span></span>
<span data-ttu-id="dda49-108">Il cmdlet **set-AzureRmManagedApplication** aggiorna le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="dda49-108">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="dda49-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dda49-109">EXAMPLES</span></span>

### <span data-ttu-id="dda49-110">Esempio 1: aggiornare la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="dda49-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="dda49-111">Questo comando Aggiorna la descrizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="dda49-111">This command updates the managed application description</span></span>

## <span data-ttu-id="dda49-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dda49-112">PARAMETERS</span></span>

### <span data-ttu-id="dda49-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dda49-113">-ApiVersion</span></span>
<span data-ttu-id="dda49-114">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="dda49-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="dda49-115">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="dda49-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda49-116">-DefaultProfile</span></span>
<span data-ttu-id="dda49-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dda49-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-118">-ID</span><span class="sxs-lookup"><span data-stu-id="dda49-118">-Id</span></span>
<span data-ttu-id="dda49-119">ID applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dda49-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="dda49-120">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda49-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-121">-Tipo</span><span class="sxs-lookup"><span data-stu-id="dda49-121">-Kind</span></span>
<span data-ttu-id="dda49-122">Tipo di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="dda49-122">The managed application kind.</span></span>
<span data-ttu-id="dda49-123">Uno di Marketplace o servicecatalog</span><span class="sxs-lookup"><span data-stu-id="dda49-123">One of marketplace or servicecatalog</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="dda49-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="dda49-125">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="dda49-125">The managed resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda49-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="dda49-127">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="dda49-127">The managed resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="dda49-128">-Name</span></span>
<span data-ttu-id="dda49-129">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="dda49-129">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-130">Parametro-</span><span class="sxs-lookup"><span data-stu-id="dda49-130">-Parameter</span></span>
<span data-ttu-id="dda49-131">Stringa formattata JSON di parametri per l'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="dda49-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="dda49-132">Può trattarsi di un percorso di un nome file o di un URI che contiene i parametri oppure i parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="dda49-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-133">-Piano</span><span class="sxs-lookup"><span data-stu-id="dda49-133">-Plan</span></span>
<span data-ttu-id="dda49-134">Tabella hash che rappresenta le proprietà del piano applicazione gestite.</span><span class="sxs-lookup"><span data-stu-id="dda49-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="dda49-135">-Pre</span></span>
<span data-ttu-id="dda49-136">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="dda49-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda49-137">-ResourceGroupName</span></span>
<span data-ttu-id="dda49-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dda49-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="dda49-139">-Tag</span></span>
<span data-ttu-id="dda49-140">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="dda49-140">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dda49-141">-Confirm</span></span>
<span data-ttu-id="dda49-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dda49-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda49-143">-WhatIf</span></span>
<span data-ttu-id="dda49-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dda49-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda49-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dda49-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda49-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda49-146">CommonParameters</span></span>
<span data-ttu-id="dda49-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda49-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda49-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda49-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda49-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dda49-149">INPUTS</span></span>

### <span data-ttu-id="dda49-150">System. String</span><span class="sxs-lookup"><span data-stu-id="dda49-150">System.String</span></span>
<span data-ttu-id="dda49-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dda49-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dda49-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dda49-152">OUTPUTS</span></span>

### <span data-ttu-id="dda49-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="dda49-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dda49-154">Note</span><span class="sxs-lookup"><span data-stu-id="dda49-154">NOTES</span></span>

## <span data-ttu-id="dda49-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dda49-155">RELATED LINKS</span></span>