---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 56ceba33845061af4e0ccdf3247bab16e079e90c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517091"
---
# <span data-ttu-id="2fedb-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fedb-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="2fedb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fedb-102">SYNOPSIS</span></span>
<span data-ttu-id="2fedb-103">Rimuove i metadati dalle configurazioni dei nodi DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="2fedb-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fedb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fedb-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fedb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fedb-105">DESCRIPTION</span></span>
<span data-ttu-id="2fedb-106">Il cmdlet **Remove-AzureRmAutomationDscNodeConfiguration** consente di rimuovere i metadati dalle configurazioni di nodi DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2fedb-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="2fedb-107">Automation archivia la configurazione del nodo DSC come documento di configurazione MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="2fedb-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="2fedb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fedb-108">EXAMPLES</span></span>

## <span data-ttu-id="2fedb-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fedb-109">PARAMETERS</span></span>

### <span data-ttu-id="2fedb-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2fedb-110">-AutomationAccountName</span></span>
<span data-ttu-id="2fedb-111">Specifica il nome di un account di automazione che contiene le configurazioni dei nodi DSC per cui questo cmdlet rimuove i metadati.</span><span class="sxs-lookup"><span data-stu-id="2fedb-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="2fedb-112">-Force</span><span class="sxs-lookup"><span data-stu-id="2fedb-112">-Force</span></span>
<span data-ttu-id="2fedb-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="2fedb-113">ps_force</span></span>

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

### <span data-ttu-id="2fedb-114">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="2fedb-114">-IgnoreNodeMappings</span></span>
<span data-ttu-id="2fedb-115">Indica che questo cmdlet ignora i mapping dei nodi.</span><span class="sxs-lookup"><span data-stu-id="2fedb-115">Indicates that this cmdlet ignores node mappings.</span></span>

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

### <span data-ttu-id="2fedb-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fedb-116">-Name</span></span>
<span data-ttu-id="2fedb-117">Specifica il nome della configurazione del nodo DSC per cui questo cmdlet rimuove i metadati.</span><span class="sxs-lookup"><span data-stu-id="2fedb-117">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="2fedb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fedb-118">-ResourceGroupName</span></span>
<span data-ttu-id="2fedb-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2fedb-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2fedb-120">Questo cmdlet consente di rimuovere i metadati per le configurazioni dei nodi DSC nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2fedb-120">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2fedb-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2fedb-121">-Confirm</span></span>
<span data-ttu-id="2fedb-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fedb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fedb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fedb-123">-WhatIf</span></span>
<span data-ttu-id="2fedb-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fedb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fedb-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fedb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fedb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fedb-126">-DefaultProfile</span></span>
<span data-ttu-id="2fedb-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fedb-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fedb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fedb-128">CommonParameters</span></span>
<span data-ttu-id="2fedb-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fedb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fedb-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fedb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fedb-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fedb-131">INPUTS</span></span>

## <span data-ttu-id="2fedb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fedb-132">OUTPUTS</span></span>

## <span data-ttu-id="2fedb-133">Note</span><span class="sxs-lookup"><span data-stu-id="2fedb-133">NOTES</span></span>

## <span data-ttu-id="2fedb-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fedb-134">RELATED LINKS</span></span>

[<span data-ttu-id="2fedb-135">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fedb-135">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="2fedb-136">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fedb-136">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="2fedb-137">Cmdlet di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="2fedb-137">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


