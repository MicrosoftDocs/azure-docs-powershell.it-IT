---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180334"
---
# <span data-ttu-id="189f3-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="189f3-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="189f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="189f3-102">SYNOPSIS</span></span>
<span data-ttu-id="189f3-103">Registra configurazione per risorsa.</span><span class="sxs-lookup"><span data-stu-id="189f3-103">Register configuration for resource.</span></span>

## <span data-ttu-id="189f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="189f3-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="189f3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="189f3-105">DESCRIPTION</span></span>
<span data-ttu-id="189f3-106">Registrare la configurazione di manutenzione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="189f3-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="189f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="189f3-107">EXAMPLES</span></span>

### <span data-ttu-id="189f3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="189f3-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="189f3-109">Registrare la configurazione di manutenzione per un host dedicato.</span><span class="sxs-lookup"><span data-stu-id="189f3-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="189f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="189f3-110">PARAMETERS</span></span>

### <span data-ttu-id="189f3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="189f3-111">-AsJob</span></span>
<span data-ttu-id="189f3-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="189f3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="189f3-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="189f3-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="189f3-114">Il nome dell'assegnazione di configurazione deve corrispondere a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="189f3-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="189f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189f3-115">-DefaultProfile</span></span>
<span data-ttu-id="189f3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="189f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="189f3-117">-Location</span><span class="sxs-lookup"><span data-stu-id="189f3-117">-Location</span></span>
<span data-ttu-id="189f3-118">Posizione senza spazi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="189f3-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="189f3-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="189f3-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="189f3-120">MaintenanceConfiguration completa.</span><span class="sxs-lookup"><span data-stu-id="189f3-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="189f3-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="189f3-121">-ProviderName</span></span>
<span data-ttu-id="189f3-122">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="189f3-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="189f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="189f3-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="189f3-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="189f3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="189f3-125">-ResourceId</span></span>
<span data-ttu-id="189f3-126">Il nome dell'assegnazione di configurazione deve corrispondere a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="189f3-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="189f3-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="189f3-127">-ResourceName</span></span>
<span data-ttu-id="189f3-128">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="189f3-128">The resource name.</span></span>

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

### <span data-ttu-id="189f3-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="189f3-129">-ResourceParentName</span></span>
<span data-ttu-id="189f3-130">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="189f3-130">The parent resource name.</span></span>

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

### <span data-ttu-id="189f3-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="189f3-131">-ResourceParentType</span></span>
<span data-ttu-id="189f3-132">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="189f3-132">The parent resource type.</span></span>

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

### <span data-ttu-id="189f3-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="189f3-133">-ResourceType</span></span>
<span data-ttu-id="189f3-134">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="189f3-134">The resource type.</span></span>

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

### <span data-ttu-id="189f3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="189f3-135">-Confirm</span></span>
<span data-ttu-id="189f3-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="189f3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="189f3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="189f3-137">-WhatIf</span></span>
<span data-ttu-id="189f3-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="189f3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="189f3-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="189f3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="189f3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189f3-140">CommonParameters</span></span>
<span data-ttu-id="189f3-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="189f3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189f3-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="189f3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189f3-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="189f3-143">INPUTS</span></span>

### <span data-ttu-id="189f3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="189f3-144">System.String</span></span>

## <span data-ttu-id="189f3-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="189f3-145">OUTPUTS</span></span>

### <span data-ttu-id="189f3-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="189f3-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="189f3-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="189f3-147">NOTES</span></span>

## <span data-ttu-id="189f3-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="189f3-148">RELATED LINKS</span></span>
