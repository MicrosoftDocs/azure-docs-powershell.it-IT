---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a6e147d64a1dea77febc833b5c46e78d070f3ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509891"
---
# <span data-ttu-id="f0123-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f0123-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f0123-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0123-102">SYNOPSIS</span></span>
<span data-ttu-id="f0123-103">Controlla l'esistenza di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="f0123-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0123-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0123-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0123-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0123-105">DESCRIPTION</span></span>
<span data-ttu-id="f0123-106">Il cmdlet **test-AzureRmDataLakeAnalyticsAccount** controlla l'esistenza di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="f0123-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f0123-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0123-107">EXAMPLES</span></span>

### <span data-ttu-id="f0123-108">Esempio 1: verificare se un account esiste</span><span class="sxs-lookup"><span data-stu-id="f0123-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="f0123-109">Questo comando verifica se l'account denominato ContosoAdlAccount esiste.</span><span class="sxs-lookup"><span data-stu-id="f0123-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="f0123-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0123-110">PARAMETERS</span></span>

### <span data-ttu-id="f0123-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0123-111">-DefaultProfile</span></span>
<span data-ttu-id="f0123-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f0123-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0123-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0123-113">-Name</span></span>
<span data-ttu-id="f0123-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="f0123-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0123-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0123-115">-ResourceGroupName</span></span>
<span data-ttu-id="f0123-116">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="f0123-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0123-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0123-117">CommonParameters</span></span>
<span data-ttu-id="f0123-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0123-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0123-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0123-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0123-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0123-120">INPUTS</span></span>

### <span data-ttu-id="f0123-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f0123-121">None</span></span>
<span data-ttu-id="f0123-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f0123-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0123-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0123-123">OUTPUTS</span></span>

### <span data-ttu-id="f0123-124">bool</span><span class="sxs-lookup"><span data-stu-id="f0123-124">bool</span></span>
<span data-ttu-id="f0123-125">Vero o falso che indica se l'account esiste o meno.</span><span class="sxs-lookup"><span data-stu-id="f0123-125">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="f0123-126">Note</span><span class="sxs-lookup"><span data-stu-id="f0123-126">NOTES</span></span>

## <span data-ttu-id="f0123-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0123-127">RELATED LINKS</span></span>

[<span data-ttu-id="f0123-128">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f0123-128">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f0123-129">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f0123-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f0123-130">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f0123-130">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


