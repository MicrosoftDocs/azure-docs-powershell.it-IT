---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 49b8351109289c46ce57224aa47b1675abe54841
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866826"
---
# <span data-ttu-id="fb92a-101">New-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="fb92a-101">New-AzureRmManagedApplication</span></span>

## <span data-ttu-id="fb92a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb92a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb92a-103">Crea un'applicazione gestita in Azure.</span><span class="sxs-lookup"><span data-stu-id="fb92a-103">Creates an Azure managed application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb92a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb92a-104">SYNTAX</span></span>

```
New-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb92a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb92a-105">DESCRIPTION</span></span>
<span data-ttu-id="fb92a-106">Il cmdlet **New-AzureRmManagedApplication** crea un'applicazione gestita in Azure.</span><span class="sxs-lookup"><span data-stu-id="fb92a-106">The **New-AzureRmManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="fb92a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb92a-107">EXAMPLES</span></span>

### <span data-ttu-id="fb92a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fb92a-108">Example 1</span></span>
```
PS C:\>New-AzureRmManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="fb92a-109">Questo comando crea un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="fb92a-109">This command creates a managed application</span></span>

## <span data-ttu-id="fb92a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb92a-110">PARAMETERS</span></span>

### <span data-ttu-id="fb92a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fb92a-111">-ApiVersion</span></span>
<span data-ttu-id="fb92a-112">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="fb92a-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fb92a-113">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="fb92a-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fb92a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb92a-114">-DefaultProfile</span></span>
<span data-ttu-id="fb92a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb92a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb92a-116">-Tipo</span><span class="sxs-lookup"><span data-stu-id="fb92a-116">-Kind</span></span>
<span data-ttu-id="fb92a-117">Tipo di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="fb92a-117">The managed application kind.</span></span>
<span data-ttu-id="fb92a-118">Uno di Marketplace o servicecatalog</span><span class="sxs-lookup"><span data-stu-id="fb92a-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb92a-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fb92a-119">-Location</span></span>
<span data-ttu-id="fb92a-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fb92a-120">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb92a-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fb92a-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="fb92a-122">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="fb92a-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="fb92a-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb92a-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="fb92a-124">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="fb92a-124">The managed resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb92a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb92a-125">-Name</span></span>
<span data-ttu-id="fb92a-126">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="fb92a-126">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb92a-127">Parametro-</span><span class="sxs-lookup"><span data-stu-id="fb92a-127">-Parameter</span></span>
<span data-ttu-id="fb92a-128">Stringa formattata JSON di parametri per l'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="fb92a-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="fb92a-129">Può trattarsi di un percorso di un nome file o di un URI che contiene i parametri oppure i parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="fb92a-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="fb92a-130">-Piano</span><span class="sxs-lookup"><span data-stu-id="fb92a-130">-Plan</span></span>
<span data-ttu-id="fb92a-131">Tabella hash che rappresenta le proprietà del piano applicazione gestite.</span><span class="sxs-lookup"><span data-stu-id="fb92a-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="fb92a-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="fb92a-132">-Pre</span></span>
<span data-ttu-id="fb92a-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="fb92a-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fb92a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb92a-134">-ResourceGroupName</span></span>
<span data-ttu-id="fb92a-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fb92a-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb92a-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb92a-136">-Tag</span></span>
<span data-ttu-id="fb92a-137">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fb92a-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fb92a-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb92a-138">-Confirm</span></span>
<span data-ttu-id="fb92a-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb92a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb92a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb92a-140">-WhatIf</span></span>
<span data-ttu-id="fb92a-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb92a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb92a-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb92a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb92a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb92a-143">CommonParameters</span></span>
<span data-ttu-id="fb92a-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb92a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb92a-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb92a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb92a-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb92a-146">INPUTS</span></span>

### <span data-ttu-id="fb92a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fb92a-147">System.String</span></span>
<span data-ttu-id="fb92a-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb92a-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fb92a-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb92a-149">OUTPUTS</span></span>

### <span data-ttu-id="fb92a-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fb92a-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fb92a-151">Note</span><span class="sxs-lookup"><span data-stu-id="fb92a-151">NOTES</span></span>

## <span data-ttu-id="fb92a-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb92a-152">RELATED LINKS</span></span>
