---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340828"
---
# <span data-ttu-id="6d985-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="6d985-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="6d985-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d985-102">SYNOPSIS</span></span>
<span data-ttu-id="6d985-103">Configurazione della registrazione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d985-103">Register configuration for resource.</span></span>

## <span data-ttu-id="6d985-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d985-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d985-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d985-105">DESCRIPTION</span></span>
<span data-ttu-id="6d985-106">Registrare la configurazione della manutenzione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d985-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="6d985-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d985-107">EXAMPLES</span></span>

### <span data-ttu-id="6d985-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d985-108">Example 1</span></span>
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

<span data-ttu-id="6d985-109">Configurazione della manutenzione della registrazione per host dedicato.</span><span class="sxs-lookup"><span data-stu-id="6d985-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="6d985-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d985-110">PARAMETERS</span></span>

### <span data-ttu-id="6d985-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d985-111">-AsJob</span></span>
<span data-ttu-id="6d985-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6d985-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d985-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="6d985-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="6d985-114">Il nome dell'assegnazione di configurazione deve corrispondere a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="6d985-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="6d985-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d985-115">-DefaultProfile</span></span>
<span data-ttu-id="6d985-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d985-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d985-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6d985-117">-Location</span></span>
<span data-ttu-id="6d985-118">Posizione senza spazi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d985-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="6d985-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6d985-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="6d985-120">MaintenanceConfiguration completo.</span><span class="sxs-lookup"><span data-stu-id="6d985-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="6d985-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="6d985-121">-ProviderName</span></span>
<span data-ttu-id="6d985-122">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d985-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="6d985-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d985-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d985-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d985-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="6d985-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d985-125">-ResourceId</span></span>
<span data-ttu-id="6d985-126">Il nome dell'assegnazione di configurazione deve corrispondere a MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="6d985-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="6d985-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6d985-127">-ResourceName</span></span>
<span data-ttu-id="6d985-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d985-128">The resource name.</span></span>

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

### <span data-ttu-id="6d985-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="6d985-129">-ResourceParentName</span></span>
<span data-ttu-id="6d985-130">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="6d985-130">The parent resource name.</span></span>

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

### <span data-ttu-id="6d985-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="6d985-131">-ResourceParentType</span></span>
<span data-ttu-id="6d985-132">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="6d985-132">The parent resource type.</span></span>

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

### <span data-ttu-id="6d985-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6d985-133">-ResourceType</span></span>
<span data-ttu-id="6d985-134">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d985-134">The resource type.</span></span>

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

### <span data-ttu-id="6d985-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d985-135">-Confirm</span></span>
<span data-ttu-id="6d985-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d985-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d985-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d985-137">-WhatIf</span></span>
<span data-ttu-id="6d985-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d985-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d985-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d985-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d985-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d985-140">CommonParameters</span></span>
<span data-ttu-id="6d985-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d985-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d985-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d985-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d985-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d985-143">INPUTS</span></span>

### <span data-ttu-id="6d985-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6d985-144">System.String</span></span>

## <span data-ttu-id="6d985-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d985-145">OUTPUTS</span></span>

### <span data-ttu-id="6d985-146">Microsoft. Azure. Commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="6d985-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="6d985-147">Note</span><span class="sxs-lookup"><span data-stu-id="6d985-147">NOTES</span></span>

## <span data-ttu-id="6d985-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d985-148">RELATED LINKS</span></span>
