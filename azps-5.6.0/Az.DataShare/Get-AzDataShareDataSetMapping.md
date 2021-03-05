---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: a25efdd89e99e52115ade8354d7e96f8ee7972ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991380"
---
# <span data-ttu-id="75ee2-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="75ee2-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="75ee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="75ee2-103">Ottiene informazioni sui mapping del set di dati nell'abbonamento alla condivisione</span><span class="sxs-lookup"><span data-stu-id="75ee2-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="75ee2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75ee2-104">SYNTAX</span></span>

### <span data-ttu-id="75ee2-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75ee2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75ee2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75ee2-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75ee2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75ee2-107">DESCRIPTION</span></span>
<span data-ttu-id="75ee2-108">Se si specifica il nome, il cmdlet **Get-AzDataShareDataSetMapping ottiene** informazioni su uno specifico mapping del set di dati.</span><span class="sxs-lookup"><span data-stu-id="75ee2-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="75ee2-109">In caso contrario, riceve informazioni su tutti i mapping di set di dati in una sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="75ee2-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="75ee2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75ee2-110">EXAMPLES</span></span>

### <span data-ttu-id="75ee2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75ee2-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="75ee2-112">Questo comando visualizza informazioni su tutti i mapping di set di dati nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="75ee2-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="75ee2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75ee2-113">PARAMETERS</span></span>

### <span data-ttu-id="75ee2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75ee2-114">-AccountName</span></span>
<span data-ttu-id="75ee2-115">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="75ee2-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="75ee2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ee2-116">-DefaultProfile</span></span>
<span data-ttu-id="75ee2-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75ee2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75ee2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="75ee2-118">-Name</span></span>
<span data-ttu-id="75ee2-119">Nome mapping set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="75ee2-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="75ee2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ee2-120">-ResourceGroupName</span></span>
<span data-ttu-id="75ee2-121">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="75ee2-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="75ee2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75ee2-122">-ResourceId</span></span>
<span data-ttu-id="75ee2-123">ID risorsa del mapping del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="75ee2-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="75ee2-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="75ee2-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="75ee2-125">Nome della sottoscrizione della condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="75ee2-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="75ee2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ee2-126">CommonParameters</span></span>
<span data-ttu-id="75ee2-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ee2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ee2-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75ee2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ee2-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="75ee2-129">INPUTS</span></span>

### <span data-ttu-id="75ee2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="75ee2-130">System.String</span></span>

## <span data-ttu-id="75ee2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75ee2-131">OUTPUTS</span></span>

### <span data-ttu-id="75ee2-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="75ee2-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="75ee2-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="75ee2-133">NOTES</span></span>

## <span data-ttu-id="75ee2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75ee2-134">RELATED LINKS</span></span>
