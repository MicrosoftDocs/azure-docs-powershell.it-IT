---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022178"
---
# <span data-ttu-id="9524a-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9524a-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="9524a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9524a-102">SYNOPSIS</span></span>
<span data-ttu-id="9524a-103">Creare o aggiornare un record di configurazione</span><span class="sxs-lookup"><span data-stu-id="9524a-103">Create or Update configuration record</span></span>

## <span data-ttu-id="9524a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9524a-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9524a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9524a-105">DESCRIPTION</span></span>
<span data-ttu-id="9524a-106">Creare o aggiornare un record di configurazione</span><span class="sxs-lookup"><span data-stu-id="9524a-106">Create or Update configuration record</span></span>

## <span data-ttu-id="9524a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9524a-107">EXAMPLES</span></span>

### <span data-ttu-id="9524a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9524a-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="9524a-109">Creare una configurazione di manutenzione con l'host dell'ambito</span><span class="sxs-lookup"><span data-stu-id="9524a-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="9524a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9524a-110">PARAMETERS</span></span>

### <span data-ttu-id="9524a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9524a-111">-AsJob</span></span>
<span data-ttu-id="9524a-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9524a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9524a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9524a-113">-DefaultProfile</span></span>
<span data-ttu-id="9524a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9524a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9524a-115">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="9524a-115">-ExtensionProperty</span></span>
<span data-ttu-id="9524a-116">Proprietà dell'estensione per risorsa.</span><span class="sxs-lookup"><span data-stu-id="9524a-116">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="9524a-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9524a-117">-Location</span></span>
<span data-ttu-id="9524a-118">Posizione di configurazione della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="9524a-118">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="9524a-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="9524a-119">-MaintenanceScope</span></span>
<span data-ttu-id="9524a-120">Ambito di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="9524a-120">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="9524a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9524a-121">-Name</span></span>
<span data-ttu-id="9524a-122">Nome della configurazione della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="9524a-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="9524a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9524a-123">-ResourceGroupName</span></span>
<span data-ttu-id="9524a-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9524a-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="9524a-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="9524a-125">-Tag</span></span>
<span data-ttu-id="9524a-126">Tag ARM.</span><span class="sxs-lookup"><span data-stu-id="9524a-126">The ARM Tags.</span></span>

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

### <span data-ttu-id="9524a-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9524a-127">-Confirm</span></span>
<span data-ttu-id="9524a-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9524a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9524a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9524a-129">-WhatIf</span></span>
<span data-ttu-id="9524a-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9524a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9524a-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9524a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9524a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9524a-132">CommonParameters</span></span>
<span data-ttu-id="9524a-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9524a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9524a-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9524a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9524a-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9524a-135">INPUTS</span></span>

### <span data-ttu-id="9524a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9524a-136">System.String</span></span>

## <span data-ttu-id="9524a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9524a-137">OUTPUTS</span></span>

### <span data-ttu-id="9524a-138">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9524a-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="9524a-139">Note</span><span class="sxs-lookup"><span data-stu-id="9524a-139">NOTES</span></span>

## <span data-ttu-id="9524a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9524a-140">RELATED LINKS</span></span>
