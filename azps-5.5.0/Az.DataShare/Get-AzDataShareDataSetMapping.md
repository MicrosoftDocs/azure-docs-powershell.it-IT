---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: 99f80aa920a402867b6385a3b4ef7ac118838f80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198798"
---
# <span data-ttu-id="50217-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="50217-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="50217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50217-102">SYNOPSIS</span></span>
<span data-ttu-id="50217-103">Ottiene informazioni sui mapping del set di dati nell'abbonamento alla condivisione</span><span class="sxs-lookup"><span data-stu-id="50217-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="50217-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50217-104">SYNTAX</span></span>

### <span data-ttu-id="50217-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50217-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50217-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50217-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50217-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50217-107">DESCRIPTION</span></span>
<span data-ttu-id="50217-108">Se si specifica il nome, il cmdlet **Get-AzDataShareDataSetMapping ottiene** informazioni su uno specifico mapping del set di dati.</span><span class="sxs-lookup"><span data-stu-id="50217-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="50217-109">In caso contrario, riceverà informazioni su tutti i mapping di set di dati in una sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="50217-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="50217-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50217-110">EXAMPLES</span></span>

### <span data-ttu-id="50217-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50217-111">Example 1</span></span>
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

 <span data-ttu-id="50217-112">Questo comando visualizza informazioni su tutti i mapping di set di dati nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="50217-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="50217-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50217-113">PARAMETERS</span></span>

### <span data-ttu-id="50217-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="50217-114">-AccountName</span></span>
<span data-ttu-id="50217-115">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="50217-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="50217-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50217-116">-DefaultProfile</span></span>
<span data-ttu-id="50217-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50217-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50217-118">-Name</span><span class="sxs-lookup"><span data-stu-id="50217-118">-Name</span></span>
<span data-ttu-id="50217-119">Nome mapping set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="50217-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="50217-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50217-120">-ResourceGroupName</span></span>
<span data-ttu-id="50217-121">Nome del gruppo di risorse dell'account azure data share.</span><span class="sxs-lookup"><span data-stu-id="50217-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="50217-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50217-122">-ResourceId</span></span>
<span data-ttu-id="50217-123">ID risorsa del mapping del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="50217-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="50217-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="50217-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="50217-125">Nome della sottoscrizione della condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="50217-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="50217-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50217-126">CommonParameters</span></span>
<span data-ttu-id="50217-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50217-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50217-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50217-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50217-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="50217-129">INPUTS</span></span>

### <span data-ttu-id="50217-130">System.String</span><span class="sxs-lookup"><span data-stu-id="50217-130">System.String</span></span>

## <span data-ttu-id="50217-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50217-131">OUTPUTS</span></span>

### <span data-ttu-id="50217-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="50217-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="50217-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="50217-133">NOTES</span></span>

## <span data-ttu-id="50217-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50217-134">RELATED LINKS</span></span>
