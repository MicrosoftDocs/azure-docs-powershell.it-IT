---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 73272c2afd0b3d8ef62a522f2e67f04854c2232e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018923"
---
# <span data-ttu-id="76ebf-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="76ebf-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="76ebf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="76ebf-103">Ottiene informazioni sui set di dati in Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="76ebf-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="76ebf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76ebf-104">SYNTAX</span></span>

### <span data-ttu-id="76ebf-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76ebf-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76ebf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76ebf-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ebf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76ebf-107">DESCRIPTION</span></span>
<span data-ttu-id="76ebf-108">Il cmdlet **Get-AzDataShareDataSet** ottiene le informazioni sui set di dati aggiunti in una condivisione in un account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="76ebf-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="76ebf-109">Se specifichi il nome del set di dati, questo cmdlet recupera le informazioni sul set di dati.</span><span class="sxs-lookup"><span data-stu-id="76ebf-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="76ebf-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i set di dati in una condivisione. Ho</span><span class="sxs-lookup"><span data-stu-id="76ebf-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="76ebf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76ebf-111">EXAMPLES</span></span>

### <span data-ttu-id="76ebf-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76ebf-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="76ebf-113">Questo comando Visualizza le informazioni relative al set di dati AdsDataSet in Condividi AdsShare in Azure Data Share account WikiAdsAccount e gli annunci di gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="76ebf-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="76ebf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76ebf-114">PARAMETERS</span></span>

### <span data-ttu-id="76ebf-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76ebf-115">-AccountName</span></span>
<span data-ttu-id="76ebf-116">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="76ebf-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="76ebf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ebf-117">-DefaultProfile</span></span>
<span data-ttu-id="76ebf-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76ebf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76ebf-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="76ebf-119">-Name</span></span>
<span data-ttu-id="76ebf-120">Nome del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="76ebf-120">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ebf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76ebf-121">-ResourceGroupName</span></span>
<span data-ttu-id="76ebf-122">Nome del gruppo di risorse dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="76ebf-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="76ebf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76ebf-123">-ResourceId</span></span>
<span data-ttu-id="76ebf-124">ID risorsa del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="76ebf-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="76ebf-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="76ebf-125">-ShareName</span></span>
<span data-ttu-id="76ebf-126">Nome della condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="76ebf-126">Azure data share name.</span></span>

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

### <span data-ttu-id="76ebf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ebf-127">CommonParameters</span></span>
<span data-ttu-id="76ebf-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ebf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ebf-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ebf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ebf-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76ebf-130">INPUTS</span></span>

### <span data-ttu-id="76ebf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="76ebf-131">System.String</span></span>

## <span data-ttu-id="76ebf-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76ebf-132">OUTPUTS</span></span>

### <span data-ttu-id="76ebf-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="76ebf-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="76ebf-134">Note</span><span class="sxs-lookup"><span data-stu-id="76ebf-134">NOTES</span></span>

## <span data-ttu-id="76ebf-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76ebf-135">RELATED LINKS</span></span>
