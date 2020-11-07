---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685686"
---
# <span data-ttu-id="d2886-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2886-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d2886-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2886-102">SYNOPSIS</span></span>
<span data-ttu-id="d2886-103">Ottiene informazioni su un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d2886-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2886-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2886-104">SYNTAX</span></span>

### <span data-ttu-id="d2886-105">Tutti in abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2886-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2886-106">Tutti nel gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d2886-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2886-107">Account specifico</span><span class="sxs-lookup"><span data-stu-id="d2886-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2886-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2886-108">DESCRIPTION</span></span>
<span data-ttu-id="d2886-109">Il cmdlet **Get-AzureRmDataLakeAnalyticsAccount** ottiene le informazioni su un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d2886-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d2886-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2886-110">EXAMPLES</span></span>

### <span data-ttu-id="d2886-111">Esempio 1: ottenere informazioni su un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="d2886-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="d2886-112">Questo comando consente di ottenere informazioni sull'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="d2886-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="d2886-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2886-113">PARAMETERS</span></span>

### <span data-ttu-id="d2886-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2886-114">-Name</span></span>
<span data-ttu-id="d2886-115">Specifica il nome dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d2886-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2886-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2886-116">-ResourceGroupName</span></span>
<span data-ttu-id="d2886-117">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d2886-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2886-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2886-118">-DefaultProfile</span></span>
<span data-ttu-id="d2886-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2886-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2886-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2886-120">CommonParameters</span></span>
<span data-ttu-id="d2886-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2886-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2886-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2886-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2886-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2886-123">INPUTS</span></span>

## <span data-ttu-id="d2886-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2886-124">OUTPUTS</span></span>

### <span data-ttu-id="d2886-125">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2886-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="d2886-126">Dettagli dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="d2886-126">The specified account details.</span></span>

### <span data-ttu-id="d2886-127">Elenco<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="d2886-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="d2886-128">Elenco di account nel gruppo di risorse o nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="d2886-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="d2886-129">Note</span><span class="sxs-lookup"><span data-stu-id="d2886-129">NOTES</span></span>

## <span data-ttu-id="d2886-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2886-130">RELATED LINKS</span></span>

[<span data-ttu-id="d2886-131">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2886-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d2886-132">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2886-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d2886-133">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2886-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d2886-134">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2886-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


