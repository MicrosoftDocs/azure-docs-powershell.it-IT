---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: bca70877b8821b06e6662f334120f126328f4451
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521000"
---
# <span data-ttu-id="095aa-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="095aa-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="095aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="095aa-102">SYNOPSIS</span></span>
<span data-ttu-id="095aa-103">Rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="095aa-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="095aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="095aa-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="095aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="095aa-105">DESCRIPTION</span></span>
<span data-ttu-id="095aa-106">Il cmdlet **Remove-AzureRmAlertRule** rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="095aa-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="095aa-107">Devi specificare il nome della regola di avviso e il gruppo di risorse a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="095aa-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="095aa-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="095aa-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="095aa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="095aa-109">EXAMPLES</span></span>

### <span data-ttu-id="095aa-110">Esempio 1: rimuovere una regola di avviso</span><span class="sxs-lookup"><span data-stu-id="095aa-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="095aa-111">Questo comando rimuove la regola di avviso denominata Alert-7da64548-214d-42CA-B12B-b245bb8f0ac8 nel gruppo di risorse predefinito-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="095aa-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="095aa-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="095aa-112">PARAMETERS</span></span>

### <span data-ttu-id="095aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095aa-113">-DefaultProfile</span></span>
<span data-ttu-id="095aa-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="095aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="095aa-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="095aa-115">-Name</span></span>
<span data-ttu-id="095aa-116">Specifica il nome della regola di avviso da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="095aa-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="095aa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095aa-117">-ResourceGroupName</span></span>
<span data-ttu-id="095aa-118">Specifica il nome del gruppo di risorse per la regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="095aa-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="095aa-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="095aa-119">-Confirm</span></span>
<span data-ttu-id="095aa-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="095aa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="095aa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="095aa-121">-WhatIf</span></span>
<span data-ttu-id="095aa-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="095aa-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="095aa-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="095aa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="095aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095aa-124">CommonParameters</span></span>
<span data-ttu-id="095aa-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095aa-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095aa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095aa-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="095aa-127">INPUTS</span></span>

### <span data-ttu-id="095aa-128">System. String</span><span class="sxs-lookup"><span data-stu-id="095aa-128">System.String</span></span>

## <span data-ttu-id="095aa-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="095aa-129">OUTPUTS</span></span>

### <span data-ttu-id="095aa-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="095aa-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="095aa-131">Note</span><span class="sxs-lookup"><span data-stu-id="095aa-131">NOTES</span></span>

## <span data-ttu-id="095aa-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="095aa-132">RELATED LINKS</span></span>

[<span data-ttu-id="095aa-133">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="095aa-133">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="095aa-134">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="095aa-134">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="095aa-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="095aa-135">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="095aa-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="095aa-136">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


