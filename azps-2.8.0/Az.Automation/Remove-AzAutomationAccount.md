---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: 8db8ab416203c9e33ec6fd7a30d2c6170318c627
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675735"
---
# <span data-ttu-id="e3638-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e3638-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="e3638-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3638-102">SYNOPSIS</span></span>
<span data-ttu-id="e3638-103">Rimuove un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e3638-103">Removes an Automation account.</span></span>

## <span data-ttu-id="e3638-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3638-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3638-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3638-105">DESCRIPTION</span></span>
<span data-ttu-id="e3638-106">Il cmdlet **Remove-AzAutomationAccount** rimuove un account di automazione di Azure da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3638-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="e3638-107">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="e3638-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="e3638-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3638-108">EXAMPLES</span></span>

### <span data-ttu-id="e3638-109">Esempio 1: rimuovere un account di automazione</span><span class="sxs-lookup"><span data-stu-id="e3638-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e3638-110">Questo comando rimuove un account di automazione denominato ContosoAutomationAccount senza richiedere la convalida dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e3638-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="e3638-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3638-111">PARAMETERS</span></span>

### <span data-ttu-id="e3638-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3638-112">-DefaultProfile</span></span>
<span data-ttu-id="e3638-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e3638-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3638-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e3638-114">-Force</span></span>
<span data-ttu-id="e3638-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="e3638-115">ps_force</span></span>

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

### <span data-ttu-id="e3638-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3638-116">-Name</span></span>
<span data-ttu-id="e3638-117">Specifica il nome dell'account di automazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3638-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3638-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3638-118">-ResourceGroupName</span></span>
<span data-ttu-id="e3638-119">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e3638-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="e3638-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3638-120">-Confirm</span></span>
<span data-ttu-id="e3638-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3638-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3638-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3638-122">-WhatIf</span></span>
<span data-ttu-id="e3638-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3638-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3638-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3638-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3638-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3638-125">CommonParameters</span></span>
<span data-ttu-id="e3638-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3638-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3638-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3638-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3638-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3638-128">INPUTS</span></span>

### <span data-ttu-id="e3638-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e3638-129">System.String</span></span>

## <span data-ttu-id="e3638-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3638-130">OUTPUTS</span></span>

### <span data-ttu-id="e3638-131">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e3638-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e3638-132">Note</span><span class="sxs-lookup"><span data-stu-id="e3638-132">NOTES</span></span>

## <span data-ttu-id="e3638-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3638-133">RELATED LINKS</span></span>

[<span data-ttu-id="e3638-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e3638-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="e3638-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e3638-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="e3638-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e3638-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


