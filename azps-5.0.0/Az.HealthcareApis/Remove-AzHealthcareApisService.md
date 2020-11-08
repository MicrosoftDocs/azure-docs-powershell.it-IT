---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 12db158089473c5f0cfb01e24b762ecf192f8991
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200839"
---
# <span data-ttu-id="21542-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="21542-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="21542-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21542-102">SYNOPSIS</span></span>
<span data-ttu-id="21542-103">Elimina un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="21542-103">Deletes a service instance.</span></span>

## <span data-ttu-id="21542-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21542-104">SYNTAX</span></span>

### <span data-ttu-id="21542-105">ServiceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="21542-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21542-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21542-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21542-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21542-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21542-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21542-108">DESCRIPTION</span></span>
<span data-ttu-id="21542-109">Elimina un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="21542-109">Deletes a service instance.</span></span>

## <span data-ttu-id="21542-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21542-110">EXAMPLES</span></span>

### <span data-ttu-id="21542-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="21542-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="21542-112">Elimina il servizio HealthcareApis esistente con il nome specificato all'interno di un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="21542-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="21542-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="21542-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="21542-114">Elimina il servizio HealthcareApis esistente con il ResourceId fornito.</span><span class="sxs-lookup"><span data-stu-id="21542-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="21542-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="21542-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="21542-116">Elimina l'oggetto servizio HealthcareApis fornito.</span><span class="sxs-lookup"><span data-stu-id="21542-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="21542-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21542-117">PARAMETERS</span></span>

### <span data-ttu-id="21542-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21542-118">-AsJob</span></span>
<span data-ttu-id="21542-119">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="21542-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="21542-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21542-120">-DefaultProfile</span></span>
<span data-ttu-id="21542-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21542-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21542-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21542-122">-InputObject</span></span>
<span data-ttu-id="21542-123">Oggetto servizio HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="21542-123">HealthcareApis service object</span></span>

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

### <span data-ttu-id="21542-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="21542-124">-Name</span></span>
<span data-ttu-id="21542-125">Nome servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="21542-125">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="21542-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21542-126">-PassThru</span></span>
<span data-ttu-id="21542-127">Se specificato, restituisce vero se l'operazione è stata eseguita correttamente</span><span class="sxs-lookup"><span data-stu-id="21542-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="21542-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21542-128">-ResourceGroupName</span></span>
<span data-ttu-id="21542-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21542-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="21542-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21542-130">-ResourceId</span></span>
<span data-ttu-id="21542-131">HealthcareApis servizio ResourceId.</span><span class="sxs-lookup"><span data-stu-id="21542-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="21542-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21542-132">-Confirm</span></span>
<span data-ttu-id="21542-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21542-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21542-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21542-134">-WhatIf</span></span>
<span data-ttu-id="21542-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21542-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21542-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21542-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21542-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21542-137">CommonParameters</span></span>
<span data-ttu-id="21542-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21542-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21542-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21542-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21542-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21542-140">INPUTS</span></span>

### <span data-ttu-id="21542-141">System. String</span><span class="sxs-lookup"><span data-stu-id="21542-141">System.String</span></span>

### <span data-ttu-id="21542-142">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="21542-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="21542-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21542-143">OUTPUTS</span></span>

### <span data-ttu-id="21542-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21542-144">System.Boolean</span></span>

## <span data-ttu-id="21542-145">Note</span><span class="sxs-lookup"><span data-stu-id="21542-145">NOTES</span></span>

## <span data-ttu-id="21542-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21542-146">RELATED LINKS</span></span>
