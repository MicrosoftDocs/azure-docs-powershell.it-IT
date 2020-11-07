---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: e527501424edfbbc12693b47b5858c3c46592402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686423"
---
# <span data-ttu-id="b7875-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b7875-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="b7875-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7875-102">SYNOPSIS</span></span>
<span data-ttu-id="b7875-103">Controlla l'esistenza di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="b7875-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7875-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7875-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7875-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7875-105">DESCRIPTION</span></span>
<span data-ttu-id="b7875-106">Il cmdlet **test-AzureRmDataLakeAnalyticsAccount** controlla l'esistenza di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="b7875-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="b7875-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7875-107">EXAMPLES</span></span>

### <span data-ttu-id="b7875-108">Esempio 1: verificare se un account esiste</span><span class="sxs-lookup"><span data-stu-id="b7875-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="b7875-109">Questo comando verifica se l'account denominato ContosoAdlAccount esiste.</span><span class="sxs-lookup"><span data-stu-id="b7875-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="b7875-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7875-110">PARAMETERS</span></span>

### <span data-ttu-id="b7875-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7875-111">-DefaultProfile</span></span>
<span data-ttu-id="b7875-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b7875-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7875-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7875-113">-Name</span></span>
<span data-ttu-id="b7875-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="b7875-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7875-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7875-115">-ResourceGroupName</span></span>
<span data-ttu-id="b7875-116">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="b7875-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7875-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7875-117">CommonParameters</span></span>
<span data-ttu-id="b7875-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7875-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7875-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7875-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7875-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7875-120">INPUTS</span></span>

### <span data-ttu-id="b7875-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b7875-121">System.String</span></span>

## <span data-ttu-id="b7875-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7875-122">OUTPUTS</span></span>

### <span data-ttu-id="b7875-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7875-123">System.Boolean</span></span>

## <span data-ttu-id="b7875-124">Note</span><span class="sxs-lookup"><span data-stu-id="b7875-124">NOTES</span></span>

## <span data-ttu-id="b7875-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7875-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7875-126">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b7875-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b7875-127">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b7875-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b7875-128">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b7875-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


