---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190279"
---
# <span data-ttu-id="b6fd0-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6fd0-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="b6fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fd0-103">Creare o aggiornare il record di configurazione</span><span class="sxs-lookup"><span data-stu-id="b6fd0-103">Create or Update configuration record</span></span>

## <span data-ttu-id="b6fd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6fd0-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6fd0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="b6fd0-106">Creare o aggiornare il record di configurazione</span><span class="sxs-lookup"><span data-stu-id="b6fd0-106">Create or Update configuration record</span></span>

## <span data-ttu-id="b6fd0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6fd0-107">EXAMPLES</span></span>

### <span data-ttu-id="b6fd0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6fd0-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="b6fd0-109">Creare una configurazione di manutenzione con ambito Host</span><span class="sxs-lookup"><span data-stu-id="b6fd0-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="b6fd0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6fd0-110">PARAMETERS</span></span>

### <span data-ttu-id="b6fd0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6fd0-111">-AsJob</span></span>
<span data-ttu-id="b6fd0-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b6fd0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6fd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6fd0-113">-DefaultProfile</span></span>
<span data-ttu-id="b6fd0-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6fd0-115">-Durata</span><span class="sxs-lookup"><span data-stu-id="b6fd0-115">-Duration</span></span>
<span data-ttu-id="b6fd0-116">Durata</span><span class="sxs-lookup"><span data-stu-id="b6fd0-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6fd0-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="b6fd0-117">-ExpirationDateTime</span></span>
<span data-ttu-id="b6fd0-118">ExpirationDateTime della pianificazione nel formato AAAA-MM-GG hh:mm</span><span class="sxs-lookup"><span data-stu-id="b6fd0-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="b6fd0-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="b6fd0-119">-ExtensionProperty</span></span>
<span data-ttu-id="b6fd0-120">Proprietà dell'estensione per risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-120">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6fd0-121">-Location</span><span class="sxs-lookup"><span data-stu-id="b6fd0-121">-Location</span></span>
<span data-ttu-id="b6fd0-122">Posizione della configurazione di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="b6fd0-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="b6fd0-123">-MaintenanceScope</span></span>
<span data-ttu-id="b6fd0-124">Ambito di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="b6fd0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b6fd0-125">-Name</span></span>
<span data-ttu-id="b6fd0-126">Nome della configurazione di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="b6fd0-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="b6fd0-127">-RecurEvery</span></span>
<span data-ttu-id="b6fd0-128">Ricorrenza della programmazione</span><span class="sxs-lookup"><span data-stu-id="b6fd0-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="b6fd0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6fd0-129">-ResourceGroupName</span></span>
<span data-ttu-id="b6fd0-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="b6fd0-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="b6fd0-131">-StartDateTime</span></span>
<span data-ttu-id="b6fd0-132">Valore StartDateTime della pianificazione nel formato AAAA-MM-GG hh:mm</span><span class="sxs-lookup"><span data-stu-id="b6fd0-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="b6fd0-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6fd0-133">-Tag</span></span>
<span data-ttu-id="b6fd0-134">Tag ARM testo.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-134">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6fd0-135">-Fuso orario</span><span class="sxs-lookup"><span data-stu-id="b6fd0-135">-Timezone</span></span>
<span data-ttu-id="b6fd0-136">Il fuso orario</span><span class="sxs-lookup"><span data-stu-id="b6fd0-136">The timezone</span></span>

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

### <span data-ttu-id="b6fd0-137">-Visibility</span><span class="sxs-lookup"><span data-stu-id="b6fd0-137">-Visibility</span></span>
<span data-ttu-id="b6fd0-138">Visibilità dell'ambito</span><span class="sxs-lookup"><span data-stu-id="b6fd0-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="b6fd0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6fd0-139">-Confirm</span></span>
<span data-ttu-id="b6fd0-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6fd0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6fd0-141">-WhatIf</span></span>
<span data-ttu-id="b6fd0-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6fd0-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6fd0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fd0-144">CommonParameters</span></span>
<span data-ttu-id="b6fd0-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fd0-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6fd0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fd0-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6fd0-147">INPUTS</span></span>

### <span data-ttu-id="b6fd0-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b6fd0-148">System.String</span></span>

## <span data-ttu-id="b6fd0-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6fd0-149">OUTPUTS</span></span>

### <span data-ttu-id="b6fd0-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6fd0-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="b6fd0-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6fd0-151">NOTES</span></span>

## <span data-ttu-id="b6fd0-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6fd0-152">RELATED LINKS</span></span>
