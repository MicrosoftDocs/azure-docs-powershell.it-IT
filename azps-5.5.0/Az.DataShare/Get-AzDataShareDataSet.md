---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177055"
---
# <span data-ttu-id="aad51-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="aad51-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="aad51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad51-102">SYNOPSIS</span></span>
<span data-ttu-id="aad51-103">Recupera informazioni sui set di dati nella condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="aad51-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="aad51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aad51-104">SYNTAX</span></span>

### <span data-ttu-id="aad51-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aad51-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aad51-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aad51-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aad51-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aad51-107">DESCRIPTION</span></span>
<span data-ttu-id="aad51-108">Il cmdlet **Get-AzDataShareDataSet** ottiene informazioni sui set di dati aggiunti in una condivisione in un account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="aad51-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="aad51-109">Se si specifica il nome del set di dati, questo cmdlet ottiene informazioni sul set di dati.</span><span class="sxs-lookup"><span data-stu-id="aad51-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="aad51-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i set di dati in una condivisione. I</span><span class="sxs-lookup"><span data-stu-id="aad51-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="aad51-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aad51-111">EXAMPLES</span></span>

### <span data-ttu-id="aad51-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aad51-112">Example 1</span></span>
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

<span data-ttu-id="aad51-113">Questo comando visualizza informazioni sul set di dati AdsDataSet in Share AdsShare nell'account wikiAdsAccount per la condivisione di dati di Azure e nel gruppo di risorse ADS.</span><span class="sxs-lookup"><span data-stu-id="aad51-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="aad51-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aad51-114">PARAMETERS</span></span>

### <span data-ttu-id="aad51-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aad51-115">-AccountName</span></span>
<span data-ttu-id="aad51-116">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="aad51-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="aad51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad51-117">-DefaultProfile</span></span>
<span data-ttu-id="aad51-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aad51-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aad51-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aad51-119">-Name</span></span>
<span data-ttu-id="aad51-120">Nome del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="aad51-120">Azure data set name.</span></span>

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

### <span data-ttu-id="aad51-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad51-121">-ResourceGroupName</span></span>
<span data-ttu-id="aad51-122">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="aad51-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="aad51-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aad51-123">-ResourceId</span></span>
<span data-ttu-id="aad51-124">ID della risorsa del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="aad51-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="aad51-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="aad51-125">-ShareName</span></span>
<span data-ttu-id="aad51-126">Nome della condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="aad51-126">Azure data share name.</span></span>

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

### <span data-ttu-id="aad51-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad51-127">CommonParameters</span></span>
<span data-ttu-id="aad51-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad51-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad51-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aad51-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad51-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="aad51-130">INPUTS</span></span>

### <span data-ttu-id="aad51-131">System.String</span><span class="sxs-lookup"><span data-stu-id="aad51-131">System.String</span></span>

## <span data-ttu-id="aad51-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aad51-132">OUTPUTS</span></span>

### <span data-ttu-id="aad51-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="aad51-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="aad51-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="aad51-134">NOTES</span></span>

## <span data-ttu-id="aad51-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aad51-135">RELATED LINKS</span></span>
