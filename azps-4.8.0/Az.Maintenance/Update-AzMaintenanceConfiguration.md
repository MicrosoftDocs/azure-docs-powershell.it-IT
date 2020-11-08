---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189596"
---
# <span data-ttu-id="30c37-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="30c37-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="30c37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30c37-102">SYNOPSIS</span></span>
<span data-ttu-id="30c37-103">Record configurazione patch</span><span class="sxs-lookup"><span data-stu-id="30c37-103">Patch configuration record</span></span>

## <span data-ttu-id="30c37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30c37-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c37-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30c37-105">DESCRIPTION</span></span>
<span data-ttu-id="30c37-106">Record configurazione manutenzione patch</span><span class="sxs-lookup"><span data-stu-id="30c37-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="30c37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30c37-107">EXAMPLES</span></span>

### <span data-ttu-id="30c37-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30c37-108">Example 1</span></span>
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

<span data-ttu-id="30c37-109">Record configurazione manutenzione patch</span><span class="sxs-lookup"><span data-stu-id="30c37-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="30c37-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30c37-110">PARAMETERS</span></span>

### <span data-ttu-id="30c37-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30c37-111">-AsJob</span></span>
<span data-ttu-id="30c37-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="30c37-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30c37-113">-Configurazione</span><span class="sxs-lookup"><span data-stu-id="30c37-113">-Configuration</span></span>
<span data-ttu-id="30c37-114">La configurazione di manutenzione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="30c37-114">The maintenance configuration to be updated.</span></span>

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

### <span data-ttu-id="30c37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c37-115">-DefaultProfile</span></span>
<span data-ttu-id="30c37-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30c37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30c37-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="30c37-117">-Name</span></span>
<span data-ttu-id="30c37-118">Nome della configurazione della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="30c37-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="30c37-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c37-119">-ResourceGroupName</span></span>
<span data-ttu-id="30c37-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30c37-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="30c37-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30c37-121">-Confirm</span></span>
<span data-ttu-id="30c37-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30c37-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30c37-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c37-123">-WhatIf</span></span>
<span data-ttu-id="30c37-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30c37-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30c37-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30c37-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30c37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c37-126">CommonParameters</span></span>
<span data-ttu-id="30c37-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c37-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30c37-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c37-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30c37-129">INPUTS</span></span>

### <span data-ttu-id="30c37-130">System. String</span><span class="sxs-lookup"><span data-stu-id="30c37-130">System.String</span></span>

### <span data-ttu-id="30c37-131">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="30c37-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="30c37-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30c37-132">OUTPUTS</span></span>

### <span data-ttu-id="30c37-133">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="30c37-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="30c37-134">Note</span><span class="sxs-lookup"><span data-stu-id="30c37-134">NOTES</span></span>

## <span data-ttu-id="30c37-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30c37-135">RELATED LINKS</span></span>
