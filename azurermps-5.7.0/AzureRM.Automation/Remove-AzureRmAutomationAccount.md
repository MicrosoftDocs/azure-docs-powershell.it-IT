---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 854a5bd2fb9644d6060810edba44ac7082eb6903
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515804"
---
# <span data-ttu-id="e229f-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e229f-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="e229f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e229f-102">SYNOPSIS</span></span>
<span data-ttu-id="e229f-103">Rimuove un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e229f-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e229f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e229f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e229f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e229f-105">DESCRIPTION</span></span>
<span data-ttu-id="e229f-106">Il cmdlet **Remove-AzureRmAutomationAccount** rimuove un account di automazione di Azure da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e229f-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="e229f-107">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="e229f-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="e229f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e229f-108">EXAMPLES</span></span>

### <span data-ttu-id="e229f-109">Esempio 1: rimuovere un account di automazione</span><span class="sxs-lookup"><span data-stu-id="e229f-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e229f-110">Questo comando rimuove un account di automazione denominato ContosoAutomationAccount senza richiedere la convalida dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e229f-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="e229f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e229f-111">PARAMETERS</span></span>

### <span data-ttu-id="e229f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e229f-112">-DefaultProfile</span></span>
<span data-ttu-id="e229f-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e229f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e229f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e229f-114">-Force</span></span>
<span data-ttu-id="e229f-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="e229f-115">ps_force</span></span>

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

### <span data-ttu-id="e229f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e229f-116">-Name</span></span>
<span data-ttu-id="e229f-117">Specifica il nome dell'account di automazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e229f-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e229f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e229f-118">-ResourceGroupName</span></span>
<span data-ttu-id="e229f-119">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e229f-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="e229f-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e229f-120">-Confirm</span></span>
<span data-ttu-id="e229f-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e229f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e229f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e229f-122">-WhatIf</span></span>
<span data-ttu-id="e229f-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e229f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e229f-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e229f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e229f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e229f-125">CommonParameters</span></span>
<span data-ttu-id="e229f-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e229f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e229f-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e229f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e229f-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e229f-128">INPUTS</span></span>

### <span data-ttu-id="e229f-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e229f-129">None</span></span>
<span data-ttu-id="e229f-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e229f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e229f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e229f-131">OUTPUTS</span></span>

### <span data-ttu-id="e229f-132">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e229f-132">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e229f-133">Note</span><span class="sxs-lookup"><span data-stu-id="e229f-133">NOTES</span></span>

## <span data-ttu-id="e229f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e229f-134">RELATED LINKS</span></span>

[<span data-ttu-id="e229f-135">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e229f-135">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="e229f-136">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e229f-136">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="e229f-137">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e229f-137">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


