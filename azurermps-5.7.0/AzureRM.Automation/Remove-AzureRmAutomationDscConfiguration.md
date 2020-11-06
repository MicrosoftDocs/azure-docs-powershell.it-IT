---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: c328dcbf912b5b907f0e27c902bc7eb3dc31a44e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510163"
---
# <span data-ttu-id="a6787-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6787-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="a6787-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6787-102">SYNOPSIS</span></span>
<span data-ttu-id="a6787-103">Rimuove le configurazioni DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="a6787-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6787-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6787-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6787-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6787-105">DESCRIPTION</span></span>
<span data-ttu-id="a6787-106">Il cmdlet **Remove-AzureRmAutomationDscConfiguration** rimuove le configurazioni DSC (APS desired state Configuration) di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a6787-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="a6787-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6787-107">EXAMPLES</span></span>

## <span data-ttu-id="a6787-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6787-108">PARAMETERS</span></span>

### <span data-ttu-id="a6787-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6787-109">-AutomationAccountName</span></span>
<span data-ttu-id="a6787-110">Specifica il nome dell'account di automazione che contiene le configurazioni DSC rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6787-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6787-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6787-111">-DefaultProfile</span></span>
<span data-ttu-id="a6787-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a6787-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6787-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a6787-113">-Force</span></span>
<span data-ttu-id="a6787-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="a6787-114">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6787-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6787-115">-Name</span></span>
<span data-ttu-id="a6787-116">Specifica il nome della configurazione DSC rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6787-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6787-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6787-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6787-118">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene le configurazioni DSC.</span><span class="sxs-lookup"><span data-stu-id="a6787-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="a6787-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6787-119">-Confirm</span></span>
<span data-ttu-id="a6787-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6787-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6787-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6787-121">-WhatIf</span></span>
<span data-ttu-id="a6787-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6787-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6787-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6787-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6787-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6787-124">CommonParameters</span></span>
<span data-ttu-id="a6787-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6787-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6787-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6787-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6787-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6787-127">INPUTS</span></span>

### <span data-ttu-id="a6787-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a6787-128">None</span></span>
<span data-ttu-id="a6787-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a6787-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6787-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6787-130">OUTPUTS</span></span>

## <span data-ttu-id="a6787-131">Note</span><span class="sxs-lookup"><span data-stu-id="a6787-131">NOTES</span></span>

## <span data-ttu-id="a6787-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6787-132">RELATED LINKS</span></span>

[<span data-ttu-id="a6787-133">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6787-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="a6787-134">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6787-134">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="a6787-135">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6787-135">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


