---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 42fc322e9f593ecad6c295952d46274eb2563799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517087"
---
# <span data-ttu-id="ef001-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ef001-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="ef001-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef001-102">SYNOPSIS</span></span>
<span data-ttu-id="ef001-103">Rimuove un modulo dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="ef001-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef001-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef001-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef001-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef001-105">DESCRIPTION</span></span>
<span data-ttu-id="ef001-106">Il cmdlet **Remove-AzureRmAutomationModule** rimuove un modulo da un account di automazione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ef001-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="ef001-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef001-107">EXAMPLES</span></span>

### <span data-ttu-id="ef001-108">Esempio 1: rimuovere un modulo</span><span class="sxs-lookup"><span data-stu-id="ef001-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ef001-109">Questo comando rimuove un modulo denominato ContosoModule dall'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ef001-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ef001-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef001-110">PARAMETERS</span></span>

### <span data-ttu-id="ef001-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef001-111">-AutomationAccountName</span></span>
<span data-ttu-id="ef001-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove un modulo.</span><span class="sxs-lookup"><span data-stu-id="ef001-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="ef001-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ef001-113">-Force</span></span>
<span data-ttu-id="ef001-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="ef001-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef001-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef001-115">-Name</span></span>
<span data-ttu-id="ef001-116">Specifica il nome del modulo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef001-116">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ef001-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef001-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef001-118">Specifica il nome di un gruppo di risorse in cui questo cmdlet rimuove un modulo.</span><span class="sxs-lookup"><span data-stu-id="ef001-118">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="ef001-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ef001-119">-Confirm</span></span>
<span data-ttu-id="ef001-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef001-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef001-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef001-121">-WhatIf</span></span>
<span data-ttu-id="ef001-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef001-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef001-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef001-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef001-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef001-124">-DefaultProfile</span></span>
<span data-ttu-id="ef001-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef001-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef001-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef001-126">CommonParameters</span></span>
<span data-ttu-id="ef001-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef001-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef001-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef001-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef001-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef001-129">INPUTS</span></span>

## <span data-ttu-id="ef001-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef001-130">OUTPUTS</span></span>

## <span data-ttu-id="ef001-131">Note</span><span class="sxs-lookup"><span data-stu-id="ef001-131">NOTES</span></span>

## <span data-ttu-id="ef001-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef001-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef001-133">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ef001-133">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="ef001-134">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ef001-134">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="ef001-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ef001-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


