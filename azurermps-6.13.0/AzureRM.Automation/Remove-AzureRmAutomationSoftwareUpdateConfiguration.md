---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: e0e74aa910c11a10c26cf6bed623d2e2c02f93ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511984"
---
# <span data-ttu-id="65829-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="65829-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="65829-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65829-102">SYNOPSIS</span></span>
<span data-ttu-id="65829-103">Rimuove una configurazione di aggiornamento del software di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="65829-103">Removes an azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65829-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65829-104">SYNTAX</span></span>

### <span data-ttu-id="65829-105">BySucName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="65829-105">BySucName (Default)</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65829-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="65829-106">BySuc</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65829-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65829-107">DESCRIPTION</span></span>
<span data-ttu-id="65829-108">Questo cmdlet ha rimosso una configurazione di aggiornamento del software di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="65829-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="65829-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65829-109">EXAMPLES</span></span>

### <span data-ttu-id="65829-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65829-110">Example 1</span></span>
<span data-ttu-id="65829-111">Questo esempio Mostra come rimuovere "MyUpdateConfiguration" dall'account di automazione</span><span class="sxs-lookup"><span data-stu-id="65829-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="65829-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65829-112">PARAMETERS</span></span>

### <span data-ttu-id="65829-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65829-113">-AutomationAccountName</span></span>
<span data-ttu-id="65829-114">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="65829-114">The automation account name.</span></span>

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

### <span data-ttu-id="65829-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65829-115">-DefaultProfile</span></span>
<span data-ttu-id="65829-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65829-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65829-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="65829-117">-Name</span></span>
<span data-ttu-id="65829-118">Nome della configurazione di aggiornamento software da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="65829-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="65829-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65829-119">-PassThru</span></span>
<span data-ttu-id="65829-120">PassThru restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="65829-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="65829-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="65829-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="65829-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65829-122">-ResourceGroupName</span></span>
<span data-ttu-id="65829-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="65829-123">The resource group name.</span></span>

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

### <span data-ttu-id="65829-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="65829-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="65829-125">Configurazione di aggiornamento software da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="65829-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="65829-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65829-126">-Confirm</span></span>
<span data-ttu-id="65829-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65829-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65829-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65829-128">-WhatIf</span></span>
<span data-ttu-id="65829-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65829-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65829-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65829-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65829-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65829-131">CommonParameters</span></span>
<span data-ttu-id="65829-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65829-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65829-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65829-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65829-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65829-134">INPUTS</span></span>

### <span data-ttu-id="65829-135">System. String</span><span class="sxs-lookup"><span data-stu-id="65829-135">System.String</span></span>

### <span data-ttu-id="65829-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="65829-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="65829-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65829-137">OUTPUTS</span></span>

### <span data-ttu-id="65829-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="65829-138">System.Object</span></span>
## <span data-ttu-id="65829-139">Note</span><span class="sxs-lookup"><span data-stu-id="65829-139">NOTES</span></span>

## <span data-ttu-id="65829-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65829-140">RELATED LINKS</span></span>
