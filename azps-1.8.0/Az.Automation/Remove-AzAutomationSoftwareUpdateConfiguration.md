---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 3b608feb9ed496be72d1d74f4a5a2be0569714de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684985"
---
# <span data-ttu-id="7c24e-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c24e-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="7c24e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c24e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c24e-103">Rimuove una configurazione di aggiornamento del software di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7c24e-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="7c24e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c24e-104">SYNTAX</span></span>

### <span data-ttu-id="7c24e-105">BySucName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c24e-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c24e-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="7c24e-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c24e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c24e-107">DESCRIPTION</span></span>
<span data-ttu-id="7c24e-108">Questo cmdlet ha rimosso una configurazione di aggiornamento del software di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7c24e-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="7c24e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c24e-109">EXAMPLES</span></span>

### <span data-ttu-id="7c24e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c24e-110">Example 1</span></span>
<span data-ttu-id="7c24e-111">Questo esempio Mostra come rimuovere "MyUpdateConfiguration" dall'account di automazione</span><span class="sxs-lookup"><span data-stu-id="7c24e-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="7c24e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c24e-112">PARAMETERS</span></span>

### <span data-ttu-id="7c24e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7c24e-113">-AutomationAccountName</span></span>
<span data-ttu-id="7c24e-114">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="7c24e-114">The automation account name.</span></span>

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

### <span data-ttu-id="7c24e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c24e-115">-DefaultProfile</span></span>
<span data-ttu-id="7c24e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c24e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c24e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c24e-117">-Name</span></span>
<span data-ttu-id="7c24e-118">Nome della configurazione di aggiornamento software da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7c24e-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="7c24e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c24e-119">-PassThru</span></span>
<span data-ttu-id="7c24e-120">PassThru restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="7c24e-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="7c24e-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7c24e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c24e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c24e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c24e-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c24e-123">The resource group name.</span></span>

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

### <span data-ttu-id="7c24e-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c24e-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="7c24e-125">Configurazione di aggiornamento software da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7c24e-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="7c24e-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c24e-126">-Confirm</span></span>
<span data-ttu-id="7c24e-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c24e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c24e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c24e-128">-WhatIf</span></span>
<span data-ttu-id="7c24e-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c24e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c24e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c24e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c24e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c24e-131">CommonParameters</span></span>
<span data-ttu-id="7c24e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c24e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c24e-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c24e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c24e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c24e-134">INPUTS</span></span>

### <span data-ttu-id="7c24e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7c24e-135">System.String</span></span>

### <span data-ttu-id="7c24e-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c24e-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="7c24e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c24e-137">OUTPUTS</span></span>

### <span data-ttu-id="7c24e-138">System. void</span><span class="sxs-lookup"><span data-stu-id="7c24e-138">System.Void</span></span>

### <span data-ttu-id="7c24e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c24e-139">System.Boolean</span></span>

## <span data-ttu-id="7c24e-140">Note</span><span class="sxs-lookup"><span data-stu-id="7c24e-140">NOTES</span></span>

## <span data-ttu-id="7c24e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c24e-141">RELATED LINKS</span></span>
