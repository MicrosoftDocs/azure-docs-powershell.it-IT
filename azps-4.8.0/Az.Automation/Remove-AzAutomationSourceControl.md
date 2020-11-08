---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190594"
---
# <span data-ttu-id="84348-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="84348-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="84348-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84348-102">SYNOPSIS</span></span>
<span data-ttu-id="84348-103">Rimuove un controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="84348-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="84348-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84348-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84348-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84348-105">DESCRIPTION</span></span>
<span data-ttu-id="84348-106">Il cmdlet Remove-AzAutomationSourceControl rimuove un controllo del codice sorgente da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="84348-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="84348-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84348-107">EXAMPLES</span></span>

### <span data-ttu-id="84348-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84348-108">Example 1</span></span>
<span data-ttu-id="84348-109">Questo comando rimuove il controllo del codice sorgente di automazione denominato VSTSNative nell'account denominato devAccount.</span><span class="sxs-lookup"><span data-stu-id="84348-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="84348-110">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="84348-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="84348-111">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="84348-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="84348-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84348-112">PARAMETERS</span></span>

### <span data-ttu-id="84348-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="84348-113">-AutomationAccountName</span></span>
<span data-ttu-id="84348-114">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="84348-114">The automation account name.</span></span>

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

### <span data-ttu-id="84348-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84348-115">-DefaultProfile</span></span>
<span data-ttu-id="84348-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84348-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84348-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="84348-117">-Name</span></span>
<span data-ttu-id="84348-118">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="84348-118">The source control name.</span></span>

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

### <span data-ttu-id="84348-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84348-119">-PassThru</span></span>
<span data-ttu-id="84348-120">PassThru restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="84348-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84348-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="84348-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="84348-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84348-122">-ResourceGroupName</span></span>
<span data-ttu-id="84348-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84348-123">The resource group name.</span></span>

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

### <span data-ttu-id="84348-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84348-124">-Confirm</span></span>
<span data-ttu-id="84348-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84348-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84348-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84348-126">-WhatIf</span></span>
<span data-ttu-id="84348-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84348-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84348-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84348-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84348-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84348-129">CommonParameters</span></span>
<span data-ttu-id="84348-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84348-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84348-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84348-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84348-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84348-132">INPUTS</span></span>

### <span data-ttu-id="84348-133">System. String</span><span class="sxs-lookup"><span data-stu-id="84348-133">System.String</span></span>

## <span data-ttu-id="84348-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84348-134">OUTPUTS</span></span>

### <span data-ttu-id="84348-135">System. void</span><span class="sxs-lookup"><span data-stu-id="84348-135">System.Void</span></span>

### <span data-ttu-id="84348-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84348-136">System.Boolean</span></span>

## <span data-ttu-id="84348-137">Note</span><span class="sxs-lookup"><span data-stu-id="84348-137">NOTES</span></span>

## <span data-ttu-id="84348-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84348-138">RELATED LINKS</span></span>
