---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 2b0d6096e9691445c939daea113dcdac2fa6c5fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684966"
---
# <span data-ttu-id="77bce-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="77bce-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="77bce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77bce-102">SYNOPSIS</span></span>
<span data-ttu-id="77bce-103">Modifica la configurazione del nodo a cui è associato un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="77bce-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="77bce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77bce-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77bce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77bce-105">DESCRIPTION</span></span>
<span data-ttu-id="77bce-106">Il cmdlet **set-AzAutomationDscNode** modifica una configurazione del nodo DSC (APS desired state Configuration).</span><span class="sxs-lookup"><span data-stu-id="77bce-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="77bce-107">Azure Automation archivia la configurazione del nodo DSC come documento di configurazione MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="77bce-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="77bce-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77bce-108">EXAMPLES</span></span>

### <span data-ttu-id="77bce-109">Esempio 1: modificare il mapping della configurazione dei nodi</span><span class="sxs-lookup"><span data-stu-id="77bce-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="77bce-110">Questo comando assegna la configurazione del nodo denominata Contoso. NodeConfiguration01 al nodo con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="77bce-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="77bce-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77bce-111">PARAMETERS</span></span>

### <span data-ttu-id="77bce-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="77bce-112">-AutomationAccountName</span></span>
<span data-ttu-id="77bce-113">Specifica il nome dell'account di automazione che contiene il nodo DSC per cui questo cmdlet modifica la configurazione.</span><span class="sxs-lookup"><span data-stu-id="77bce-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="77bce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77bce-114">-DefaultProfile</span></span>
<span data-ttu-id="77bce-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="77bce-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77bce-116">-Force</span><span class="sxs-lookup"><span data-stu-id="77bce-116">-Force</span></span>
<span data-ttu-id="77bce-117">ps_force il comando per l'esecuzione senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77bce-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77bce-118">-ID</span><span class="sxs-lookup"><span data-stu-id="77bce-118">-Id</span></span>
<span data-ttu-id="77bce-119">Specifica l'ID univoco del nodo DSC per cui questo cmdlet modifica la configurazione.</span><span class="sxs-lookup"><span data-stu-id="77bce-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="77bce-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="77bce-120">-NodeConfigurationName</span></span>
<span data-ttu-id="77bce-121">Specifica il nome della configurazione del nodo a cui questo cmdlet esegue il mapping del nodo.</span><span class="sxs-lookup"><span data-stu-id="77bce-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

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

### <span data-ttu-id="77bce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77bce-122">-ResourceGroupName</span></span>
<span data-ttu-id="77bce-123">Specifica il nome di un gruppo di risorse in cui questo cmdlet modifica la configurazione di un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="77bce-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="77bce-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77bce-124">-Confirm</span></span>
<span data-ttu-id="77bce-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77bce-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77bce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77bce-126">-WhatIf</span></span>
<span data-ttu-id="77bce-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77bce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77bce-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77bce-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77bce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77bce-129">CommonParameters</span></span>
<span data-ttu-id="77bce-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77bce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77bce-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77bce-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77bce-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77bce-132">INPUTS</span></span>

### <span data-ttu-id="77bce-133">System. Guid</span><span class="sxs-lookup"><span data-stu-id="77bce-133">System.Guid</span></span>

### <span data-ttu-id="77bce-134">System. String</span><span class="sxs-lookup"><span data-stu-id="77bce-134">System.String</span></span>

## <span data-ttu-id="77bce-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77bce-135">OUTPUTS</span></span>

### <span data-ttu-id="77bce-136">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="77bce-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="77bce-137">Note</span><span class="sxs-lookup"><span data-stu-id="77bce-137">NOTES</span></span>

## <span data-ttu-id="77bce-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77bce-138">RELATED LINKS</span></span>

[<span data-ttu-id="77bce-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="77bce-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="77bce-140">Registro-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="77bce-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="77bce-141">Annullamento della registrazione-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="77bce-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)

