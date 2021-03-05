---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: dcd44f9b43184ffc36d58bd5b65a065d7e81b4b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964781"
---
# <span data-ttu-id="e2d16-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2d16-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="e2d16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2d16-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d16-103">Ottiene informazioni su un account di Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e2d16-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e2d16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2d16-104">SYNTAX</span></span>

### <span data-ttu-id="e2d16-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2d16-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2d16-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2d16-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2d16-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="e2d16-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2d16-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e2d16-108">DESCRIPTION</span></span>
<span data-ttu-id="e2d16-109">Il cmdlet **Get-AzDataLakeAnalyticsAccount** ottiene informazioni su un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e2d16-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e2d16-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2d16-110">EXAMPLES</span></span>

### <span data-ttu-id="e2d16-111">Esempio 1: Ottenere informazioni su un account Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="e2d16-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="e2d16-112">Questo comando recupera informazioni sull'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="e2d16-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="e2d16-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2d16-113">PARAMETERS</span></span>

### <span data-ttu-id="e2d16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d16-114">-DefaultProfile</span></span>
<span data-ttu-id="e2d16-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e2d16-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2d16-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e2d16-116">-Name</span></span>
<span data-ttu-id="e2d16-117">Specifica il nome dell'account di Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e2d16-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d16-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d16-118">-ResourceGroupName</span></span>
<span data-ttu-id="e2d16-119">Specifica il nome del gruppo di risorse dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e2d16-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d16-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d16-120">CommonParameters</span></span>
<span data-ttu-id="e2d16-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d16-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d16-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d16-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d16-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="e2d16-123">INPUTS</span></span>

### <span data-ttu-id="e2d16-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e2d16-124">System.String</span></span>

## <span data-ttu-id="e2d16-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2d16-125">OUTPUTS</span></span>

### <span data-ttu-id="e2d16-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2d16-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="e2d16-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="e2d16-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="e2d16-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="e2d16-128">NOTES</span></span>

## <span data-ttu-id="e2d16-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2d16-129">RELATED LINKS</span></span>

[<span data-ttu-id="e2d16-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2d16-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e2d16-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2d16-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e2d16-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2d16-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e2d16-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2d16-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


