---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: f0c5c52773d5750b86ce82d696e9130df76f4700
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022180"
---
# <span data-ttu-id="6b191-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="6b191-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="6b191-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b191-102">SYNOPSIS</span></span>
<span data-ttu-id="6b191-103">Configurazione della registrazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b191-103">Register configuration for resource.</span></span>

## <span data-ttu-id="6b191-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b191-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b191-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b191-105">DESCRIPTION</span></span>
<span data-ttu-id="6b191-106">Registrare la configurazione della manutenzione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b191-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="6b191-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b191-107">EXAMPLES</span></span>

### <span data-ttu-id="6b191-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6b191-108">Example 1</span></span>
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

<span data-ttu-id="6b191-109">Configurare la configurazione di manutenzione per l'host didicated.</span><span class="sxs-lookup"><span data-stu-id="6b191-109">Register maintenance configuration for didicated host.</span></span>

## <span data-ttu-id="6b191-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b191-110">PARAMETERS</span></span>

### <span data-ttu-id="6b191-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b191-111">-AsJob</span></span>
<span data-ttu-id="6b191-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6b191-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b191-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="6b191-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="6b191-114">Il nome dell'assegnazione di configurazione deve corrispondere a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="6b191-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="6b191-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b191-115">-DefaultProfile</span></span>
<span data-ttu-id="6b191-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b191-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b191-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6b191-117">-Location</span></span>
<span data-ttu-id="6b191-118">Posizione senza spazi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b191-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="6b191-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6b191-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="6b191-120">MaintenanceConfiguration completo.</span><span class="sxs-lookup"><span data-stu-id="6b191-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="6b191-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="6b191-121">-ProviderName</span></span>
<span data-ttu-id="6b191-122">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b191-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="6b191-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b191-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b191-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b191-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="6b191-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b191-125">-ResourceId</span></span>
<span data-ttu-id="6b191-126">Il nome dell'assegnazione di configurazione deve corrispondere a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="6b191-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="6b191-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b191-127">-ResourceName</span></span>
<span data-ttu-id="6b191-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b191-128">The resource name.</span></span>

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

### <span data-ttu-id="6b191-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="6b191-129">-ResourceParentName</span></span>
<span data-ttu-id="6b191-130">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="6b191-130">The parent resource name.</span></span>

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

### <span data-ttu-id="6b191-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="6b191-131">-ResourceParentType</span></span>
<span data-ttu-id="6b191-132">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="6b191-132">The parent resource type.</span></span>

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

### <span data-ttu-id="6b191-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6b191-133">-ResourceType</span></span>
<span data-ttu-id="6b191-134">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b191-134">The resource type.</span></span>

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

### <span data-ttu-id="6b191-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b191-135">-Confirm</span></span>
<span data-ttu-id="6b191-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b191-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b191-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b191-137">-WhatIf</span></span>
<span data-ttu-id="6b191-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b191-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b191-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b191-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b191-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b191-140">CommonParameters</span></span>
<span data-ttu-id="6b191-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b191-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b191-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b191-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b191-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b191-143">INPUTS</span></span>

### <span data-ttu-id="6b191-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6b191-144">System.String</span></span>

## <span data-ttu-id="6b191-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b191-145">OUTPUTS</span></span>

### <span data-ttu-id="6b191-146">Microsoft. Azure. Commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="6b191-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="6b191-147">Note</span><span class="sxs-lookup"><span data-stu-id="6b191-147">NOTES</span></span>

## <span data-ttu-id="6b191-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b191-148">RELATED LINKS</span></span>
