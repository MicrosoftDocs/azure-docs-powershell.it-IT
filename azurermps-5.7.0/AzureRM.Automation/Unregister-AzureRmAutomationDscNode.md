---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 486664833e585733dc02a5c6f1c94d8673dfc4a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519927"
---
# <span data-ttu-id="e9002-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e9002-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="e9002-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9002-102">SYNOPSIS</span></span>
<span data-ttu-id="e9002-103">Rimuove un nodo DSC dalla gestione di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e9002-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9002-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9002-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9002-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9002-105">DESCRIPTION</span></span>
<span data-ttu-id="e9002-106">Il cmdlet **Unregister-AzureRmAutomationDscNode** rimuove un nodo DSC (APS desired state Configuration) dalla gestione di un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9002-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="e9002-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9002-107">EXAMPLES</span></span>

### <span data-ttu-id="e9002-108">Esempio 1: rimuovere un nodo Azure DSC dalla gestione di un account di automazione</span><span class="sxs-lookup"><span data-stu-id="e9002-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="e9002-109">Questo comando rimuove il nodo DSC che ha il GUID specificato dalla gestione dall'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e9002-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e9002-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9002-110">PARAMETERS</span></span>

### <span data-ttu-id="e9002-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9002-111">-AutomationAccountName</span></span>
<span data-ttu-id="e9002-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="e9002-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="e9002-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9002-113">-DefaultProfile</span></span>
<span data-ttu-id="e9002-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e9002-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9002-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e9002-115">-Force</span></span>
<span data-ttu-id="e9002-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="e9002-116">ps_force</span></span>

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

### <span data-ttu-id="e9002-117">-ID</span><span class="sxs-lookup"><span data-stu-id="e9002-117">-Id</span></span>
<span data-ttu-id="e9002-118">Specifica l'ID univoco del nodo DSC rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9002-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9002-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9002-119">-ResourceGroupName</span></span>
<span data-ttu-id="e9002-120">Specifica il nome di un gruppo di risorse in cui questo cmdlet Annulla la registrazione di un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="e9002-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="e9002-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e9002-121">-Confirm</span></span>
<span data-ttu-id="e9002-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9002-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9002-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9002-123">-WhatIf</span></span>
<span data-ttu-id="e9002-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9002-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9002-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9002-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9002-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9002-126">CommonParameters</span></span>
<span data-ttu-id="e9002-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9002-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9002-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9002-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9002-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9002-129">INPUTS</span></span>

### <span data-ttu-id="e9002-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e9002-130">None</span></span>
<span data-ttu-id="e9002-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e9002-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9002-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9002-132">OUTPUTS</span></span>

### <span data-ttu-id="e9002-133">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="e9002-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="e9002-134">Note</span><span class="sxs-lookup"><span data-stu-id="e9002-134">NOTES</span></span>

## <span data-ttu-id="e9002-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9002-135">RELATED LINKS</span></span>

[<span data-ttu-id="e9002-136">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e9002-136">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="e9002-137">Registro-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e9002-137">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="e9002-138">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e9002-138">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


