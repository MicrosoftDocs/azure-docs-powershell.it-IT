---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 97a72b9dbeb50d1710625f7a6142151834a84d92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012206"
---
# <span data-ttu-id="7f212-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="7f212-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="7f212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f212-102">SYNOPSIS</span></span>
<span data-ttu-id="7f212-103">Ottiene informazioni sui set di dati di origine nella sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="7f212-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="7f212-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f212-104">SYNTAX</span></span>

### <span data-ttu-id="7f212-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f212-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f212-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f212-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f212-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7f212-107">DESCRIPTION</span></span>
<span data-ttu-id="7f212-108">Il cmdlet **Get-AzDataShareSourceDataSet** fornisce informazioni sui set di dati di origine nella sottoscrizione della condivisione.</span><span class="sxs-lookup"><span data-stu-id="7f212-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="7f212-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f212-109">EXAMPLES</span></span>

### <span data-ttu-id="7f212-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7f212-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="7f212-111">Recupera i set di dati disponibili nella condivisione di origine</span><span class="sxs-lookup"><span data-stu-id="7f212-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="7f212-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f212-112">PARAMETERS</span></span>

### <span data-ttu-id="7f212-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7f212-113">-AccountName</span></span>
<span data-ttu-id="7f212-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7f212-114">Azure data share account name</span></span>

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

### <span data-ttu-id="7f212-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f212-115">-DefaultProfile</span></span>
<span data-ttu-id="7f212-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f212-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f212-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f212-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f212-118">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7f212-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="7f212-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7f212-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="7f212-120">Nome della sottoscrizione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7f212-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="7f212-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="7f212-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="7f212-122">ID risorsa sottoscrizione condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7f212-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="7f212-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f212-123">CommonParameters</span></span>
<span data-ttu-id="7f212-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f212-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f212-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7f212-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f212-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="7f212-126">INPUTS</span></span>

### <span data-ttu-id="7f212-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7f212-127">System.String</span></span>

## <span data-ttu-id="7f212-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f212-128">OUTPUTS</span></span>

### <span data-ttu-id="7f212-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="7f212-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="7f212-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="7f212-130">NOTES</span></span>

## <span data-ttu-id="7f212-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f212-131">RELATED LINKS</span></span>
