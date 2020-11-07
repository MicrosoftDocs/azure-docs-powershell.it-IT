---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 703be26244e61b797f3359ef508d92e38847bf8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675726"
---
# <span data-ttu-id="7b5ab-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7b5ab-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="7b5ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b5ab-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5ab-103">Rimuove una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="7b5ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b5ab-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b5ab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b5ab-105">DESCRIPTION</span></span>
<span data-ttu-id="7b5ab-106">Il cmdlet **Remove-AzAutomationCredential** consente di rimuovere una credenziale da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="7b5ab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b5ab-107">EXAMPLES</span></span>

### <span data-ttu-id="7b5ab-108">Esempio 1: rimuovere una credenziale</span><span class="sxs-lookup"><span data-stu-id="7b5ab-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7b5ab-109">Questo comando rimuove una credenziale denominata ContosoCredential nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7b5ab-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b5ab-110">PARAMETERS</span></span>

### <span data-ttu-id="7b5ab-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7b5ab-111">-AutomationAccountName</span></span>
<span data-ttu-id="7b5ab-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove una credenziale.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="7b5ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5ab-113">-DefaultProfile</span></span>
<span data-ttu-id="7b5ab-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7b5ab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b5ab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b5ab-115">-Name</span></span>
<span data-ttu-id="7b5ab-116">Specifica il nome delle credenziali rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-116">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b5ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b5ab-118">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una credenziale.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="7b5ab-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b5ab-119">-Confirm</span></span>
<span data-ttu-id="7b5ab-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b5ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b5ab-121">-WhatIf</span></span>
<span data-ttu-id="7b5ab-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b5ab-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b5ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5ab-124">CommonParameters</span></span>
<span data-ttu-id="7b5ab-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b5ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5ab-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b5ab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5ab-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b5ab-127">INPUTS</span></span>

### <span data-ttu-id="7b5ab-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7b5ab-128">System.String</span></span>

## <span data-ttu-id="7b5ab-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b5ab-129">OUTPUTS</span></span>

### <span data-ttu-id="7b5ab-130">System. void</span><span class="sxs-lookup"><span data-stu-id="7b5ab-130">System.Void</span></span>

## <span data-ttu-id="7b5ab-131">Note</span><span class="sxs-lookup"><span data-stu-id="7b5ab-131">NOTES</span></span>

## <span data-ttu-id="7b5ab-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b5ab-132">RELATED LINKS</span></span>

[<span data-ttu-id="7b5ab-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7b5ab-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="7b5ab-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7b5ab-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="7b5ab-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7b5ab-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)

