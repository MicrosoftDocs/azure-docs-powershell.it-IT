---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: 1a556a92d59830a4be331c8415fde0c85ddba539
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675721"
---
# <span data-ttu-id="7efc4-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7efc4-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="7efc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7efc4-102">SYNOPSIS</span></span>
<span data-ttu-id="7efc4-103">Rimuove le configurazioni DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="7efc4-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="7efc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7efc4-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7efc4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7efc4-105">DESCRIPTION</span></span>
<span data-ttu-id="7efc4-106">Il cmdlet **Remove-AzAutomationDscConfiguration** rimuove le configurazioni DSC (APS desired state Configuration) di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7efc4-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="7efc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7efc4-107">EXAMPLES</span></span>

## <span data-ttu-id="7efc4-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7efc4-108">PARAMETERS</span></span>

### <span data-ttu-id="7efc4-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7efc4-109">-AutomationAccountName</span></span>
<span data-ttu-id="7efc4-110">Specifica il nome dell'account di automazione che contiene le configurazioni DSC rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7efc4-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7efc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efc4-111">-DefaultProfile</span></span>
<span data-ttu-id="7efc4-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7efc4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7efc4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7efc4-113">-Force</span></span>
<span data-ttu-id="7efc4-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="7efc4-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efc4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7efc4-115">-Name</span></span>
<span data-ttu-id="7efc4-116">Specifica il nome della configurazione DSC rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7efc4-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7efc4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7efc4-117">-ResourceGroupName</span></span>
<span data-ttu-id="7efc4-118">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene le configurazioni DSC.</span><span class="sxs-lookup"><span data-stu-id="7efc4-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="7efc4-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7efc4-119">-Confirm</span></span>
<span data-ttu-id="7efc4-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7efc4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efc4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7efc4-121">-WhatIf</span></span>
<span data-ttu-id="7efc4-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7efc4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7efc4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7efc4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efc4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efc4-124">CommonParameters</span></span>
<span data-ttu-id="7efc4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7efc4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efc4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7efc4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efc4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7efc4-127">INPUTS</span></span>

### <span data-ttu-id="7efc4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7efc4-128">System.String</span></span>

## <span data-ttu-id="7efc4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7efc4-129">OUTPUTS</span></span>

### <span data-ttu-id="7efc4-130">System. void</span><span class="sxs-lookup"><span data-stu-id="7efc4-130">System.Void</span></span>

## <span data-ttu-id="7efc4-131">Note</span><span class="sxs-lookup"><span data-stu-id="7efc4-131">NOTES</span></span>

## <span data-ttu-id="7efc4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7efc4-132">RELATED LINKS</span></span>

[<span data-ttu-id="7efc4-133">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7efc4-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="7efc4-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7efc4-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="7efc4-135">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7efc4-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


