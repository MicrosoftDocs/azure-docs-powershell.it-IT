---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205442"
---
# <span data-ttu-id="1a8e6-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="1a8e6-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="1a8e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1a8e6-103">Rimuove un controllo origine di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="1a8e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a8e6-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a8e6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1a8e6-105">DESCRIPTION</span></span>
<span data-ttu-id="1a8e6-106">Il Remove-AzAutomationSourceControl cmdlet rimuove un controllo del codice sorgente dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="1a8e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a8e6-107">EXAMPLES</span></span>

### <span data-ttu-id="1a8e6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a8e6-108">Example 1</span></span>
<span data-ttu-id="1a8e6-109">Questo comando rimuove il controllo origine automazione denominato VSTSNative nell'account denominato devAccount.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="1a8e6-110">Questo comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="1a8e6-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="1a8e6-111">Di conseguenza, non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="1a8e6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a8e6-112">PARAMETERS</span></span>

### <span data-ttu-id="1a8e6-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a8e6-113">-AutomationAccountName</span></span>
<span data-ttu-id="1a8e6-114">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-114">The automation account name.</span></span>

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

### <span data-ttu-id="1a8e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a8e6-115">-DefaultProfile</span></span>
<span data-ttu-id="1a8e6-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a8e6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1a8e6-117">-Name</span></span>
<span data-ttu-id="1a8e6-118">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-118">The source control name.</span></span>

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

### <span data-ttu-id="1a8e6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a8e6-119">-PassThru</span></span>
<span data-ttu-id="1a8e6-120">PassThru restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1a8e6-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a8e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="1a8e6-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-123">The resource group name.</span></span>

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

### <span data-ttu-id="1a8e6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a8e6-124">-Confirm</span></span>
<span data-ttu-id="1a8e6-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a8e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a8e6-126">-WhatIf</span></span>
<span data-ttu-id="1a8e6-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a8e6-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a8e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a8e6-129">CommonParameters</span></span>
<span data-ttu-id="1a8e6-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a8e6-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a8e6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a8e6-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="1a8e6-132">INPUTS</span></span>

### <span data-ttu-id="1a8e6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1a8e6-133">System.String</span></span>

## <span data-ttu-id="1a8e6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a8e6-134">OUTPUTS</span></span>

### <span data-ttu-id="1a8e6-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="1a8e6-135">System.Void</span></span>

### <span data-ttu-id="1a8e6-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a8e6-136">System.Boolean</span></span>

## <span data-ttu-id="1a8e6-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="1a8e6-137">NOTES</span></span>

## <span data-ttu-id="1a8e6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a8e6-138">RELATED LINKS</span></span>
