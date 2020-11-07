---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: d19825fea43e8fc029e960a513d1c2ad306a8406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674700"
---
# <span data-ttu-id="54e76-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="54e76-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="54e76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54e76-102">SYNOPSIS</span></span>
<span data-ttu-id="54e76-103">Ottiene informazioni sui mapping dei DataSet nell'abbonamento alla condivisione</span><span class="sxs-lookup"><span data-stu-id="54e76-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="54e76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54e76-104">SYNTAX</span></span>

### <span data-ttu-id="54e76-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54e76-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54e76-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54e76-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54e76-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54e76-107">DESCRIPTION</span></span>
<span data-ttu-id="54e76-108">Il cmdlet **Get-AzDataShareDataSetMapping** ottiene le informazioni su un particolare mapping del set di dati se il nome è specificato.</span><span class="sxs-lookup"><span data-stu-id="54e76-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="54e76-109">In caso contrario, riceverà informazioni su tutti i mapping del set di dati in un abbonamento di condivisione.</span><span class="sxs-lookup"><span data-stu-id="54e76-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="54e76-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54e76-110">EXAMPLES</span></span>

### <span data-ttu-id="54e76-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="54e76-111">Example 1</span></span>
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

 <span data-ttu-id="54e76-112">Questo comando Visualizza le informazioni su tutti i mapping del DataSet nell'abbonamento di condivisione.</span><span class="sxs-lookup"><span data-stu-id="54e76-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="54e76-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54e76-113">PARAMETERS</span></span>

### <span data-ttu-id="54e76-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54e76-114">-AccountName</span></span>
<span data-ttu-id="54e76-115">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="54e76-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="54e76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e76-116">-DefaultProfile</span></span>
<span data-ttu-id="54e76-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54e76-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54e76-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="54e76-118">-Name</span></span>
<span data-ttu-id="54e76-119">Nome del mapping set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="54e76-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="54e76-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e76-120">-ResourceGroupName</span></span>
<span data-ttu-id="54e76-121">Nome del gruppo di risorse di Azure Data Share account.</span><span class="sxs-lookup"><span data-stu-id="54e76-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="54e76-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54e76-122">-ResourceId</span></span>
<span data-ttu-id="54e76-123">ID risorsa del mapping del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="54e76-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="54e76-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="54e76-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="54e76-125">Nome dell'abbonamento a condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="54e76-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="54e76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e76-126">CommonParameters</span></span>
<span data-ttu-id="54e76-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e76-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e76-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e76-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54e76-129">INPUTS</span></span>

### <span data-ttu-id="54e76-130">System. String</span><span class="sxs-lookup"><span data-stu-id="54e76-130">System.String</span></span>

## <span data-ttu-id="54e76-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54e76-131">OUTPUTS</span></span>

### <span data-ttu-id="54e76-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="54e76-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="54e76-133">Note</span><span class="sxs-lookup"><span data-stu-id="54e76-133">NOTES</span></span>

## <span data-ttu-id="54e76-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54e76-134">RELATED LINKS</span></span>