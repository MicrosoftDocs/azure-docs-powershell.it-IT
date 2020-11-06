---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSourceControl.md
ms.openlocfilehash: abd09a195db5652d2dfdffce17096116895eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511980"
---
# <span data-ttu-id="63969-101">Remove-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="63969-101">Remove-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="63969-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63969-102">SYNOPSIS</span></span>
<span data-ttu-id="63969-103">Rimuove un controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="63969-103">Removes an Azure Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63969-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63969-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63969-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63969-105">DESCRIPTION</span></span>
<span data-ttu-id="63969-106">Il cmdlet Remove-AzureRmAutomationSourceControl rimuove un controllo del codice sorgente da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="63969-106">The Remove-AzureRmAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="63969-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63969-107">EXAMPLES</span></span>

### <span data-ttu-id="63969-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="63969-108">Example 1</span></span>
<span data-ttu-id="63969-109">Questo comando rimuove il controllo del codice sorgente di automazione denominato VSTSNative nell'account denominato devAccount.</span><span class="sxs-lookup"><span data-stu-id="63969-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="63969-110">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="63969-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="63969-111">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="63969-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="63969-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63969-112">PARAMETERS</span></span>

### <span data-ttu-id="63969-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="63969-113">-AutomationAccountName</span></span>
<span data-ttu-id="63969-114">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="63969-114">The automation account name.</span></span>

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

### <span data-ttu-id="63969-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63969-115">-DefaultProfile</span></span>
<span data-ttu-id="63969-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63969-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63969-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="63969-117">-Name</span></span>
<span data-ttu-id="63969-118">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="63969-118">The source control name.</span></span>

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

### <span data-ttu-id="63969-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63969-119">-PassThru</span></span>
<span data-ttu-id="63969-120">PassThru restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="63969-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="63969-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="63969-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="63969-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63969-122">-ResourceGroupName</span></span>
<span data-ttu-id="63969-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63969-123">The resource group name.</span></span>

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

### <span data-ttu-id="63969-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63969-124">-Confirm</span></span>
<span data-ttu-id="63969-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63969-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63969-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63969-126">-WhatIf</span></span>
<span data-ttu-id="63969-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63969-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63969-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63969-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63969-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63969-129">CommonParameters</span></span>
<span data-ttu-id="63969-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63969-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63969-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63969-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63969-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63969-132">INPUTS</span></span>

### <span data-ttu-id="63969-133">System. String</span><span class="sxs-lookup"><span data-stu-id="63969-133">System.String</span></span>

## <span data-ttu-id="63969-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63969-134">OUTPUTS</span></span>

### <span data-ttu-id="63969-135">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="63969-135">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="63969-136">Note</span><span class="sxs-lookup"><span data-stu-id="63969-136">NOTES</span></span>

## <span data-ttu-id="63969-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63969-137">RELATED LINKS</span></span>
