---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330859"
---
# <span data-ttu-id="0fda0-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fda0-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="0fda0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fda0-102">SYNOPSIS</span></span>
<span data-ttu-id="0fda0-103">Creare o aggiornare un record di configurazione</span><span class="sxs-lookup"><span data-stu-id="0fda0-103">Create or Update configuration record</span></span>

## <span data-ttu-id="0fda0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fda0-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fda0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fda0-105">DESCRIPTION</span></span>
<span data-ttu-id="0fda0-106">Creare o aggiornare un record di configurazione</span><span class="sxs-lookup"><span data-stu-id="0fda0-106">Create or Update configuration record</span></span>

## <span data-ttu-id="0fda0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fda0-107">EXAMPLES</span></span>

### <span data-ttu-id="0fda0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0fda0-108">Example 1</span></span>
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

<span data-ttu-id="0fda0-109">Creare una configurazione di manutenzione con l'host dell'ambito</span><span class="sxs-lookup"><span data-stu-id="0fda0-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="0fda0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fda0-110">PARAMETERS</span></span>

### <span data-ttu-id="0fda0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fda0-111">-AsJob</span></span>
<span data-ttu-id="0fda0-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0fda0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fda0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fda0-113">-DefaultProfile</span></span>
<span data-ttu-id="0fda0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0fda0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fda0-115">-Durata</span><span class="sxs-lookup"><span data-stu-id="0fda0-115">-Duration</span></span>
<span data-ttu-id="0fda0-116">La durata</span><span class="sxs-lookup"><span data-stu-id="0fda0-116">The duration</span></span>


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

### <span data-ttu-id="0fda0-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="0fda0-117">-ExpirationDateTime</span></span>
<span data-ttu-id="0fda0-118">ExpirationDateTime della programmazione in formato AAAA-MM-DD HH: mm</span><span class="sxs-lookup"><span data-stu-id="0fda0-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="0fda0-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="0fda0-119">-ExtensionProperty</span></span>
<span data-ttu-id="0fda0-120">Proprietà dell'estensione per risorsa.</span><span class="sxs-lookup"><span data-stu-id="0fda0-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="0fda0-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0fda0-121">-Location</span></span>
<span data-ttu-id="0fda0-122">Posizione di configurazione della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="0fda0-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="0fda0-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="0fda0-123">-MaintenanceScope</span></span>
<span data-ttu-id="0fda0-124">Ambito di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="0fda0-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="0fda0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fda0-125">-Name</span></span>
<span data-ttu-id="0fda0-126">Nome della configurazione della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="0fda0-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="0fda0-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="0fda0-127">-RecurEvery</span></span>
<span data-ttu-id="0fda0-128">Ricorrenza della pianificazione</span><span class="sxs-lookup"><span data-stu-id="0fda0-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="0fda0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fda0-129">-ResourceGroupName</span></span>
<span data-ttu-id="0fda0-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fda0-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="0fda0-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="0fda0-131">-StartDateTime</span></span>
<span data-ttu-id="0fda0-132">StartDateTime della programmazione in formato AAAA-MM-DD HH: mm</span><span class="sxs-lookup"><span data-stu-id="0fda0-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="0fda0-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="0fda0-133">-Tag</span></span>
<span data-ttu-id="0fda0-134">Tag ARM.</span><span class="sxs-lookup"><span data-stu-id="0fda0-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="0fda0-135">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="0fda0-135">-Timezone</span></span>
<span data-ttu-id="0fda0-136">Il fuso orario</span><span class="sxs-lookup"><span data-stu-id="0fda0-136">The timezone</span></span>

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

### <span data-ttu-id="0fda0-137">-Visibilità</span><span class="sxs-lookup"><span data-stu-id="0fda0-137">-Visibility</span></span>
<span data-ttu-id="0fda0-138">Visibilità dell'ambito</span><span class="sxs-lookup"><span data-stu-id="0fda0-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="0fda0-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0fda0-139">-Confirm</span></span>
<span data-ttu-id="0fda0-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fda0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fda0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fda0-141">-WhatIf</span></span>
<span data-ttu-id="0fda0-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fda0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fda0-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fda0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fda0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fda0-144">CommonParameters</span></span>
<span data-ttu-id="0fda0-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fda0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fda0-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fda0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fda0-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fda0-147">INPUTS</span></span>

### <span data-ttu-id="0fda0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0fda0-148">System.String</span></span>

## <span data-ttu-id="0fda0-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fda0-149">OUTPUTS</span></span>

### <span data-ttu-id="0fda0-150">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fda0-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="0fda0-151">Note</span><span class="sxs-lookup"><span data-stu-id="0fda0-151">NOTES</span></span>

## <span data-ttu-id="0fda0-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fda0-152">RELATED LINKS</span></span>
