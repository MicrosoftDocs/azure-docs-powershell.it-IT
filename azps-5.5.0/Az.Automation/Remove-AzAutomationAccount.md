---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205539"
---
# <span data-ttu-id="8ce28-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ce28-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="8ce28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ce28-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce28-103">Rimuove un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="8ce28-103">Removes an Automation account.</span></span>

## <span data-ttu-id="8ce28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ce28-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ce28-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8ce28-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce28-106">Il cmdlet **Remove-AzAutomationAccount** rimuove un account di automazione di Azure da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8ce28-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="8ce28-107">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="8ce28-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="8ce28-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ce28-108">EXAMPLES</span></span>

### <span data-ttu-id="8ce28-109">Esempio 1: Rimuovere un account di automazione</span><span class="sxs-lookup"><span data-stu-id="8ce28-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8ce28-110">Questo comando rimuove un account di automazione denominato ContosoAutomationAccount senza richiedere la convalida dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8ce28-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="8ce28-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ce28-111">PARAMETERS</span></span>

### <span data-ttu-id="8ce28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce28-112">-DefaultProfile</span></span>
<span data-ttu-id="8ce28-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="8ce28-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ce28-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8ce28-114">-Force</span></span>
<span data-ttu-id="8ce28-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="8ce28-115">ps_force</span></span>

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

### <span data-ttu-id="8ce28-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8ce28-116">-Name</span></span>
<span data-ttu-id="8ce28-117">Specifica il nome dell'account di automazione rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ce28-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8ce28-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce28-118">-ResourceGroupName</span></span>
<span data-ttu-id="8ce28-119">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="8ce28-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="8ce28-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ce28-120">-Confirm</span></span>
<span data-ttu-id="8ce28-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ce28-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce28-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce28-122">-WhatIf</span></span>
<span data-ttu-id="8ce28-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ce28-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ce28-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ce28-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce28-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce28-125">CommonParameters</span></span>
<span data-ttu-id="8ce28-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ce28-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce28-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce28-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce28-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="8ce28-128">INPUTS</span></span>

### <span data-ttu-id="8ce28-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8ce28-129">System.String</span></span>

## <span data-ttu-id="8ce28-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ce28-130">OUTPUTS</span></span>

### <span data-ttu-id="8ce28-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ce28-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="8ce28-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="8ce28-132">NOTES</span></span>

## <span data-ttu-id="8ce28-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ce28-133">RELATED LINKS</span></span>

[<span data-ttu-id="8ce28-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ce28-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="8ce28-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ce28-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="8ce28-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ce28-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


