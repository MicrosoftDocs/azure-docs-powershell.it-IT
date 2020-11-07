---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 9441ce20d4099f0582e64846e026dc201a2047ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678757"
---
# <span data-ttu-id="1df92-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="1df92-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="1df92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1df92-102">SYNOPSIS</span></span>
<span data-ttu-id="1df92-103">Rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="1df92-103">Removes an alert rule.</span></span>

## <span data-ttu-id="1df92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1df92-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1df92-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1df92-105">DESCRIPTION</span></span>
<span data-ttu-id="1df92-106">Il cmdlet **Remove-AzAlertRule** rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="1df92-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="1df92-107">Devi specificare il nome della regola di avviso e il gruppo di risorse a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="1df92-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="1df92-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1df92-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="1df92-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1df92-109">EXAMPLES</span></span>

### <span data-ttu-id="1df92-110">Esempio 1: rimuovere una regola di avviso</span><span class="sxs-lookup"><span data-stu-id="1df92-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="1df92-111">Questo comando rimuove la regola di avviso denominata Alert-7da64548-214d-42CA-B12B-b245bb8f0ac8 nel gruppo di risorse predefinito-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="1df92-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="1df92-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1df92-112">PARAMETERS</span></span>

### <span data-ttu-id="1df92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df92-113">-DefaultProfile</span></span>
<span data-ttu-id="1df92-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1df92-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1df92-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1df92-115">-Name</span></span>
<span data-ttu-id="1df92-116">Specifica il nome della regola di avviso da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1df92-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1df92-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df92-117">-ResourceGroupName</span></span>
<span data-ttu-id="1df92-118">Specifica il nome del gruppo di risorse per la regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="1df92-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1df92-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1df92-119">-Confirm</span></span>
<span data-ttu-id="1df92-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1df92-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1df92-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1df92-121">-WhatIf</span></span>
<span data-ttu-id="1df92-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1df92-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1df92-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1df92-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1df92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df92-124">CommonParameters</span></span>
<span data-ttu-id="1df92-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1df92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df92-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df92-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df92-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1df92-127">INPUTS</span></span>

### <span data-ttu-id="1df92-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1df92-128">System.String</span></span>

## <span data-ttu-id="1df92-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1df92-129">OUTPUTS</span></span>

### <span data-ttu-id="1df92-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1df92-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1df92-131">Note</span><span class="sxs-lookup"><span data-stu-id="1df92-131">NOTES</span></span>

## <span data-ttu-id="1df92-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1df92-132">RELATED LINKS</span></span>

[<span data-ttu-id="1df92-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="1df92-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="1df92-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="1df92-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="1df92-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="1df92-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="1df92-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="1df92-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

