---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: 165850e0212969fea76e85f209d3fcf7c2040b79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684981"
---
# <span data-ttu-id="deafa-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="deafa-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="deafa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="deafa-102">SYNOPSIS</span></span>
<span data-ttu-id="deafa-103">Rimuove un controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="deafa-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="deafa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="deafa-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="deafa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="deafa-105">DESCRIPTION</span></span>
<span data-ttu-id="deafa-106">Il cmdlet Remove-AzAutomationSourceControl rimuove un controllo del codice sorgente da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="deafa-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="deafa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="deafa-107">EXAMPLES</span></span>

### <span data-ttu-id="deafa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="deafa-108">Example 1</span></span>
<span data-ttu-id="deafa-109">Questo comando rimuove il controllo del codice sorgente di automazione denominato VSTSNative nell'account denominato devAccount.</span><span class="sxs-lookup"><span data-stu-id="deafa-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="deafa-110">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="deafa-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="deafa-111">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="deafa-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="deafa-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="deafa-112">PARAMETERS</span></span>

### <span data-ttu-id="deafa-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="deafa-113">-AutomationAccountName</span></span>
<span data-ttu-id="deafa-114">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="deafa-114">The automation account name.</span></span>

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

### <span data-ttu-id="deafa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deafa-115">-DefaultProfile</span></span>
<span data-ttu-id="deafa-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="deafa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deafa-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="deafa-117">-Name</span></span>
<span data-ttu-id="deafa-118">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="deafa-118">The source control name.</span></span>

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

### <span data-ttu-id="deafa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="deafa-119">-PassThru</span></span>
<span data-ttu-id="deafa-120">PassThru restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="deafa-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="deafa-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="deafa-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="deafa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deafa-122">-ResourceGroupName</span></span>
<span data-ttu-id="deafa-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="deafa-123">The resource group name.</span></span>

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

### <span data-ttu-id="deafa-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="deafa-124">-Confirm</span></span>
<span data-ttu-id="deafa-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deafa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deafa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deafa-126">-WhatIf</span></span>
<span data-ttu-id="deafa-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="deafa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deafa-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="deafa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deafa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deafa-129">CommonParameters</span></span>
<span data-ttu-id="deafa-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deafa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deafa-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deafa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deafa-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="deafa-132">INPUTS</span></span>

### <span data-ttu-id="deafa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="deafa-133">System.String</span></span>

## <span data-ttu-id="deafa-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="deafa-134">OUTPUTS</span></span>

### <span data-ttu-id="deafa-135">System. void</span><span class="sxs-lookup"><span data-stu-id="deafa-135">System.Void</span></span>

### <span data-ttu-id="deafa-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="deafa-136">System.Boolean</span></span>

## <span data-ttu-id="deafa-137">Note</span><span class="sxs-lookup"><span data-stu-id="deafa-137">NOTES</span></span>

## <span data-ttu-id="deafa-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="deafa-138">RELATED LINKS</span></span>
