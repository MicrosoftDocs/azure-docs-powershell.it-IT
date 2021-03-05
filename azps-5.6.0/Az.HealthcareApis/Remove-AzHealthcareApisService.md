---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 448b400d4a01924d7ef2ce64acc0f7edf827b827
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013166"
---
# <span data-ttu-id="fd7e0-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="fd7e0-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="fd7e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7e0-103">Elimina un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-103">Deletes a service instance.</span></span>

## <span data-ttu-id="fd7e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd7e0-104">SYNTAX</span></span>

### <span data-ttu-id="fd7e0-105">ServiceNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd7e0-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7e0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd7e0-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7e0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd7e0-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd7e0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fd7e0-108">DESCRIPTION</span></span>
<span data-ttu-id="fd7e0-109">Elimina un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-109">Deletes a service instance.</span></span>

## <span data-ttu-id="fd7e0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd7e0-110">EXAMPLES</span></span>

### <span data-ttu-id="fd7e0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd7e0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="fd7e0-112">Elimina il servizio HealthcareApis esistente con il nome specificato all'interno di un gruppo di risorse fornito.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="fd7e0-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fd7e0-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="fd7e0-114">Elimina il servizio HealthcareApis esistente con il valore ResourceId fornito.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="fd7e0-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="fd7e0-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="fd7e0-116">Elimina l'oggetto servizio HealthcareApis fornito.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="fd7e0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd7e0-117">PARAMETERS</span></span>

### <span data-ttu-id="fd7e0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd7e0-118">-AsJob</span></span>
<span data-ttu-id="fd7e0-119">Eseguire il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="fd7e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7e0-120">-DefaultProfile</span></span>
<span data-ttu-id="fd7e0-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd7e0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd7e0-122">-InputObject</span></span>
<span data-ttu-id="fd7e0-123">Oggetto servizio HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="fd7e0-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd7e0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fd7e0-124">-Name</span></span>
<span data-ttu-id="fd7e0-125">Nome del servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd7e0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd7e0-126">-PassThru</span></span>
<span data-ttu-id="fd7e0-127">Se specificato, restituisce true se l'operazione è riuscita</span><span class="sxs-lookup"><span data-stu-id="fd7e0-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="fd7e0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7e0-128">-ResourceGroupName</span></span>
<span data-ttu-id="fd7e0-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd7e0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd7e0-130">-ResourceId</span></span>
<span data-ttu-id="fd7e0-131">HealthcareApis Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd7e0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd7e0-132">-Confirm</span></span>
<span data-ttu-id="fd7e0-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7e0-134">-WhatIf</span></span>
<span data-ttu-id="fd7e0-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd7e0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd7e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7e0-137">CommonParameters</span></span>
<span data-ttu-id="fd7e0-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7e0-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd7e0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7e0-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="fd7e0-140">INPUTS</span></span>

### <span data-ttu-id="fd7e0-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="fd7e0-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="fd7e0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fd7e0-142">System.String</span></span>

## <span data-ttu-id="fd7e0-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd7e0-143">OUTPUTS</span></span>

### <span data-ttu-id="fd7e0-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd7e0-144">System.Boolean</span></span>

## <span data-ttu-id="fd7e0-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="fd7e0-145">NOTES</span></span>

## <span data-ttu-id="fd7e0-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd7e0-146">RELATED LINKS</span></span>
