---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a4c63e22427e3ae0b666bb7d99b8217a990657c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186119"
---
# <span data-ttu-id="a879f-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="a879f-101">Get-AzDataShare</span></span>

## <span data-ttu-id="a879f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a879f-102">SYNOPSIS</span></span>
<span data-ttu-id="a879f-103">Ottenere informazioni sulle condivisioni dati.</span><span class="sxs-lookup"><span data-stu-id="a879f-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="a879f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a879f-104">SYNTAX</span></span>

### <span data-ttu-id="a879f-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a879f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a879f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a879f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a879f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a879f-107">DESCRIPTION</span></span>
<span data-ttu-id="a879f-108">Il cmdlet **Get-AzDataShare** ottiene informazioni sulle condivisioni dati in una condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a879f-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="a879f-109">Se si specifica il nome di una condivisione dati, questo cmdlet ottiene informazioni sulla condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="a879f-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="a879f-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutte le condivisioni dati in un account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a879f-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="a879f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a879f-111">EXAMPLES</span></span>

### <span data-ttu-id="a879f-112">Esempio 1: Ottenere una condivisione dati specifica</span><span class="sxs-lookup"><span data-stu-id="a879f-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="a879f-113">Questo comando visualizza informazioni sulla condivisione di dati di AdsShare nell'account di condivisione dati WikiAdsAccount di Azure e nel gruppo di risorse ADS.</span><span class="sxs-lookup"><span data-stu-id="a879f-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="a879f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a879f-114">PARAMETERS</span></span>

### <span data-ttu-id="a879f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a879f-115">-AccountName</span></span>
<span data-ttu-id="a879f-116">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a879f-116">Azure data share account name</span></span>

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

### <span data-ttu-id="a879f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a879f-117">-DefaultProfile</span></span>
<span data-ttu-id="a879f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a879f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a879f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a879f-119">-Name</span></span>
<span data-ttu-id="a879f-120">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a879f-120">Azure data share name</span></span>

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

### <span data-ttu-id="a879f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a879f-121">-ResourceGroupName</span></span>
<span data-ttu-id="a879f-122">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a879f-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a879f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a879f-123">-ResourceId</span></span>
<span data-ttu-id="a879f-124">ID risorsa della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a879f-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="a879f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a879f-125">CommonParameters</span></span>
<span data-ttu-id="a879f-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a879f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a879f-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a879f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a879f-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="a879f-128">INPUTS</span></span>

### <span data-ttu-id="a879f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a879f-129">System.String</span></span>

## <span data-ttu-id="a879f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a879f-130">OUTPUTS</span></span>

### <span data-ttu-id="a879f-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="a879f-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="a879f-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="a879f-132">NOTES</span></span>

## <span data-ttu-id="a879f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a879f-133">RELATED LINKS</span></span>
