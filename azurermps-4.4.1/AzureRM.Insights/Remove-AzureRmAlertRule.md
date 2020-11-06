---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520083"
---
# <span data-ttu-id="677b7-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="677b7-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="677b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="677b7-102">SYNOPSIS</span></span>
<span data-ttu-id="677b7-103">Rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="677b7-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="677b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="677b7-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="677b7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="677b7-105">DESCRIPTION</span></span>
<span data-ttu-id="677b7-106">Il cmdlet **Remove-AzureRmAlertRule** rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="677b7-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="677b7-107">Devi specificare il nome della regola di avviso e il gruppo di risorse a cui è assegnato.</span><span class="sxs-lookup"><span data-stu-id="677b7-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

## <span data-ttu-id="677b7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="677b7-108">EXAMPLES</span></span>

### <span data-ttu-id="677b7-109">Esempio 1: rimuovere una regola di avviso</span><span class="sxs-lookup"><span data-stu-id="677b7-109">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="677b7-110">Questo comando rimuove la regola di avviso denominata Alert-7da64548-214d-42CA-B12B-b245bb8f0ac8 nel gruppo di risorse predefinito-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="677b7-110">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="677b7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="677b7-111">PARAMETERS</span></span>

### <span data-ttu-id="677b7-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="677b7-112">-Name</span></span>
<span data-ttu-id="677b7-113">Specifica il nome della regola di avviso da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="677b7-113">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="677b7-114">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="677b7-114">-ResourceGroup</span></span>
<span data-ttu-id="677b7-115">Specifica il nome del gruppo di risorse per la regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="677b7-115">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="677b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677b7-116">-DefaultProfile</span></span>
<span data-ttu-id="677b7-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="677b7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="677b7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677b7-118">CommonParameters</span></span>
<span data-ttu-id="677b7-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677b7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677b7-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="677b7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677b7-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="677b7-121">INPUTS</span></span>

## <span data-ttu-id="677b7-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="677b7-122">OUTPUTS</span></span>

### <span data-ttu-id="677b7-123">System. Collections. Generic. list ' 1 [Microsoft. Azure. AzureOperationResponse]</span><span class="sxs-lookup"><span data-stu-id="677b7-123">System.Collections.Generic.List\`1[Microsoft.Azure.AzureOperationResponse]</span></span>

## <span data-ttu-id="677b7-124">Note</span><span class="sxs-lookup"><span data-stu-id="677b7-124">NOTES</span></span>

## <span data-ttu-id="677b7-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="677b7-125">RELATED LINKS</span></span>

[<span data-ttu-id="677b7-126">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="677b7-126">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="677b7-127">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="677b7-127">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="677b7-128">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="677b7-128">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="677b7-129">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="677b7-129">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="677b7-130">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="677b7-130">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


