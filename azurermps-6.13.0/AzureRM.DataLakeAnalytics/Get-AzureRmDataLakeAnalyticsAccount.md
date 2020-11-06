---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 32c7478e7e2419a8f83c839efd841f25446a96c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511760"
---
# <span data-ttu-id="4c2bf-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4c2bf-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="4c2bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="4c2bf-103">Ottiene informazioni su un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="4c2bf-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c2bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c2bf-104">SYNTAX</span></span>

### <span data-ttu-id="4c2bf-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c2bf-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c2bf-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4c2bf-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c2bf-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="4c2bf-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c2bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c2bf-108">DESCRIPTION</span></span>
<span data-ttu-id="4c2bf-109">Il cmdlet **Get-AzureRmDataLakeAnalyticsAccount** ottiene le informazioni su un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4c2bf-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4c2bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c2bf-110">EXAMPLES</span></span>

### <span data-ttu-id="4c2bf-111">Esempio 1: ottenere informazioni su un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="4c2bf-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="4c2bf-112">Questo comando consente di ottenere informazioni sull'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="4c2bf-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="4c2bf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c2bf-113">PARAMETERS</span></span>

### <span data-ttu-id="4c2bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c2bf-114">-DefaultProfile</span></span>
<span data-ttu-id="4c2bf-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4c2bf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c2bf-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c2bf-116">-Name</span></span>
<span data-ttu-id="4c2bf-117">Specifica il nome dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="4c2bf-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="4c2bf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c2bf-118">-ResourceGroupName</span></span>
<span data-ttu-id="4c2bf-119">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="4c2bf-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="4c2bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c2bf-120">CommonParameters</span></span>
<span data-ttu-id="4c2bf-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c2bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c2bf-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c2bf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c2bf-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c2bf-123">INPUTS</span></span>

### <span data-ttu-id="4c2bf-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4c2bf-124">System.String</span></span>

## <span data-ttu-id="4c2bf-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c2bf-125">OUTPUTS</span></span>

### <span data-ttu-id="4c2bf-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4c2bf-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="4c2bf-127">Note</span><span class="sxs-lookup"><span data-stu-id="4c2bf-127">NOTES</span></span>

## <span data-ttu-id="4c2bf-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c2bf-128">RELATED LINKS</span></span>

[<span data-ttu-id="4c2bf-129">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4c2bf-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4c2bf-130">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4c2bf-130">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4c2bf-131">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4c2bf-131">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4c2bf-132">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4c2bf-132">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


