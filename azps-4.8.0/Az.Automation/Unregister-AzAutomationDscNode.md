---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: d6d233bcd9ac439d163c0b6de6866a0c7dac0b04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190582"
---
# <span data-ttu-id="8a1ae-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8a1ae-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="8a1ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="8a1ae-103">Rimuove un nodo DSC dalla gestione di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="8a1ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a1ae-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a1ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a1ae-105">DESCRIPTION</span></span>
<span data-ttu-id="8a1ae-106">Il cmdlet **Unregister-AzAutomationDscNode** rimuove un nodo DSC (APS desired state Configuration) dalla gestione di un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="8a1ae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a1ae-107">EXAMPLES</span></span>

### <span data-ttu-id="8a1ae-108">Esempio 1: rimuovere un nodo Azure DSC dalla gestione di un account di automazione</span><span class="sxs-lookup"><span data-stu-id="8a1ae-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="8a1ae-109">Questo comando rimuove il nodo DSC che ha il GUID specificato dalla gestione dall'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8a1ae-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a1ae-110">PARAMETERS</span></span>

### <span data-ttu-id="8a1ae-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8a1ae-111">-AutomationAccountName</span></span>
<span data-ttu-id="8a1ae-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="8a1ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a1ae-113">-DefaultProfile</span></span>
<span data-ttu-id="8a1ae-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8a1ae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a1ae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a1ae-115">-Force</span></span>
<span data-ttu-id="8a1ae-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="8a1ae-116">ps_force</span></span>

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

### <span data-ttu-id="8a1ae-117">-ID</span><span class="sxs-lookup"><span data-stu-id="8a1ae-117">-Id</span></span>
<span data-ttu-id="8a1ae-118">Specifica l'ID univoco del nodo DSC rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a1ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a1ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a1ae-120">Specifica il nome di un gruppo di risorse in cui questo cmdlet Annulla la registrazione di un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="8a1ae-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a1ae-121">-Confirm</span></span>
<span data-ttu-id="8a1ae-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a1ae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a1ae-123">-WhatIf</span></span>
<span data-ttu-id="8a1ae-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a1ae-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a1ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a1ae-126">CommonParameters</span></span>
<span data-ttu-id="8a1ae-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a1ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a1ae-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a1ae-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a1ae-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a1ae-129">INPUTS</span></span>

### <span data-ttu-id="8a1ae-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="8a1ae-130">System.Guid</span></span>

### <span data-ttu-id="8a1ae-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8a1ae-131">System.String</span></span>

## <span data-ttu-id="8a1ae-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a1ae-132">OUTPUTS</span></span>

### <span data-ttu-id="8a1ae-133">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="8a1ae-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="8a1ae-134">Note</span><span class="sxs-lookup"><span data-stu-id="8a1ae-134">NOTES</span></span>

## <span data-ttu-id="8a1ae-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a1ae-135">RELATED LINKS</span></span>

[<span data-ttu-id="8a1ae-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8a1ae-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="8a1ae-137">Registro-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8a1ae-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="8a1ae-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8a1ae-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


