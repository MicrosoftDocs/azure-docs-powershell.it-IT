---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192263"
---
# <span data-ttu-id="de833-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="de833-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="de833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de833-102">SYNOPSIS</span></span>
<span data-ttu-id="de833-103">Record di configurazione delle patch</span><span class="sxs-lookup"><span data-stu-id="de833-103">Patch configuration record</span></span>

## <span data-ttu-id="de833-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de833-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de833-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de833-105">DESCRIPTION</span></span>
<span data-ttu-id="de833-106">Record di configurazione della manutenzione delle patch</span><span class="sxs-lookup"><span data-stu-id="de833-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="de833-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de833-107">EXAMPLES</span></span>

### <span data-ttu-id="de833-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de833-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="de833-109">Record di configurazione della manutenzione delle patch</span><span class="sxs-lookup"><span data-stu-id="de833-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="de833-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de833-110">PARAMETERS</span></span>

### <span data-ttu-id="de833-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de833-111">-AsJob</span></span>
<span data-ttu-id="de833-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="de833-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de833-113">-Configuration</span><span class="sxs-lookup"><span data-stu-id="de833-113">-Configuration</span></span>
<span data-ttu-id="de833-114">Configurazione di manutenzione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="de833-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de833-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de833-115">-DefaultProfile</span></span>
<span data-ttu-id="de833-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de833-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de833-117">-Name</span><span class="sxs-lookup"><span data-stu-id="de833-117">-Name</span></span>
<span data-ttu-id="de833-118">Nome della configurazione di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="de833-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="de833-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de833-119">-ResourceGroupName</span></span>
<span data-ttu-id="de833-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de833-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="de833-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de833-121">-Confirm</span></span>
<span data-ttu-id="de833-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de833-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de833-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de833-123">-WhatIf</span></span>
<span data-ttu-id="de833-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de833-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de833-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de833-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de833-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de833-126">CommonParameters</span></span>
<span data-ttu-id="de833-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de833-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de833-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de833-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de833-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="de833-129">INPUTS</span></span>

### <span data-ttu-id="de833-130">System.String</span><span class="sxs-lookup"><span data-stu-id="de833-130">System.String</span></span>

### <span data-ttu-id="de833-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="de833-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="de833-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de833-132">OUTPUTS</span></span>

### <span data-ttu-id="de833-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="de833-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="de833-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="de833-134">NOTES</span></span>

## <span data-ttu-id="de833-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de833-135">RELATED LINKS</span></span>
