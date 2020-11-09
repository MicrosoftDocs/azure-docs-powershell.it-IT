---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298129"
---
# <span data-ttu-id="33e25-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="33e25-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="33e25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33e25-102">SYNOPSIS</span></span>
<span data-ttu-id="33e25-103">Ottiene informazioni su un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="33e25-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="33e25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33e25-104">SYNTAX</span></span>

### <span data-ttu-id="33e25-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33e25-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33e25-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="33e25-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33e25-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="33e25-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33e25-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33e25-108">DESCRIPTION</span></span>
<span data-ttu-id="33e25-109">Il cmdlet **Get-AzDataLakeAnalyticsAccount** ottiene le informazioni su un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="33e25-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="33e25-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33e25-110">EXAMPLES</span></span>

### <span data-ttu-id="33e25-111">Esempio 1: ottenere informazioni su un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="33e25-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="33e25-112">Questo comando consente di ottenere informazioni sull'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="33e25-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="33e25-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33e25-113">PARAMETERS</span></span>

### <span data-ttu-id="33e25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e25-114">-DefaultProfile</span></span>
<span data-ttu-id="33e25-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="33e25-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33e25-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="33e25-116">-Name</span></span>
<span data-ttu-id="33e25-117">Specifica il nome dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="33e25-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="33e25-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e25-118">-ResourceGroupName</span></span>
<span data-ttu-id="33e25-119">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="33e25-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="33e25-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e25-120">CommonParameters</span></span>
<span data-ttu-id="33e25-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33e25-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e25-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e25-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e25-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33e25-123">INPUTS</span></span>

### <span data-ttu-id="33e25-124">System. String</span><span class="sxs-lookup"><span data-stu-id="33e25-124">System.String</span></span>

## <span data-ttu-id="33e25-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33e25-125">OUTPUTS</span></span>

### <span data-ttu-id="33e25-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="33e25-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="33e25-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="33e25-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="33e25-128">Note</span><span class="sxs-lookup"><span data-stu-id="33e25-128">NOTES</span></span>

## <span data-ttu-id="33e25-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33e25-129">RELATED LINKS</span></span>

[<span data-ttu-id="33e25-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="33e25-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="33e25-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="33e25-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="33e25-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="33e25-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="33e25-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="33e25-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


