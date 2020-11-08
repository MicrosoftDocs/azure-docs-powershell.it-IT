---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033138"
---
# <span data-ttu-id="4e184-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="4e184-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="4e184-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e184-102">SYNOPSIS</span></span>
<span data-ttu-id="4e184-103">Ottiene informazioni sui set di dati di origine nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="4e184-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="4e184-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e184-104">SYNTAX</span></span>

### <span data-ttu-id="4e184-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e184-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e184-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e184-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e184-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e184-107">DESCRIPTION</span></span>
<span data-ttu-id="4e184-108">Il cmdlet **Get-AzDataShareSourceDataSet** fornisce informazioni sui set di dati di origine nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="4e184-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="4e184-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e184-109">EXAMPLES</span></span>

### <span data-ttu-id="4e184-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e184-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="4e184-111">Ottiene i DataSet disponibili nella condivisione di origine</span><span class="sxs-lookup"><span data-stu-id="4e184-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="4e184-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e184-112">PARAMETERS</span></span>

### <span data-ttu-id="4e184-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4e184-113">-AccountName</span></span>
<span data-ttu-id="4e184-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="4e184-114">Azure data share account name</span></span>

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

### <span data-ttu-id="4e184-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e184-115">-DefaultProfile</span></span>
<span data-ttu-id="4e184-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e184-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e184-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e184-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e184-118">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="4e184-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4e184-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4e184-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="4e184-120">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="4e184-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="4e184-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="4e184-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="4e184-122">ID risorsa di abbonamento a Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="4e184-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="4e184-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e184-123">CommonParameters</span></span>
<span data-ttu-id="4e184-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e184-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e184-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e184-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e184-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e184-126">INPUTS</span></span>

### <span data-ttu-id="4e184-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4e184-127">System.String</span></span>

## <span data-ttu-id="4e184-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e184-128">OUTPUTS</span></span>

### <span data-ttu-id="4e184-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="4e184-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="4e184-130">Note</span><span class="sxs-lookup"><span data-stu-id="4e184-130">NOTES</span></span>

## <span data-ttu-id="4e184-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e184-131">RELATED LINKS</span></span>
