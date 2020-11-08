---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189598"
---
# <span data-ttu-id="b2355-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2355-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="b2355-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2355-102">SYNOPSIS</span></span>
<span data-ttu-id="b2355-103">Creare o aggiornare un record di configurazione</span><span class="sxs-lookup"><span data-stu-id="b2355-103">Create or Update configuration record</span></span>

## <span data-ttu-id="b2355-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2355-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2355-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2355-105">DESCRIPTION</span></span>
<span data-ttu-id="b2355-106">Creare o aggiornare un record di configurazione</span><span class="sxs-lookup"><span data-stu-id="b2355-106">Create or Update configuration record</span></span>

## <span data-ttu-id="b2355-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2355-107">EXAMPLES</span></span>

### <span data-ttu-id="b2355-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2355-108">Example 1</span></span>
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

<span data-ttu-id="b2355-109">Creare una configurazione di manutenzione con l'host dell'ambito</span><span class="sxs-lookup"><span data-stu-id="b2355-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="b2355-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2355-110">PARAMETERS</span></span>

### <span data-ttu-id="b2355-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2355-111">-AsJob</span></span>
<span data-ttu-id="b2355-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b2355-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2355-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2355-113">-DefaultProfile</span></span>
<span data-ttu-id="b2355-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2355-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2355-115">-Durata</span><span class="sxs-lookup"><span data-stu-id="b2355-115">-Duration</span></span>
<span data-ttu-id="b2355-116">La durata</span><span class="sxs-lookup"><span data-stu-id="b2355-116">The duration</span></span>


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

### <span data-ttu-id="b2355-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="b2355-117">-ExpirationDateTime</span></span>
<span data-ttu-id="b2355-118">ExpirationDateTime della programmazione in formato AAAA-MM-DD HH: mm</span><span class="sxs-lookup"><span data-stu-id="b2355-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="b2355-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="b2355-119">-ExtensionProperty</span></span>
<span data-ttu-id="b2355-120">Proprietà dell'estensione per risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2355-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="b2355-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b2355-121">-Location</span></span>
<span data-ttu-id="b2355-122">Posizione di configurazione della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="b2355-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="b2355-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="b2355-123">-MaintenanceScope</span></span>
<span data-ttu-id="b2355-124">Ambito di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="b2355-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="b2355-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2355-125">-Name</span></span>
<span data-ttu-id="b2355-126">Nome della configurazione della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="b2355-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="b2355-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="b2355-127">-RecurEvery</span></span>
<span data-ttu-id="b2355-128">Ricorrenza della pianificazione</span><span class="sxs-lookup"><span data-stu-id="b2355-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="b2355-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2355-129">-ResourceGroupName</span></span>
<span data-ttu-id="b2355-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2355-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="b2355-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="b2355-131">-StartDateTime</span></span>
<span data-ttu-id="b2355-132">StartDateTime della programmazione in formato AAAA-MM-DD HH: mm</span><span class="sxs-lookup"><span data-stu-id="b2355-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="b2355-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2355-133">-Tag</span></span>
<span data-ttu-id="b2355-134">Tag ARM.</span><span class="sxs-lookup"><span data-stu-id="b2355-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="b2355-135">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="b2355-135">-Timezone</span></span>
<span data-ttu-id="b2355-136">Il fuso orario</span><span class="sxs-lookup"><span data-stu-id="b2355-136">The timezone</span></span>

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

### <span data-ttu-id="b2355-137">-Visibilità</span><span class="sxs-lookup"><span data-stu-id="b2355-137">-Visibility</span></span>
<span data-ttu-id="b2355-138">Visibilità dell'ambito</span><span class="sxs-lookup"><span data-stu-id="b2355-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="b2355-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2355-139">-Confirm</span></span>
<span data-ttu-id="b2355-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2355-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2355-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2355-141">-WhatIf</span></span>
<span data-ttu-id="b2355-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2355-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2355-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2355-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2355-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2355-144">CommonParameters</span></span>
<span data-ttu-id="b2355-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2355-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2355-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2355-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2355-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2355-147">INPUTS</span></span>

### <span data-ttu-id="b2355-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b2355-148">System.String</span></span>

## <span data-ttu-id="b2355-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2355-149">OUTPUTS</span></span>

### <span data-ttu-id="b2355-150">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2355-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="b2355-151">Note</span><span class="sxs-lookup"><span data-stu-id="b2355-151">NOTES</span></span>

## <span data-ttu-id="b2355-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2355-152">RELATED LINKS</span></span>
