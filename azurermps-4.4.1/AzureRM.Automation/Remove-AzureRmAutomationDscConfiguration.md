---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2cd60a70b057689cf7edf154df28253b86e110a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517092"
---
# <span data-ttu-id="b1034-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1034-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="b1034-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1034-102">SYNOPSIS</span></span>
<span data-ttu-id="b1034-103">Rimuove le configurazioni DSC dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="b1034-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1034-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1034-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1034-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1034-105">DESCRIPTION</span></span>
<span data-ttu-id="b1034-106">Il cmdlet **Remove-AzureRmAutomationDscConfiguration** rimuove le configurazioni DSC (APS desired state Configuration) di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b1034-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="b1034-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1034-107">EXAMPLES</span></span>

## <span data-ttu-id="b1034-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1034-108">PARAMETERS</span></span>

### <span data-ttu-id="b1034-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b1034-109">-AutomationAccountName</span></span>
<span data-ttu-id="b1034-110">Specifica il nome dell'account di automazione che contiene le configurazioni DSC rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1034-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1034-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b1034-111">-Force</span></span>
<span data-ttu-id="b1034-112">ps_force</span><span class="sxs-lookup"><span data-stu-id="b1034-112">ps_force</span></span>

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

### <span data-ttu-id="b1034-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1034-113">-Name</span></span>
<span data-ttu-id="b1034-114">Specifica il nome della configurazione DSC rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1034-114">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1034-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1034-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1034-116">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene le configurazioni DSC.</span><span class="sxs-lookup"><span data-stu-id="b1034-116">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="b1034-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1034-117">-Confirm</span></span>
<span data-ttu-id="b1034-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1034-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1034-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1034-119">-WhatIf</span></span>
<span data-ttu-id="b1034-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1034-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1034-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1034-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1034-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1034-122">-DefaultProfile</span></span>
<span data-ttu-id="b1034-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1034-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1034-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1034-124">CommonParameters</span></span>
<span data-ttu-id="b1034-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1034-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1034-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1034-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1034-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1034-127">INPUTS</span></span>

## <span data-ttu-id="b1034-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1034-128">OUTPUTS</span></span>

## <span data-ttu-id="b1034-129">Note</span><span class="sxs-lookup"><span data-stu-id="b1034-129">NOTES</span></span>

## <span data-ttu-id="b1034-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1034-130">RELATED LINKS</span></span>

[<span data-ttu-id="b1034-131">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1034-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="b1034-132">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1034-132">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="b1034-133">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1034-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


