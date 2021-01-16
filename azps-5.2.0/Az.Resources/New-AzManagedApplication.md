---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349108"
---
# <span data-ttu-id="55cf2-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="55cf2-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="55cf2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="55cf2-103">Crea un'applicazione gestita in Azure.</span><span class="sxs-lookup"><span data-stu-id="55cf2-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="55cf2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55cf2-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55cf2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="55cf2-106">Il cmdlet **New-AzManagedApplication** crea un'applicazione gestita in Azure.</span><span class="sxs-lookup"><span data-stu-id="55cf2-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="55cf2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55cf2-107">EXAMPLES</span></span>

### <span data-ttu-id="55cf2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="55cf2-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="55cf2-109">Questo comando crea un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="55cf2-109">This command creates a managed application</span></span>

## <span data-ttu-id="55cf2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55cf2-110">PARAMETERS</span></span>

### <span data-ttu-id="55cf2-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="55cf2-111">-ApiVersion</span></span>
<span data-ttu-id="55cf2-112">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="55cf2-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="55cf2-113">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="55cf2-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="55cf2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55cf2-114">-DefaultProfile</span></span>
<span data-ttu-id="55cf2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55cf2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55cf2-116">-Tipo</span><span class="sxs-lookup"><span data-stu-id="55cf2-116">-Kind</span></span>
<span data-ttu-id="55cf2-117">Tipo di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="55cf2-117">The managed application kind.</span></span>
<span data-ttu-id="55cf2-118">Uno di Marketplace o servicecatalog</span><span class="sxs-lookup"><span data-stu-id="55cf2-118">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="55cf2-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="55cf2-119">-Location</span></span>
<span data-ttu-id="55cf2-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="55cf2-120">The resource location.</span></span>

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

### <span data-ttu-id="55cf2-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="55cf2-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="55cf2-122">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="55cf2-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="55cf2-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55cf2-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="55cf2-124">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="55cf2-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="55cf2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="55cf2-125">-Name</span></span>
<span data-ttu-id="55cf2-126">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="55cf2-126">The managed application name.</span></span>

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

### <span data-ttu-id="55cf2-127">Parametro-</span><span class="sxs-lookup"><span data-stu-id="55cf2-127">-Parameter</span></span>
<span data-ttu-id="55cf2-128">Stringa formattata JSON di parametri per l'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="55cf2-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="55cf2-129">Può trattarsi di un percorso di un nome file o di un URI che contiene i parametri oppure i parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="55cf2-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="55cf2-130">-Piano</span><span class="sxs-lookup"><span data-stu-id="55cf2-130">-Plan</span></span>
<span data-ttu-id="55cf2-131">Tabella hash che rappresenta le proprietà del piano applicazione gestite.</span><span class="sxs-lookup"><span data-stu-id="55cf2-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="55cf2-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="55cf2-132">-Pre</span></span>
<span data-ttu-id="55cf2-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="55cf2-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="55cf2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55cf2-134">-ResourceGroupName</span></span>
<span data-ttu-id="55cf2-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55cf2-135">The resource group name.</span></span>

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

### <span data-ttu-id="55cf2-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="55cf2-136">-Tag</span></span>
<span data-ttu-id="55cf2-137">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="55cf2-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="55cf2-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="55cf2-138">-Confirm</span></span>
<span data-ttu-id="55cf2-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55cf2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55cf2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55cf2-140">-WhatIf</span></span>
<span data-ttu-id="55cf2-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55cf2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55cf2-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55cf2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55cf2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55cf2-143">CommonParameters</span></span>
<span data-ttu-id="55cf2-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55cf2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55cf2-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55cf2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55cf2-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55cf2-146">INPUTS</span></span>

### <span data-ttu-id="55cf2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="55cf2-147">System.String</span></span>

### <span data-ttu-id="55cf2-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="55cf2-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="55cf2-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55cf2-149">OUTPUTS</span></span>

### <span data-ttu-id="55cf2-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="55cf2-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="55cf2-151">Note</span><span class="sxs-lookup"><span data-stu-id="55cf2-151">NOTES</span></span>

## <span data-ttu-id="55cf2-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55cf2-152">RELATED LINKS</span></span>
