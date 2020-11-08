---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189601"
---
# <span data-ttu-id="9ddd2-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="9ddd2-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="9ddd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ddd2-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddd2-103">Annullare la registrazione della configurazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="9ddd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ddd2-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ddd2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ddd2-105">DESCRIPTION</span></span>
<span data-ttu-id="9ddd2-106">Annullare la registrazione della configurazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="9ddd2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ddd2-107">EXAMPLES</span></span>

### <span data-ttu-id="9ddd2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9ddd2-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="9ddd2-109">Annullare la registrazione della configurazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="9ddd2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ddd2-110">PARAMETERS</span></span>

### <span data-ttu-id="9ddd2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ddd2-111">-AsJob</span></span>
<span data-ttu-id="9ddd2-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9ddd2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ddd2-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="9ddd2-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="9ddd2-114">Nome dell'assegnazione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="9ddd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddd2-115">-DefaultProfile</span></span>
<span data-ttu-id="9ddd2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ddd2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9ddd2-117">-Force</span></span>
<span data-ttu-id="9ddd2-118">Forza Rimuovi senza conferma.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="9ddd2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ddd2-119">-PassThru</span></span>
<span data-ttu-id="9ddd2-120">Restituisce lo stato dell'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="9ddd2-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ddd2-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="9ddd2-122">-ProviderName</span></span>
<span data-ttu-id="9ddd2-123">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-123">The resource provider Name.</span></span>

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

### <span data-ttu-id="9ddd2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ddd2-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ddd2-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="9ddd2-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9ddd2-126">-ResourceName</span></span>
<span data-ttu-id="9ddd2-127">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-127">The resource name.</span></span>

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

### <span data-ttu-id="9ddd2-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="9ddd2-128">-ResourceParentName</span></span>
<span data-ttu-id="9ddd2-129">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-129">The parent resource name.</span></span>

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

### <span data-ttu-id="9ddd2-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="9ddd2-130">-ResourceParentType</span></span>
<span data-ttu-id="9ddd2-131">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-131">The parent resource type.</span></span>

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

### <span data-ttu-id="9ddd2-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9ddd2-132">-ResourceType</span></span>
<span data-ttu-id="9ddd2-133">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-133">The resource type.</span></span>

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

### <span data-ttu-id="9ddd2-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9ddd2-134">-Confirm</span></span>
<span data-ttu-id="9ddd2-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ddd2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ddd2-136">-WhatIf</span></span>
<span data-ttu-id="9ddd2-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ddd2-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ddd2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddd2-139">CommonParameters</span></span>
<span data-ttu-id="9ddd2-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ddd2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddd2-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ddd2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddd2-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ddd2-142">INPUTS</span></span>

### <span data-ttu-id="9ddd2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9ddd2-143">System.String</span></span>

## <span data-ttu-id="9ddd2-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ddd2-144">OUTPUTS</span></span>

### <span data-ttu-id="9ddd2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ddd2-145">System.Boolean</span></span>

## <span data-ttu-id="9ddd2-146">Note</span><span class="sxs-lookup"><span data-stu-id="9ddd2-146">NOTES</span></span>

## <span data-ttu-id="9ddd2-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ddd2-147">RELATED LINKS</span></span>