---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 2a242f7a265efa2dd97f967101074615381d4cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512995"
---
# <span data-ttu-id="3a79a-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="3a79a-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="3a79a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a79a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a79a-103">Applicazione gestita degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="3a79a-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a79a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a79a-104">SYNTAX</span></span>

### <span data-ttu-id="3a79a-105">Set di parametri del nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="3a79a-105">The managed application name parameter set.</span></span> <span data-ttu-id="3a79a-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="3a79a-106">(Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a79a-107">Set di parametri ID applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="3a79a-107">The managed application Id parameter set.</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a79a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a79a-108">DESCRIPTION</span></span>
<span data-ttu-id="3a79a-109">Il cmdlet **set-AzureRmManagedApplication** aggiorna le applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="3a79a-109">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="3a79a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a79a-110">EXAMPLES</span></span>

### <span data-ttu-id="3a79a-111">Esempio 1: aggiornare la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="3a79a-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="3a79a-112">Questo comando Aggiorna la descrizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="3a79a-112">This command updates the managed application description</span></span>

## <span data-ttu-id="3a79a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a79a-113">PARAMETERS</span></span>

### <span data-ttu-id="3a79a-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3a79a-114">-ApiVersion</span></span>
<span data-ttu-id="3a79a-115">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="3a79a-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3a79a-116">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="3a79a-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3a79a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a79a-117">-DefaultProfile</span></span>
<span data-ttu-id="3a79a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a79a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a79a-119">-Tipo</span><span class="sxs-lookup"><span data-stu-id="3a79a-119">-Kind</span></span>
<span data-ttu-id="3a79a-120">Tipo di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="3a79a-120">The managed application kind.</span></span>
<span data-ttu-id="3a79a-121">Uno di Marketplace o servicecatalog</span><span class="sxs-lookup"><span data-stu-id="3a79a-121">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="3a79a-122">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3a79a-122">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="3a79a-123">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="3a79a-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="3a79a-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a79a-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="3a79a-125">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="3a79a-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="3a79a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a79a-126">-Name</span></span>
<span data-ttu-id="3a79a-127">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="3a79a-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a79a-128">Parametro-</span><span class="sxs-lookup"><span data-stu-id="3a79a-128">-Parameter</span></span>
<span data-ttu-id="3a79a-129">Stringa formattata JSON di parametri per l'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="3a79a-129">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="3a79a-130">Può trattarsi di un percorso di un nome file o di un URI che contiene i parametri oppure i parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="3a79a-130">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="3a79a-131">-Piano</span><span class="sxs-lookup"><span data-stu-id="3a79a-131">-Plan</span></span>
<span data-ttu-id="3a79a-132">Tabella hash che rappresenta le proprietà del piano applicazione gestite.</span><span class="sxs-lookup"><span data-stu-id="3a79a-132">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="3a79a-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="3a79a-133">-Pre</span></span>
<span data-ttu-id="3a79a-134">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="3a79a-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3a79a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a79a-135">-ResourceGroupName</span></span>
<span data-ttu-id="3a79a-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3a79a-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a79a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="3a79a-137">-Tag</span></span>
<span data-ttu-id="3a79a-138">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="3a79a-138">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="3a79a-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a79a-139">-Confirm</span></span>
<span data-ttu-id="3a79a-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a79a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a79a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a79a-141">-WhatIf</span></span>
<span data-ttu-id="3a79a-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a79a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a79a-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a79a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a79a-144">-ID</span><span class="sxs-lookup"><span data-stu-id="3a79a-144">-Id</span></span>
<span data-ttu-id="3a79a-145">ID applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3a79a-145">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="3a79a-146">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="3a79a-146">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a79a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a79a-147">CommonParameters</span></span>
<span data-ttu-id="3a79a-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a79a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a79a-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a79a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a79a-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a79a-150">INPUTS</span></span>

### <span data-ttu-id="3a79a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3a79a-151">System.String</span></span>
<span data-ttu-id="3a79a-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3a79a-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3a79a-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a79a-153">OUTPUTS</span></span>

### <span data-ttu-id="3a79a-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3a79a-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3a79a-155">Note</span><span class="sxs-lookup"><span data-stu-id="3a79a-155">NOTES</span></span>

## <span data-ttu-id="3a79a-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a79a-156">RELATED LINKS</span></span>

