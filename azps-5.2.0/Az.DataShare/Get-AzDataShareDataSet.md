---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341176"
---
# <span data-ttu-id="8496a-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8496a-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="8496a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8496a-102">SYNOPSIS</span></span>
<span data-ttu-id="8496a-103">Ottiene informazioni sui set di dati in Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="8496a-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="8496a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8496a-104">SYNTAX</span></span>

### <span data-ttu-id="8496a-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8496a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8496a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8496a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8496a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8496a-107">DESCRIPTION</span></span>
<span data-ttu-id="8496a-108">Il cmdlet **Get-AzDataShareDataSet** ottiene le informazioni sui set di dati aggiunti in una condivisione in un account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="8496a-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="8496a-109">Se specifichi il nome del set di dati, questo cmdlet recupera le informazioni sul set di dati.</span><span class="sxs-lookup"><span data-stu-id="8496a-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="8496a-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i set di dati in una condivisione. Ho</span><span class="sxs-lookup"><span data-stu-id="8496a-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="8496a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8496a-111">EXAMPLES</span></span>

### <span data-ttu-id="8496a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8496a-112">Example 1</span></span>
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

<span data-ttu-id="8496a-113">Questo comando Visualizza le informazioni relative al set di dati AdsDataSet in Condividi AdsShare in Azure Data Share account WikiAdsAccount e gli annunci di gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="8496a-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="8496a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8496a-114">PARAMETERS</span></span>

### <span data-ttu-id="8496a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8496a-115">-AccountName</span></span>
<span data-ttu-id="8496a-116">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="8496a-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="8496a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8496a-117">-DefaultProfile</span></span>
<span data-ttu-id="8496a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8496a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8496a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8496a-119">-Name</span></span>
<span data-ttu-id="8496a-120">Nome del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="8496a-120">Azure data set name.</span></span>

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

### <span data-ttu-id="8496a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8496a-121">-ResourceGroupName</span></span>
<span data-ttu-id="8496a-122">Nome del gruppo di risorse dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="8496a-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="8496a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8496a-123">-ResourceId</span></span>
<span data-ttu-id="8496a-124">ID risorsa del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="8496a-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="8496a-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8496a-125">-ShareName</span></span>
<span data-ttu-id="8496a-126">Nome della condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="8496a-126">Azure data share name.</span></span>

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

### <span data-ttu-id="8496a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8496a-127">CommonParameters</span></span>
<span data-ttu-id="8496a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8496a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8496a-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8496a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8496a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8496a-130">INPUTS</span></span>

### <span data-ttu-id="8496a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8496a-131">System.String</span></span>

## <span data-ttu-id="8496a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8496a-132">OUTPUTS</span></span>

### <span data-ttu-id="8496a-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8496a-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="8496a-134">Note</span><span class="sxs-lookup"><span data-stu-id="8496a-134">NOTES</span></span>

## <span data-ttu-id="8496a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8496a-135">RELATED LINKS</span></span>
