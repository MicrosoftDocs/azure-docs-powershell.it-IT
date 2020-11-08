---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: cda879a29d207a3e71d903c02e20129267124414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019123"
---
# <span data-ttu-id="aadb8-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="aadb8-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="aadb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aadb8-102">SYNOPSIS</span></span>
<span data-ttu-id="aadb8-103">Ottiene informazioni sui set di dati di origine nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="aadb8-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="aadb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aadb8-104">SYNTAX</span></span>

### <span data-ttu-id="aadb8-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aadb8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aadb8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aadb8-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aadb8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aadb8-107">DESCRIPTION</span></span>
<span data-ttu-id="aadb8-108">Il cmdlet **Get-AzDataShareSourceDataSet** fornisce informazioni sui set di dati di origine nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="aadb8-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="aadb8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aadb8-109">EXAMPLES</span></span>

### <span data-ttu-id="aadb8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aadb8-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="aadb8-111">Ottiene i DataSet disponibili nella condivisione di origine</span><span class="sxs-lookup"><span data-stu-id="aadb8-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="aadb8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aadb8-112">PARAMETERS</span></span>

### <span data-ttu-id="aadb8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aadb8-113">-AccountName</span></span>
<span data-ttu-id="aadb8-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="aadb8-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aadb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aadb8-115">-DefaultProfile</span></span>
<span data-ttu-id="aadb8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aadb8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aadb8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aadb8-117">-ResourceGroupName</span></span>
<span data-ttu-id="aadb8-118">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="aadb8-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aadb8-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="aadb8-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="aadb8-120">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="aadb8-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aadb8-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="aadb8-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="aadb8-122">ID risorsa di abbonamento a Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="aadb8-122">Azure data share subscription resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadb8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadb8-123">CommonParameters</span></span>
<span data-ttu-id="aadb8-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aadb8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadb8-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aadb8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadb8-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aadb8-126">INPUTS</span></span>

### <span data-ttu-id="aadb8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="aadb8-127">System.String</span></span>

## <span data-ttu-id="aadb8-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aadb8-128">OUTPUTS</span></span>

### <span data-ttu-id="aadb8-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="aadb8-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="aadb8-130">Note</span><span class="sxs-lookup"><span data-stu-id="aadb8-130">NOTES</span></span>

## <span data-ttu-id="aadb8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aadb8-131">RELATED LINKS</span></span>
