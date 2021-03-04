---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 8ddc84e3fac5df9253ffdacb61d4f4c7a5568c6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957758"
---
# <span data-ttu-id="719cf-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="719cf-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="719cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="719cf-102">SYNOPSIS</span></span>
<span data-ttu-id="719cf-103">Rimuove una configurazione di aggiornamento software di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="719cf-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="719cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="719cf-104">SYNTAX</span></span>

### <span data-ttu-id="719cf-105">BySucName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="719cf-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="719cf-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="719cf-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="719cf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="719cf-107">DESCRIPTION</span></span>
<span data-ttu-id="719cf-108">Questo cmdlet ha rimosso una configurazione di aggiornamento software di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="719cf-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="719cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="719cf-109">EXAMPLES</span></span>

### <span data-ttu-id="719cf-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="719cf-110">Example 1</span></span>
<span data-ttu-id="719cf-111">Questo esempio mostra come rimuovere "MyUpdateConfiguration" dall'account di automazione</span><span class="sxs-lookup"><span data-stu-id="719cf-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="719cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="719cf-112">PARAMETERS</span></span>

### <span data-ttu-id="719cf-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="719cf-113">-AutomationAccountName</span></span>
<span data-ttu-id="719cf-114">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="719cf-114">The automation account name.</span></span>

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

### <span data-ttu-id="719cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="719cf-115">-DefaultProfile</span></span>
<span data-ttu-id="719cf-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="719cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="719cf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="719cf-117">-Name</span></span>
<span data-ttu-id="719cf-118">Nome della configurazione di aggiornamento software da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="719cf-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="719cf-119">-PassThru</span></span>
<span data-ttu-id="719cf-120">PassThru restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="719cf-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="719cf-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="719cf-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="719cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="719cf-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="719cf-123">The resource group name.</span></span>

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

### <span data-ttu-id="719cf-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="719cf-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="719cf-125">Configurazione degli aggiornamenti software da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="719cf-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="719cf-126">-Confirm</span></span>
<span data-ttu-id="719cf-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="719cf-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="719cf-128">-WhatIf</span></span>
<span data-ttu-id="719cf-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="719cf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="719cf-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="719cf-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="719cf-131">CommonParameters</span></span>
<span data-ttu-id="719cf-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="719cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="719cf-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="719cf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="719cf-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="719cf-134">INPUTS</span></span>

### <span data-ttu-id="719cf-135">System.String</span><span class="sxs-lookup"><span data-stu-id="719cf-135">System.String</span></span>

### <span data-ttu-id="719cf-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="719cf-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="719cf-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="719cf-137">OUTPUTS</span></span>

### <span data-ttu-id="719cf-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="719cf-138">System.Void</span></span>

### <span data-ttu-id="719cf-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="719cf-139">System.Boolean</span></span>

## <span data-ttu-id="719cf-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="719cf-140">NOTES</span></span>

## <span data-ttu-id="719cf-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="719cf-141">RELATED LINKS</span></span>
