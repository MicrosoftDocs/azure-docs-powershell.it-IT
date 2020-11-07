---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: b0fc044ee2a4704c9bb6803ab0cf7a4be4ea95e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866344"
---
# <span data-ttu-id="a8afe-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a8afe-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="a8afe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8afe-102">SYNOPSIS</span></span>
<span data-ttu-id="a8afe-103">Rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="a8afe-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8afe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8afe-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8afe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8afe-105">DESCRIPTION</span></span>
<span data-ttu-id="a8afe-106">Il cmdlet **Remove-AzureRmAlertRule** rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="a8afe-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="a8afe-107">Devi specificare il nome della regola di avviso e il gruppo di risorse a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="a8afe-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="a8afe-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a8afe-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a8afe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8afe-109">EXAMPLES</span></span>

### <span data-ttu-id="a8afe-110">Esempio 1: rimuovere una regola di avviso</span><span class="sxs-lookup"><span data-stu-id="a8afe-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="a8afe-111">Questo comando rimuove la regola di avviso denominata Alert-7da64548-214d-42CA-B12B-b245bb8f0ac8 nel gruppo di risorse predefinito-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="a8afe-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="a8afe-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8afe-112">PARAMETERS</span></span>

### <span data-ttu-id="a8afe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8afe-113">-DefaultProfile</span></span>
<span data-ttu-id="a8afe-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a8afe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8afe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8afe-115">-Name</span></span>
<span data-ttu-id="a8afe-116">Specifica il nome della regola di avviso da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a8afe-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="a8afe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8afe-117">-ResourceGroupName</span></span>
<span data-ttu-id="a8afe-118">Specifica il nome del gruppo di risorse per la regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="a8afe-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="a8afe-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8afe-119">-Confirm</span></span>
<span data-ttu-id="a8afe-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8afe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8afe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8afe-121">-WhatIf</span></span>
<span data-ttu-id="a8afe-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8afe-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8afe-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8afe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8afe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8afe-124">CommonParameters</span></span>
<span data-ttu-id="a8afe-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8afe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8afe-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8afe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8afe-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8afe-127">INPUTS</span></span>

### <span data-ttu-id="a8afe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a8afe-128">System.String</span></span>

## <span data-ttu-id="a8afe-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8afe-129">OUTPUTS</span></span>

### <span data-ttu-id="a8afe-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a8afe-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="a8afe-131">Note</span><span class="sxs-lookup"><span data-stu-id="a8afe-131">NOTES</span></span>

## <span data-ttu-id="a8afe-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8afe-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8afe-133">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a8afe-133">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="a8afe-134">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a8afe-134">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="a8afe-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="a8afe-135">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="a8afe-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a8afe-136">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


