---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 71d524aeea441c80b90642a01f1a2f34996904ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685842"
---
# <span data-ttu-id="7b17e-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7b17e-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="7b17e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b17e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b17e-103">Ottiene informazioni su un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="7b17e-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b17e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b17e-104">SYNTAX</span></span>

### <span data-ttu-id="7b17e-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b17e-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b17e-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7b17e-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b17e-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="7b17e-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b17e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b17e-108">DESCRIPTION</span></span>
<span data-ttu-id="7b17e-109">Il cmdlet **Get-AzureRmDataLakeAnalyticsAccount** ottiene le informazioni su un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="7b17e-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7b17e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b17e-110">EXAMPLES</span></span>

### <span data-ttu-id="7b17e-111">Esempio 1: ottenere informazioni su un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="7b17e-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="7b17e-112">Questo comando consente di ottenere informazioni sull'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="7b17e-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="7b17e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b17e-113">PARAMETERS</span></span>

### <span data-ttu-id="7b17e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b17e-114">-DefaultProfile</span></span>
<span data-ttu-id="7b17e-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7b17e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b17e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b17e-116">-Name</span></span>
<span data-ttu-id="7b17e-117">Specifica il nome dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="7b17e-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b17e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b17e-118">-ResourceGroupName</span></span>
<span data-ttu-id="7b17e-119">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="7b17e-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b17e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b17e-120">CommonParameters</span></span>
<span data-ttu-id="7b17e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b17e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b17e-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b17e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b17e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b17e-123">INPUTS</span></span>

### <span data-ttu-id="7b17e-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7b17e-124">None</span></span>
<span data-ttu-id="7b17e-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7b17e-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b17e-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b17e-126">OUTPUTS</span></span>

### <span data-ttu-id="7b17e-127">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7b17e-127">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="7b17e-128">Dettagli dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="7b17e-128">The specified account details.</span></span>

### <span data-ttu-id="7b17e-129">Elenco<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="7b17e-129">List<PSDataLakeAnalyticsAccountBasic></span></span>
<span data-ttu-id="7b17e-130">Elenco di account nel gruppo di risorse o nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="7b17e-130">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="7b17e-131">Note</span><span class="sxs-lookup"><span data-stu-id="7b17e-131">NOTES</span></span>

## <span data-ttu-id="7b17e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b17e-132">RELATED LINKS</span></span>

[<span data-ttu-id="7b17e-133">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7b17e-133">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7b17e-134">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7b17e-134">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7b17e-135">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7b17e-135">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7b17e-136">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7b17e-136">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


