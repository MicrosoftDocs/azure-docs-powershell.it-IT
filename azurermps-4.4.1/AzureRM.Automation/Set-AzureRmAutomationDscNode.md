---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: d7b5d3102aa7f5f9965b3e4da1a79b322141a3d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511352"
---
# <span data-ttu-id="27f5d-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="27f5d-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="27f5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="27f5d-103">Modifica la configurazione del nodo a cui è associato un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="27f5d-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27f5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27f5d-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27f5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="27f5d-106">Il cmdlet **set-AzureRmAutomationDscNode** modifica una configurazione del nodo DSC (APS desired state Configuration).</span><span class="sxs-lookup"><span data-stu-id="27f5d-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="27f5d-107">Azure Automation archivia la configurazione del nodo DSC come documento di configurazione MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="27f5d-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="27f5d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27f5d-108">EXAMPLES</span></span>

### <span data-ttu-id="27f5d-109">Esempio 1: modificare il mapping della configurazione dei nodi</span><span class="sxs-lookup"><span data-stu-id="27f5d-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="27f5d-110">Questo comando assegna la configurazione del nodo denominata Contoso. NodeConfiguration01 al nodo con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="27f5d-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="27f5d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27f5d-111">PARAMETERS</span></span>

### <span data-ttu-id="27f5d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="27f5d-112">-AutomationAccountName</span></span>
<span data-ttu-id="27f5d-113">Specifica il nome dell'account di automazione che contiene il nodo DSC per cui questo cmdlet modifica la configurazione.</span><span class="sxs-lookup"><span data-stu-id="27f5d-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="27f5d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="27f5d-114">-Force</span></span>
<span data-ttu-id="27f5d-115">ps_force il comando per l'esecuzione senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="27f5d-115">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27f5d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="27f5d-116">-Id</span></span>
<span data-ttu-id="27f5d-117">Specifica l'ID univoco del nodo DSC per cui questo cmdlet modifica la configurazione.</span><span class="sxs-lookup"><span data-stu-id="27f5d-117">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="27f5d-118">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="27f5d-118">-NodeConfigurationName</span></span>
<span data-ttu-id="27f5d-119">Specifica il nome della configurazione del nodo a cui questo cmdlet esegue il mapping del nodo.</span><span class="sxs-lookup"><span data-stu-id="27f5d-119">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

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

### <span data-ttu-id="27f5d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27f5d-120">-ResourceGroupName</span></span>
<span data-ttu-id="27f5d-121">Specifica il nome di un gruppo di risorse in cui questo cmdlet modifica la configurazione di un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="27f5d-121">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="27f5d-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27f5d-122">-Confirm</span></span>
<span data-ttu-id="27f5d-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27f5d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27f5d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27f5d-124">-WhatIf</span></span>
<span data-ttu-id="27f5d-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27f5d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27f5d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27f5d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27f5d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27f5d-127">-DefaultProfile</span></span>
<span data-ttu-id="27f5d-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27f5d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27f5d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27f5d-129">CommonParameters</span></span>
<span data-ttu-id="27f5d-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27f5d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27f5d-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27f5d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27f5d-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27f5d-132">INPUTS</span></span>

## <span data-ttu-id="27f5d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27f5d-133">OUTPUTS</span></span>

### <span data-ttu-id="27f5d-134">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="27f5d-134">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="27f5d-135">Note</span><span class="sxs-lookup"><span data-stu-id="27f5d-135">NOTES</span></span>

## <span data-ttu-id="27f5d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27f5d-136">RELATED LINKS</span></span>

[<span data-ttu-id="27f5d-137">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="27f5d-137">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="27f5d-138">Registro-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="27f5d-138">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="27f5d-139">Annullamento della registrazione-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="27f5d-139">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


