---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 02a6d7a129dc084b982f1827d678354265ddbc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182142"
---
# <span data-ttu-id="b9031-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b9031-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="b9031-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9031-102">SYNOPSIS</span></span>
<span data-ttu-id="b9031-103">Modifica la configurazione del nodo a cui è mappato un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="b9031-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="b9031-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9031-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9031-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b9031-105">DESCRIPTION</span></span>
<span data-ttu-id="b9031-106">Il cmdlet **Set-AzAutomationDscNode** modifica una configurazione del nodo APS Desired State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="b9031-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="b9031-107">Azure Automation archivia la configurazione del nodo DSC come documento di configurazione MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="b9031-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="b9031-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9031-108">EXAMPLES</span></span>

### <span data-ttu-id="b9031-109">Esempio 1: Modificare il mapping di configurazione del nodo</span><span class="sxs-lookup"><span data-stu-id="b9031-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="b9031-110">Questo comando assegna la configurazione del nodo denominata Contoso.NodeConfiguration01 al nodo con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="b9031-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="b9031-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9031-111">PARAMETERS</span></span>

### <span data-ttu-id="b9031-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b9031-112">-AutomationAccountName</span></span>
<span data-ttu-id="b9031-113">Specifica il nome dell'account di automazione che contiene il nodo DSC per cui questo cmdlet modifica la configurazione.</span><span class="sxs-lookup"><span data-stu-id="b9031-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="b9031-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9031-114">-DefaultProfile</span></span>
<span data-ttu-id="b9031-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b9031-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9031-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b9031-116">-Force</span></span>
<span data-ttu-id="b9031-117">ps_force il comando da eseguire senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b9031-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9031-118">-Id</span><span class="sxs-lookup"><span data-stu-id="b9031-118">-Id</span></span>
<span data-ttu-id="b9031-119">Specifica l'ID univoco del nodo DSC per cui questo cmdlet modifica la configurazione.</span><span class="sxs-lookup"><span data-stu-id="b9031-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9031-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b9031-120">-NodeConfigurationName</span></span>
<span data-ttu-id="b9031-121">Specifica il nome della configurazione del nodo a cui questo cmdlet esegue il mapping del nodo.</span><span class="sxs-lookup"><span data-stu-id="b9031-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

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

### <span data-ttu-id="b9031-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9031-122">-ResourceGroupName</span></span>
<span data-ttu-id="b9031-123">Specifica il nome di un gruppo di risorse in cui questo cmdlet modifica la configurazione di un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="b9031-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="b9031-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9031-124">-Confirm</span></span>
<span data-ttu-id="b9031-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9031-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9031-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9031-126">-WhatIf</span></span>
<span data-ttu-id="b9031-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9031-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9031-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9031-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9031-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9031-129">CommonParameters</span></span>
<span data-ttu-id="b9031-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9031-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9031-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9031-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9031-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="b9031-132">INPUTS</span></span>

### <span data-ttu-id="b9031-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b9031-133">System.Guid</span></span>

### <span data-ttu-id="b9031-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b9031-134">System.String</span></span>

## <span data-ttu-id="b9031-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9031-135">OUTPUTS</span></span>

### <span data-ttu-id="b9031-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="b9031-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="b9031-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="b9031-137">NOTES</span></span>

## <span data-ttu-id="b9031-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9031-138">RELATED LINKS</span></span>

[<span data-ttu-id="b9031-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b9031-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="b9031-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b9031-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="b9031-141">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b9031-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


