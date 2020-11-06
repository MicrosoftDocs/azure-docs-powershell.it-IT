---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 60f80f92723bbb66d1bf88c9fd8efea66c8c4e55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512003"
---
# <span data-ttu-id="05027-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="05027-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="05027-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05027-102">SYNOPSIS</span></span>
<span data-ttu-id="05027-103">Rimuove i metadati dalle configurazioni dei nodi DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="05027-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05027-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05027-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05027-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05027-105">DESCRIPTION</span></span>
<span data-ttu-id="05027-106">Il cmdlet **Remove-AzureRmAutomationDscNodeConfiguration** consente di rimuovere i metadati dalle configurazioni di nodi DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="05027-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="05027-107">Automation archivia la configurazione del nodo DSC come documento di configurazione MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="05027-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="05027-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05027-108">EXAMPLES</span></span>

## <span data-ttu-id="05027-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05027-109">PARAMETERS</span></span>

### <span data-ttu-id="05027-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05027-110">-AutomationAccountName</span></span>
<span data-ttu-id="05027-111">Specifica il nome di un account di automazione che contiene le configurazioni dei nodi DSC per cui questo cmdlet rimuove i metadati.</span><span class="sxs-lookup"><span data-stu-id="05027-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="05027-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05027-112">-DefaultProfile</span></span>
<span data-ttu-id="05027-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="05027-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05027-114">-Force</span><span class="sxs-lookup"><span data-stu-id="05027-114">-Force</span></span>
<span data-ttu-id="05027-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="05027-115">ps_force</span></span>

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

### <span data-ttu-id="05027-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="05027-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="05027-117">Indica che questo cmdlet ignora i mapping dei nodi.</span><span class="sxs-lookup"><span data-stu-id="05027-117">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05027-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="05027-118">-Name</span></span>
<span data-ttu-id="05027-119">Specifica il nome della configurazione del nodo DSC per cui questo cmdlet rimuove i metadati.</span><span class="sxs-lookup"><span data-stu-id="05027-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05027-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05027-120">-ResourceGroupName</span></span>
<span data-ttu-id="05027-121">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="05027-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="05027-122">Questo cmdlet consente di rimuovere i metadati per le configurazioni dei nodi DSC nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="05027-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="05027-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="05027-123">-Confirm</span></span>
<span data-ttu-id="05027-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05027-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05027-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05027-125">-WhatIf</span></span>
<span data-ttu-id="05027-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05027-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05027-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05027-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05027-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05027-128">CommonParameters</span></span>
<span data-ttu-id="05027-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05027-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05027-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05027-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05027-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05027-131">INPUTS</span></span>

### <span data-ttu-id="05027-132">System. String</span><span class="sxs-lookup"><span data-stu-id="05027-132">System.String</span></span>

## <span data-ttu-id="05027-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05027-133">OUTPUTS</span></span>

### <span data-ttu-id="05027-134">System. void</span><span class="sxs-lookup"><span data-stu-id="05027-134">System.Void</span></span>

## <span data-ttu-id="05027-135">Note</span><span class="sxs-lookup"><span data-stu-id="05027-135">NOTES</span></span>

## <span data-ttu-id="05027-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05027-136">RELATED LINKS</span></span>

[<span data-ttu-id="05027-137">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="05027-137">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="05027-138">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="05027-138">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="05027-139">Cmdlet di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="05027-139">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


