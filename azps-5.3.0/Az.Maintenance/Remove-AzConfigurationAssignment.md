---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475593"
---
# <span data-ttu-id="13274-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="13274-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="13274-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13274-102">SYNOPSIS</span></span>
<span data-ttu-id="13274-103">Annullare la registrazione della configurazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="13274-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="13274-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13274-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13274-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13274-105">DESCRIPTION</span></span>
<span data-ttu-id="13274-106">Annullare la registrazione della configurazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="13274-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="13274-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13274-107">EXAMPLES</span></span>

### <span data-ttu-id="13274-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13274-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="13274-109">Annullare la registrazione della configurazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="13274-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="13274-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13274-110">PARAMETERS</span></span>

### <span data-ttu-id="13274-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13274-111">-AsJob</span></span>
<span data-ttu-id="13274-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="13274-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13274-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="13274-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="13274-114">Nome dell'assegnazione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="13274-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="13274-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13274-115">-DefaultProfile</span></span>
<span data-ttu-id="13274-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13274-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13274-117">-Force</span><span class="sxs-lookup"><span data-stu-id="13274-117">-Force</span></span>
<span data-ttu-id="13274-118">Forza Rimuovi senza conferma.</span><span class="sxs-lookup"><span data-stu-id="13274-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="13274-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13274-119">-PassThru</span></span>
<span data-ttu-id="13274-120">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="13274-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="13274-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="13274-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13274-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="13274-122">-ProviderName</span></span>
<span data-ttu-id="13274-123">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="13274-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13274-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13274-124">-ResourceGroupName</span></span>
<span data-ttu-id="13274-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13274-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13274-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="13274-126">-ResourceName</span></span>
<span data-ttu-id="13274-127">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="13274-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13274-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="13274-128">-ResourceParentName</span></span>
<span data-ttu-id="13274-129">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="13274-129">The parent resource name.</span></span>

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

### <span data-ttu-id="13274-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="13274-130">-ResourceParentType</span></span>
<span data-ttu-id="13274-131">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="13274-131">The parent resource type.</span></span>

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

### <span data-ttu-id="13274-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="13274-132">-ResourceType</span></span>
<span data-ttu-id="13274-133">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="13274-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13274-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="13274-134">-Confirm</span></span>
<span data-ttu-id="13274-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13274-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13274-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13274-136">-WhatIf</span></span>
<span data-ttu-id="13274-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13274-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13274-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13274-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13274-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13274-139">CommonParameters</span></span>
<span data-ttu-id="13274-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13274-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13274-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13274-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13274-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13274-142">INPUTS</span></span>

### <span data-ttu-id="13274-143">System. String</span><span class="sxs-lookup"><span data-stu-id="13274-143">System.String</span></span>

## <span data-ttu-id="13274-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13274-144">OUTPUTS</span></span>

### <span data-ttu-id="13274-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13274-145">System.Boolean</span></span>

## <span data-ttu-id="13274-146">Note</span><span class="sxs-lookup"><span data-stu-id="13274-146">NOTES</span></span>

## <span data-ttu-id="13274-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13274-147">RELATED LINKS</span></span>
