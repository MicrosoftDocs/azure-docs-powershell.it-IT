---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022893"
---
# <span data-ttu-id="3819a-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3819a-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="3819a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3819a-102">SYNOPSIS</span></span>
<span data-ttu-id="3819a-103">Rimuove una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="3819a-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="3819a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3819a-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3819a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3819a-105">DESCRIPTION</span></span>
<span data-ttu-id="3819a-106">Il cmdlet **Remove-AzAutomationCredential** consente di rimuovere una credenziale da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3819a-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="3819a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3819a-107">EXAMPLES</span></span>

### <span data-ttu-id="3819a-108">Esempio 1: rimuovere una credenziale</span><span class="sxs-lookup"><span data-stu-id="3819a-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3819a-109">Questo comando rimuove una credenziale denominata ContosoCredential nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3819a-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3819a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3819a-110">PARAMETERS</span></span>

### <span data-ttu-id="3819a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3819a-111">-AutomationAccountName</span></span>
<span data-ttu-id="3819a-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove una credenziale.</span><span class="sxs-lookup"><span data-stu-id="3819a-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="3819a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3819a-113">-DefaultProfile</span></span>
<span data-ttu-id="3819a-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3819a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3819a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3819a-115">-Name</span></span>
<span data-ttu-id="3819a-116">Specifica il nome delle credenziali rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3819a-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3819a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3819a-117">-ResourceGroupName</span></span>
<span data-ttu-id="3819a-118">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una credenziale.</span><span class="sxs-lookup"><span data-stu-id="3819a-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="3819a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3819a-119">-Confirm</span></span>
<span data-ttu-id="3819a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3819a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3819a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3819a-121">-WhatIf</span></span>
<span data-ttu-id="3819a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3819a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3819a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3819a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3819a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3819a-124">CommonParameters</span></span>
<span data-ttu-id="3819a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3819a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3819a-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3819a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3819a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3819a-127">INPUTS</span></span>

### <span data-ttu-id="3819a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3819a-128">System.String</span></span>

## <span data-ttu-id="3819a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3819a-129">OUTPUTS</span></span>

### <span data-ttu-id="3819a-130">System. void</span><span class="sxs-lookup"><span data-stu-id="3819a-130">System.Void</span></span>

## <span data-ttu-id="3819a-131">Note</span><span class="sxs-lookup"><span data-stu-id="3819a-131">NOTES</span></span>

## <span data-ttu-id="3819a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3819a-132">RELATED LINKS</span></span>

[<span data-ttu-id="3819a-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3819a-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="3819a-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3819a-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="3819a-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3819a-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


