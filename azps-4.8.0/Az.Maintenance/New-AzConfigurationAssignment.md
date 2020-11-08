---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189606"
---
# <span data-ttu-id="38a02-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="38a02-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="38a02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38a02-102">SYNOPSIS</span></span>
<span data-ttu-id="38a02-103">Configurazione della registrazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="38a02-103">Register configuration for resource.</span></span>

## <span data-ttu-id="38a02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38a02-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38a02-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38a02-105">DESCRIPTION</span></span>
<span data-ttu-id="38a02-106">Registrare la configurazione della manutenzione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="38a02-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="38a02-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38a02-107">EXAMPLES</span></span>

### <span data-ttu-id="38a02-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38a02-108">Example 1</span></span>
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

<span data-ttu-id="38a02-109">Configurazione della manutenzione della registrazione per host dedicato.</span><span class="sxs-lookup"><span data-stu-id="38a02-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="38a02-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38a02-110">PARAMETERS</span></span>

### <span data-ttu-id="38a02-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38a02-111">-AsJob</span></span>
<span data-ttu-id="38a02-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="38a02-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38a02-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="38a02-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="38a02-114">Il nome dell'assegnazione di configurazione deve corrispondere a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="38a02-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="38a02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a02-115">-DefaultProfile</span></span>
<span data-ttu-id="38a02-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38a02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38a02-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="38a02-117">-Location</span></span>
<span data-ttu-id="38a02-118">Posizione senza spazi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="38a02-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="38a02-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="38a02-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="38a02-120">MaintenanceConfiguration completo.</span><span class="sxs-lookup"><span data-stu-id="38a02-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="38a02-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="38a02-121">-ProviderName</span></span>
<span data-ttu-id="38a02-122">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="38a02-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="38a02-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a02-123">-ResourceGroupName</span></span>
<span data-ttu-id="38a02-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38a02-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="38a02-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38a02-125">-ResourceId</span></span>
<span data-ttu-id="38a02-126">Il nome dell'assegnazione di configurazione deve corrispondere a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="38a02-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="38a02-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="38a02-127">-ResourceName</span></span>
<span data-ttu-id="38a02-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="38a02-128">The resource name.</span></span>

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

### <span data-ttu-id="38a02-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="38a02-129">-ResourceParentName</span></span>
<span data-ttu-id="38a02-130">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="38a02-130">The parent resource name.</span></span>

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

### <span data-ttu-id="38a02-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="38a02-131">-ResourceParentType</span></span>
<span data-ttu-id="38a02-132">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="38a02-132">The parent resource type.</span></span>

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

### <span data-ttu-id="38a02-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="38a02-133">-ResourceType</span></span>
<span data-ttu-id="38a02-134">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="38a02-134">The resource type.</span></span>

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

### <span data-ttu-id="38a02-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38a02-135">-Confirm</span></span>
<span data-ttu-id="38a02-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a02-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38a02-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a02-137">-WhatIf</span></span>
<span data-ttu-id="38a02-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38a02-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38a02-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38a02-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38a02-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a02-140">CommonParameters</span></span>
<span data-ttu-id="38a02-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a02-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a02-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38a02-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a02-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38a02-143">INPUTS</span></span>

### <span data-ttu-id="38a02-144">System. String</span><span class="sxs-lookup"><span data-stu-id="38a02-144">System.String</span></span>

## <span data-ttu-id="38a02-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38a02-145">OUTPUTS</span></span>

### <span data-ttu-id="38a02-146">Microsoft. Azure. Commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="38a02-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="38a02-147">Note</span><span class="sxs-lookup"><span data-stu-id="38a02-147">NOTES</span></span>

## <span data-ttu-id="38a02-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38a02-148">RELATED LINKS</span></span>