---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033172"
---
# <span data-ttu-id="b2520-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2520-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="b2520-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2520-102">SYNOPSIS</span></span>
<span data-ttu-id="b2520-103">Ottiene informazioni su un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="b2520-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="b2520-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2520-104">SYNTAX</span></span>

### <span data-ttu-id="b2520-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2520-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2520-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b2520-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2520-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="b2520-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2520-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2520-108">DESCRIPTION</span></span>
<span data-ttu-id="b2520-109">Il cmdlet **Get-AzDataLakeAnalyticsAccount** ottiene le informazioni su un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="b2520-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="b2520-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2520-110">EXAMPLES</span></span>

### <span data-ttu-id="b2520-111">Esempio 1: ottenere informazioni su un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="b2520-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="b2520-112">Questo comando consente di ottenere informazioni sull'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="b2520-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="b2520-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2520-113">PARAMETERS</span></span>

### <span data-ttu-id="b2520-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2520-114">-DefaultProfile</span></span>
<span data-ttu-id="b2520-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b2520-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2520-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2520-116">-Name</span></span>
<span data-ttu-id="b2520-117">Specifica il nome dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="b2520-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="b2520-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2520-118">-ResourceGroupName</span></span>
<span data-ttu-id="b2520-119">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="b2520-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="b2520-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2520-120">CommonParameters</span></span>
<span data-ttu-id="b2520-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2520-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2520-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2520-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2520-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2520-123">INPUTS</span></span>

### <span data-ttu-id="b2520-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b2520-124">System.String</span></span>

## <span data-ttu-id="b2520-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2520-125">OUTPUTS</span></span>

### <span data-ttu-id="b2520-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2520-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="b2520-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="b2520-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="b2520-128">Note</span><span class="sxs-lookup"><span data-stu-id="b2520-128">NOTES</span></span>

## <span data-ttu-id="b2520-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2520-129">RELATED LINKS</span></span>

[<span data-ttu-id="b2520-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2520-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b2520-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2520-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b2520-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2520-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b2520-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b2520-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


