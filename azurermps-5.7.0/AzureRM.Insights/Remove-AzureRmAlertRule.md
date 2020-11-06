---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: eaa7cfa9f58bb9bb5affa7a035d194910bcf0006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512604"
---
# <span data-ttu-id="a12f6-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a12f6-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="a12f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a12f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a12f6-103">Rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="a12f6-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a12f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a12f6-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a12f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a12f6-105">DESCRIPTION</span></span>
<span data-ttu-id="a12f6-106">Il cmdlet **Remove-AzureRmAlertRule** rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="a12f6-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="a12f6-107">Devi specificare il nome della regola di avviso e il gruppo di risorse a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="a12f6-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

<span data-ttu-id="a12f6-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a12f6-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a12f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a12f6-109">EXAMPLES</span></span>

### <span data-ttu-id="a12f6-110">Esempio 1: rimuovere una regola di avviso</span><span class="sxs-lookup"><span data-stu-id="a12f6-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="a12f6-111">Questo comando rimuove la regola di avviso denominata Alert-7da64548-214d-42CA-B12B-b245bb8f0ac8 nel gruppo di risorse predefinito-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="a12f6-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="a12f6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a12f6-112">PARAMETERS</span></span>

### <span data-ttu-id="a12f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12f6-113">-DefaultProfile</span></span>
<span data-ttu-id="a12f6-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a12f6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a12f6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a12f6-115">-Name</span></span>
<span data-ttu-id="a12f6-116">Specifica il nome della regola di avviso da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a12f6-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a12f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a12f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="a12f6-118">Specifica il nome del gruppo di risorse per la regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="a12f6-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a12f6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12f6-119">CommonParameters</span></span>
<span data-ttu-id="a12f6-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a12f6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12f6-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a12f6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12f6-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a12f6-122">INPUTS</span></span>

### <span data-ttu-id="a12f6-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a12f6-123">None</span></span>
<span data-ttu-id="a12f6-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a12f6-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a12f6-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a12f6-125">OUTPUTS</span></span>

### <span data-ttu-id="a12f6-126">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a12f6-126">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="a12f6-127">Note</span><span class="sxs-lookup"><span data-stu-id="a12f6-127">NOTES</span></span>

## <span data-ttu-id="a12f6-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a12f6-128">RELATED LINKS</span></span>

[<span data-ttu-id="a12f6-129">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a12f6-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="a12f6-130">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a12f6-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="a12f6-131">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="a12f6-131">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="a12f6-132">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a12f6-132">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


