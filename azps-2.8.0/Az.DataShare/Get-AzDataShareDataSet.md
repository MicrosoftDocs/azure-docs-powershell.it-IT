---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 0c591a60e1a7b1a5b5d20e7a4747bc8c08389816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674699"
---
# <span data-ttu-id="92757-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="92757-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="92757-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92757-102">SYNOPSIS</span></span>
<span data-ttu-id="92757-103">Ottiene informazioni sui set di dati in Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="92757-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="92757-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92757-104">SYNTAX</span></span>

### <span data-ttu-id="92757-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92757-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92757-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92757-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92757-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92757-107">DESCRIPTION</span></span>
<span data-ttu-id="92757-108">Il cmdlet **Get-AzDataShareDataSet** ottiene le informazioni sui set di dati aggiunti in una condivisione in un account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="92757-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="92757-109">Se specifichi il nome del set di dati, questo cmdlet recupera le informazioni sul set di dati.</span><span class="sxs-lookup"><span data-stu-id="92757-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="92757-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i set di dati in una condivisione. Ho</span><span class="sxs-lookup"><span data-stu-id="92757-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="92757-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92757-111">EXAMPLES</span></span>

### <span data-ttu-id="92757-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92757-112">Example 1</span></span>
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

<span data-ttu-id="92757-113">Questo comando Visualizza le informazioni relative al set di dati AdsDataSet in Condividi AdsShare in Azure Data Share account WikiAdsAccount e gli annunci di gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="92757-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="92757-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92757-114">PARAMETERS</span></span>

### <span data-ttu-id="92757-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="92757-115">-AccountName</span></span>
<span data-ttu-id="92757-116">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="92757-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="92757-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92757-117">-DefaultProfile</span></span>
<span data-ttu-id="92757-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92757-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92757-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="92757-119">-Name</span></span>
<span data-ttu-id="92757-120">Nome del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="92757-120">Azure data set name.</span></span>

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

### <span data-ttu-id="92757-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92757-121">-ResourceGroupName</span></span>
<span data-ttu-id="92757-122">Nome del gruppo di risorse dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="92757-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="92757-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92757-123">-ResourceId</span></span>
<span data-ttu-id="92757-124">ID risorsa del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="92757-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="92757-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="92757-125">-ShareName</span></span>
<span data-ttu-id="92757-126">Nome della condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="92757-126">Azure data share name.</span></span>

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

### <span data-ttu-id="92757-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92757-127">CommonParameters</span></span>
<span data-ttu-id="92757-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92757-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92757-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92757-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92757-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92757-130">INPUTS</span></span>

### <span data-ttu-id="92757-131">System. String</span><span class="sxs-lookup"><span data-stu-id="92757-131">System.String</span></span>

## <span data-ttu-id="92757-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92757-132">OUTPUTS</span></span>

### <span data-ttu-id="92757-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="92757-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="92757-134">Note</span><span class="sxs-lookup"><span data-stu-id="92757-134">NOTES</span></span>

## <span data-ttu-id="92757-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92757-135">RELATED LINKS</span></span>
