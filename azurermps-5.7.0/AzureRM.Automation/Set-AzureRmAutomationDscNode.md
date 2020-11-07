---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: 663573e7f4e111880c5ed0014dcad18480f665ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685852"
---
# <span data-ttu-id="b8063-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b8063-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="b8063-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8063-102">SYNOPSIS</span></span>
<span data-ttu-id="b8063-103">Modifica la configurazione del nodo a cui è associato un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="b8063-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8063-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8063-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8063-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8063-105">DESCRIPTION</span></span>
<span data-ttu-id="b8063-106">Il cmdlet **set-AzureRmAutomationDscNode** modifica una configurazione del nodo DSC (APS desired state Configuration).</span><span class="sxs-lookup"><span data-stu-id="b8063-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="b8063-107">Azure Automation archivia la configurazione del nodo DSC come documento di configurazione MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="b8063-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="b8063-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8063-108">EXAMPLES</span></span>

### <span data-ttu-id="b8063-109">Esempio 1: modificare il mapping della configurazione dei nodi</span><span class="sxs-lookup"><span data-stu-id="b8063-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="b8063-110">Questo comando assegna la configurazione del nodo denominata Contoso. NodeConfiguration01 al nodo con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="b8063-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="b8063-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8063-111">PARAMETERS</span></span>

### <span data-ttu-id="b8063-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b8063-112">-AutomationAccountName</span></span>
<span data-ttu-id="b8063-113">Specifica il nome dell'account di automazione che contiene il nodo DSC per cui questo cmdlet modifica la configurazione.</span><span class="sxs-lookup"><span data-stu-id="b8063-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8063-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8063-114">-DefaultProfile</span></span>
<span data-ttu-id="b8063-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b8063-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8063-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b8063-116">-Force</span></span>
<span data-ttu-id="b8063-117">ps_force il comando per l'esecuzione senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b8063-117">ps_force the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8063-118">-ID</span><span class="sxs-lookup"><span data-stu-id="b8063-118">-Id</span></span>
<span data-ttu-id="b8063-119">Specifica l'ID univoco del nodo DSC per cui questo cmdlet modifica la configurazione.</span><span class="sxs-lookup"><span data-stu-id="b8063-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8063-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b8063-120">-NodeConfigurationName</span></span>
<span data-ttu-id="b8063-121">Specifica il nome della configurazione del nodo a cui questo cmdlet esegue il mapping del nodo.</span><span class="sxs-lookup"><span data-stu-id="b8063-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8063-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8063-122">-ResourceGroupName</span></span>
<span data-ttu-id="b8063-123">Specifica il nome di un gruppo di risorse in cui questo cmdlet modifica la configurazione di un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="b8063-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8063-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b8063-124">-Confirm</span></span>
<span data-ttu-id="b8063-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8063-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8063-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8063-126">-WhatIf</span></span>
<span data-ttu-id="b8063-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8063-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8063-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8063-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8063-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8063-129">CommonParameters</span></span>
<span data-ttu-id="b8063-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8063-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8063-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8063-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8063-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8063-132">INPUTS</span></span>

### <span data-ttu-id="b8063-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b8063-133">None</span></span>
<span data-ttu-id="b8063-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b8063-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8063-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8063-135">OUTPUTS</span></span>

### <span data-ttu-id="b8063-136">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="b8063-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="b8063-137">Note</span><span class="sxs-lookup"><span data-stu-id="b8063-137">NOTES</span></span>

## <span data-ttu-id="b8063-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8063-138">RELATED LINKS</span></span>

[<span data-ttu-id="b8063-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b8063-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="b8063-140">Registro-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b8063-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="b8063-141">Annullamento della registrazione-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b8063-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


